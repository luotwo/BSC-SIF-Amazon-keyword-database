---
tags: [tool, aba-rank, search-volume, keyword-tiering]
type: concept
date: 2026-04-22
---

# ABA真实排名 vs 搜索量估算

> 来源：SKILL.md SOP规范 + POC品类实跑验证（BENCHMARK.md）

---

## 核心原则

**有真实ABA排名时，必须用ABA排名判断流量层级，不允许仅凭搜索量分层。**

---

## 层级换算区间表

| 流量层级 | ABA排名区间 | 周均搜索量换算 | 广告策略含义 |
|--------|-----------|------------|-----------|
| **大词** | < 10万 | 周均 > 12,500 | 高竞争，新品不打首页精准，先广泛建权重 |
| **中词** | 10–50万 | 周均 2,500–12,500 | 主推窗口，手动广泛先行 |
| **长尾词** | 50–100万 | 周均 500–2,500 | 精准匹配，小词带大词 |
| **小词** | > 100万 | 周均 < 500 | 精准首选，Listing埋词 |
| **品牌词** | 不适用 | 不限 | 独立预算，精准匹配截流 |

---

## 为什么不能只用搜索量

### 案例1：`walkie talkie`（来自BENCHMARK.md）

- 周均搜索量：中等水平（曾被误判为中词）
- 真实ABA排名：**15,914**（大词区间）
- 正确层级：**大词**
- 错误后果：新品0评论期用精准匹配打首页 → ACOS爆表

### 案例2：`gmrs radio`（来自BENCHMARK.md）

- 周均搜索量：中等（曾被误判为中词）
- 真实ABA排名：**34,697**（大词区间）
- 正确层级：**大词**

### 案例3：`poc radio`（POC品类实测）

- 周均搜索量：~1,101
- 按搜索量换算：长尾词（500–2,500区间）
- 真实ABA排名：**319,523**（中词区间）
- 正确层级：**中词**（广泛先行而非精准守位）

---

## 何时必须获取ABA排名

1. **制定匹配类型建议前**：大词/中词 vs 长尾词/小词，广告策略差异显著
2. **Listing 埋词优先级排序前**：标题前部词必须是真实大词/中词
3. **新品广告预算分配前**：大词预算优先级高，但不能在0评论期打首页精准

---

## 估算标注规范

- 有真实ABA数据：直接填入 `ABA排名` 字段
- 无ABA数据（`keyword_rank = null`）：
  - 用周均搜索量换算层级
  - `流量层级` 字段标注 `[估算]`
  - `ABA排名` 字段留空或填0

---

## 获取真实ABA排名的方法

使用 `market_get_keyword_root_trend` 的 `latest.keyword_rank` 字段：

```
market_get_keyword_root_trend(keyword="poc radio", marketplace="US", granularity="week")
→ latest.keyword_rank = 319523  ← 这就是真实ABA排名
```

见 [[tool-sif-mcp-capabilities]] 的详细说明。

---

## 相关页面

- [[tool-sif-mcp-capabilities]] — root_trend API说明
- [[strategy-new-product-ad-launch]] — 不同层级词的广告启动策略
- [[poc-radio-category]] — POC品类实测分层结果
