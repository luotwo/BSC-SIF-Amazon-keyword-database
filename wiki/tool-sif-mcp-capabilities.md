---
tags: [tool, sif-mcp, api, data-source]
type: entity
date: 2026-04-22
---

# SIF MCP 工具能力图谱

> 记录各 API 的能力边界、数据字段含义、已知缺陷与推荐使用场景。
> 以实测为准，不引用外部文档。

---

## 一、API 能力总览

| API | 核心用途 | 关键输出字段 | 当前状态 |
|-----|--------|-----------|--------|
| `market_get_keyword_demand` | 批量探测关键词需求（趋势/季节/YoY） | `demand_intensity`, `trend.direction`, `yoy_change`, `seasonality`, `weeks_to_peak` | ✅ 正常 |
| `market_get_keyword_root_trend` | 单词根历史趋势 + **真实ABA排名** | `keyword_search_volumes[]`, **`keyword_ranks[]`**, `ext_search_volumes[]`, `latest.coverage_ratio` | ✅ 正常 |
| `market_get_keyword_history` | 多词历史搜索量序列 | `history[].volume` | ✅ 正常 |
| `market_get_keyword_competition` | 竞争强度 + 竞品排名 + Top3集中度 | `top_competitors[]`, `market_structure`, `concentration_profile` | ❌ **UNAUTHORIZED** |
| `market_get_asin_keyword_signals` | ASIN关键词信号（拓词用） | `keywords[].keyword`, `keywords[].score` | ✅ 正常（需ASIN） |
| `ops_get_asin_traffic_trend` | ASIN流量趋势（自然+广告） | `nfScore`, `spScore`, `sbScore`, `sbvScore` | ✅ 正常（需ASIN） |

---

## 二、`market_get_keyword_root_trend` 详解

### 为什么优先用它获取ABA排名

- 返回 `keyword_ranks[]` 字段 = **真实ABA搜索排名**（周粒度历史序列）
- 比 `market_get_keyword_demand` 的周均搜索量估算精准得多
- `latest.keyword_rank` 是最近一周的真实ABA值
- `latest.coverage_ratio` 表示该词流量被已知ASIN覆盖的比例（<1说明流量分散）

### 关键字段解读

```
keyword_search_volumes[]  → SIF自有口径搜索量（可能与ABA有差异）
keyword_ranks[]           → 真实ABA排名（重要！越小=流量越大）
ext_search_volumes[]      → 扩展口径搜索量（通常 >= keyword_search_volumes）
latest.coverage_ratio     → 已知ASIN覆盖率（two way radio=0.33，说明大量流量去向不明）
```

### null值的含义

- `keyword_ranks[]` 中出现 null = 该周 ABA 数据缺失（搜索量太低未被ABA收录）
- 大量 null 的词（如 `lte radio`）说明该词体量极小，不稳定

---

## 三、`market_get_keyword_demand` vs `market_get_keyword_root_trend`

| 维度 | demand | root_trend |
|-----|--------|-----------|
| 一次查询词数 | 1-20个 | 1个 |
| 是否返回ABA排名 | ❌ 不返回 | ✅ 返回 `keyword_ranks[]` |
| 趋势判断 | ✅ 丰富（YoY/季节/动量/诊断） | 仅原始序列，需自行判断 |
| 适用场景 | 批量筛词、快速探测需求 | 获取真实ABA、深入单词历史 |
| 推荐使用顺序 | 第1步：批量探测候选词 | 第2步：对入选词获取ABA排名 |

---

## 四、已知缺陷记录

### ❌ `market_get_keyword_competition` UNAUTHORIZED（2026-04-22确认）

- **现象**：调用返回 401/UNAUTHORIZED 或类似权限错误
- **影响字段**：竞争强度、CPC参考、Top3集中度、竞品排名变化
- **处理方式**：相关字段一律标注 **[缺失]**，不用搜索量或其他数据替代
- **修复状态**：未修复（截至2026-04-22）
- **影响范围**：POC品类词库全部词的竞争强度字段

### ⚠️ 部分词 ABA 数据稀疏（大量null周）

- **触发条件**：词的周搜索量低于ABA收录阈值（大约 <100/周）
- **受影响词**：`lte radio`, `push to talk radio`, `network walkie talkie` 等
- **处理方式**：`latest.keyword_rank = null` 时，以搜索量估算层级，标注 **[估算]**

---

## 五、`coverage_ratio` 的含义与应用

- `coverage_ratio = keyword_search_volumes / ext_search_volumes`
- **比值接近1**（如 `4g walkie talkie` = 1.0）：该词流量基本被已知ASIN覆盖，竞争格局清晰
- **比值远小于1**（如 `two way radio` = 0.33）：大量流量流向未被SIF收录的ASIN，竞争更复杂，总盘更大
- 对大词（`two way radio`），ext_search_volumes（10,243）比 keyword_search_volumes（3,388）高3倍，说明实际市场规模更大

---

## 六、推荐调用顺序（POC品类调研流程）

```
1. market_get_keyword_demand([候选词列表])
   → 批量过滤，保留有数据且趋势向好的词

2. market_get_keyword_root_trend(核心词)
   → 获取真实ABA排名，确认流量层级

3. market_get_keyword_competition(关键词)   ← 当前 UNAUTHORIZED，跳过
   → 获取竞争强度（恢复后补填）

4. market_get_asin_keyword_signals(竞品ASIN × 48+)
   → 多竞品拓词，发现未覆盖的共性词根
```

---

## 相关页面

- [[tool-aba-rank-vs-search-volume]] — ABA排名换算方法
- [[poc-radio-category]] — POC品类实战案例
- [[event-poc-radio-pulse-2025q4]] — root_trend发现脉冲事件的案例
