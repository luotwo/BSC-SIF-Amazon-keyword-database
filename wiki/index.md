# Amazon 关键词库知识库索引

> 本知识库服务于亚马逊关键词调研与广告策略积累，以品类经验复用为核心目标。
> 查询时先读本索引定位页面，再深入阅读相关页面。

---

## 📦 品类/词库维度

| 页面 | 一句话摘要 |
|------|---------|
| [poc-radio-category.md](poc-radio-category.md) | POC对讲机（US站）品类关键词全景：ABA分层、词根结构、旺季规律、否词逻辑 |
| [sim-card-us-category.md](sim-card-us-category.md) | 美国SIM卡（US站）品类关键词全景：大词锚定+eSIM增长词+品牌截流三层架构，旺季7-8月，4个必须否词 |
| [dumbbell-collar-clamp-us-category.md](dumbbell-collar-clamp-us-category.md) | 哑铃配件扣（US站）双大词 barbell clamps/clips（均ABA<7万），weight前缀中词群，尺寸词细分，16竞品共性词表，旺季Q1 |

---

## 📣 广告策略维度

| 页面 | 一句话摘要 |
|------|---------|
| [strategy-new-product-ad-launch.md](strategy-new-product-ad-launch.md) | 新品广告启动路径：广泛先行→词组过渡→精准守位，0评论期约束与小词带大词 |
| [strategy-seasonal-keyword-planning.md](strategy-seasonal-keyword-planning.md) | 旺季关键词备战：四个时间窗口的操作节奏，以POC品类为案例 |
| [strategy-keyword-listing-linkage.md](strategy-keyword-listing-linkage.md) | 精准词回写Listing的触发条件与优先级：标题前部/卖点首行/A+文案 |

---

## 🔧 数据工具维度

| 页面 | 一句话摘要 |
|------|---------|
| [tool-sif-mcp-capabilities.md](tool-sif-mcp-capabilities.md) | SIF MCP各API能力边界、已知缺陷（competition UNAUTHORIZED）、root_trend vs demand 使用场景 |
| [tool-aba-rank-vs-search-volume.md](tool-aba-rank-vs-search-volume.md) | ABA真实排名 vs 搜索量估算的差异、换算区间表、何时必须用ABA |

---

## ⚡ 事件/异常维度

| 页面 | 一句话摘要 |
|------|---------|
| [event-poc-radio-pulse-2025q4.md](event-poc-radio-pulse-2025q4.md) | 2025年11-12月 poc radio 脉冲事件：周量从1K飙升至83K，ABA排名骤降至4K，持续4周后回落 |

---

## 维护约定

- 每次新品调研后，在对应品类页追加当期数据快照
- 发现新事件/异常时，新建事件页并更新 `log.md`
- 工具 API 出现新缺陷或修复时，更新 `tool-sif-mcp-capabilities.md`
- 本索引最多 200 行，超过时合并低价值条目
