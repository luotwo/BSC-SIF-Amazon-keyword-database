---
tags: [category, poc-radio, walkie-talkie, US]
type: entity
date: 2026-04-22
marketplace: US
---

# POC对讲机 品类关键词全景（US站）

> 数据截止：2026-04-22 | 数据来源：SIF MCP（`market_get_keyword_demand` + `market_get_keyword_root_trend`）

---

## 一、词库分层总表

| 关键词 | ABA排名 | 流量层级 | 词根类型 | 精准度 | 匹配建议 | 周均搜索量 | YoY | 旺季月 | 距旺季_周 |
|--------|--------|--------|--------|-------|--------|----------|-----|-------|---------|
| `two way radio` | 99,187 | 大词 | 共性词根 | 相对精准 | 广泛先行 | ~3,388 | 平稳 | 7月/11月 | 12 |
| `poc radio` | 319,523 | 中词 | 品类词根 | 绝对精准 | 广泛先行 | ~1,101 | +129% | 11月/12月/2月 | 32 |
| `walkie talkie long range` | [估算] | 长尾词 | 属性词根 | 绝对精准 | 精准守位 | ~1,585 | -3% | 11月/8月 | 28 |
| `ptt radio` | [估算] | 小词 | 品类词根 | 绝对精准 | 精准首选 | ~328 | +50% | 2月/1月 | 40 |
| `4g walkie talkie` | 1,517,193 | 小词 | 属性词根 | 相对精准 | 精准首选 | ~237 | +5% | 7月/11月 | 12 |
| `lte walkie talkie` | [估算] | 小词 | 属性词根 | 相对精准 | 精准首选 | ~212 | 平稳 | 10月/4月 | 0 |
| `poc walkie talkie` | 无数据 | 小词 | 品类词根 | 绝对精准 | 精准首选 | ~0 | 下滑 | - | - |

> **层级判断依据**：优先使用真实ABA排名，无ABA时按周均搜索量换算（标注[估算]）。
> 换算区间：大词<10万，中词10-50万，长尾词50-100万，小词>100万。

---

## 二、词根结构分析

### 主词根覆盖

| 词根类型 | 代表词 | 作用 |
|--------|-------|-----|
| 共性词根 | `two way radio` | 大类流量入口，必须覆盖 |
| 品类词根 | `poc radio`, `ptt radio` | 精准用户核心词，主攻 |
| 属性词根 | `walkie talkie long range`, `4g walkie talkie`, `lte walkie talkie` | 辅助词，精准匹配埋位 |

### 缺失词根类型

- **品牌词根**：本次未调研竞品品牌词（需补充48+竞品ASIN反查后获取）
- **受众词根**：未发现有效受众词（如 `radio for construction`, `radio for security guard`）

---

## 三、旺季规律

```
poc radio:          ██████████░░░░░░░░░░████████████████████░░
                    Q1          Q2          Q3          Q4
                    旺          淡          淡          旺峰

two way radio:      ████████░░░░░████████████░░░░░░░░░░████████
                    Q1          Q2          Q3          Q4
                    平          夏旺         平          冬旺

ptt radio:          ████████████░░░░░░░░░░░░░░░░░░░░████████████
                    旺(1-3月)   淡季(4-9月)          旺(10-12月)
```

**关键节点**：
- `poc radio` 11-12月为年度最高峰，2月次高峰
- `two way radio` 有双旺季：7月（户外季）+ 11月（Q4促销）
- `ptt radio` 旺季在Q1（1-3月），淡季为5-9月

---

## 四、否词库（种子否词）

| 否词 | 否词类型 | 原因 |
|-----|--------|-----|
| `zello walkie talkie` | 精准否定 | App品牌词，买家意图是软件而非硬件，需求-21%/年 |
| `network walkie talkie` | 精准否定 | 无ABA数据，量极低，前台不明确 |
| `internet walkie talkie` | 精准否定 | 无历史数据，量可忽略 |
| `long range two way radio` | 词组否定 | 结构性下滑-39%/年，需求萎缩 |
| `lte radio` | 精准否定 | 数据稀疏，量少，与poc radio重叠但更弱 |

---

## 五、Listing 联动分配

| 回写位置 | 对应词 |
|--------|-------|
| **标题前部** | `poc radio` |
| **卖点首行** | `ptt radio`, `walkie talkie long range` |
| **A+文案** | `two way radio`, `4g walkie talkie`, `lte walkie talkie` |
| **不回写** | 否词、`poc walkie talkie` |

---

## 六、竞争强度

> ⚠️ 本次调研期间 `market_get_keyword_competition` API 全程 UNAUTHORIZED，竞争强度字段全部标注 **[缺失]**。
> 见 [[tool-sif-mcp-capabilities]] 的已知缺陷记录。

---

## 七、特殊信号

### poc radio 2025年Q4脉冲事件

- 正常周均：~1,000-1,400
- 2025-11-23 周起：骤升至5,095 → 12月峰值83,309
- ABA排名从~325K骤降至4,139（全品类顶级词水准）
- 持续约4周后快速回落至当前~1,101水平
- 详见 [[event-poc-radio-pulse-2025q4]]

---

## 相关页面

- [[strategy-new-product-ad-launch]] — 新品广告启动路径
- [[strategy-seasonal-keyword-planning]] — 旺季备战窗口操作
- [[tool-sif-mcp-capabilities]] — API使用限制
- [[tool-aba-rank-vs-search-volume]] — ABA排名换算方法
- [[event-poc-radio-pulse-2025q4]] — Q4脉冲事件记录
