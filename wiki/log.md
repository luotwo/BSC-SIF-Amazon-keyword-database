# 知识库操作日志

---

## [2026-04-22] init | 知识库初始化

- 创建 `wiki/` 目录结构
- 创建 `wiki/index.md`（四维度索引）
- 触发来源：用户要求搭建更细维度的品类知识库

---

## [2026-04-22] ingest | 哑铃配件扣 多竞品拓词完成（US站）

**数据来源**：`market_get_asin_keyword_signals` × 19 竞品 ASIN（16 个有效，3 个错误品类已过滤）

**更新页面**：
- `dumbbell-collar-clamp-us-category.md` — 全面扩充：
  - 大词层：barbell clips 从"中词估算"更正为**大词（ABA 69,567）**
  - 新增"weight"前缀中词群：weight clamps、weight clips for bars、weight bar clamps
  - 新增尺寸词层：1 inch / 2 inch 系列词，含 ABA 确认数据
  - 新增「多竞品拓词结果」章节（共性词覆盖度表格）
  - 新增否词：`bar clamp`（木工工具）、`cap barbell`、`rogue fitness` 等
  - 新增 SP 商品定投候选池

**关键要点**：
- `barbell clips` 实测 ABA 69,567 = **大词**，非估算中词，是品类第二锚词
- `weight clips for bars`（848/周）+ `weight clamps`（939/周）+ `weight bar clamps`（752/周）三词均为 12-13/16 竞品共性词，初始词表遗漏
- 2英寸词系列（barbell clamps 2 inch / 2 inch barbell clamps）出现频率极高：16/16 和 15/16 竞品覆盖
- `bar clamp`（ABA 261,635）确认为木工工具词，须加否词库
- 发现两个纯 SB 玩家（B01MRGIOQH / B01N09NKVL）无自然排名，非自然竞争威胁
- 错误品类 ASIN（barbell pad × 2 + ankle strap × 1）需从 SP 商品定投候选池排除

---

## [2026-04-22] ingest | 哑铃配件扣品类关键词调研（US站）

**数据来源**：SIF MCP 实测（`market_get_keyword_demand` × 30词 + `market_get_keyword_root_trend` for "barbell clamps" + `market_get_keyword_competition` for "barbell clamps"）

**创建页面**：
- `dumbbell-collar-clamp-us-category.md` — 品类全景，双锚词结构，转化缺口分析，旺季看板，否词库

**关键要点**：
- `barbell clamps` ABA 42,936 = 大词，月均 ~29,500，竞品 257 个，**转化缺口开放 4 周且持续扩大**（Top3 点击 52.6% vs 转化 25.3%）
- `barbell clips`（4,732/周）是增长词（+14% YoY），与 barbell clamps 构成双锚词
- `weight clips`（1,671/周）恢复最强（+45% YoY）
- 旺季：1-3月（新年健身季），当前（4月）为淡季入口，低成本布局期
- 自然位壁垒极高：需 4.8★ + 12,000+ 评论才能稳住
- 价格主力区间：$9.99-$19.95
- 否词：pipe clamp / hose clamp / dog collar / pet collar / hair clamp 等非健身类目词

---

## [2026-04-22] ingest | 经验对比：公众号文章 vs SOP（竞品ASIN复用技巧）

**来源**：微信公众号文章《亚马逊关键词库搭建：我是如何30秒拿到5000+流量词的》

**新增内容**：
- `strategy-new-product-ad-launch.md` — 新增「竞品 ASIN 二次复用」章节：拓词用的 48+ ASIN 直接复用为 SP 商品投放候选池
- `sim-card-us-category.md` — 新增竞品 ASIN 复用提示段落

**文章与 SOP 主要差异**（已记录，不重复入库）：
- 文章用搜索量分层，SOP 用 ABA 排名优先 → SOP 更准确
- 文章无否词库 → SOP 必建
- 文章「潜力词」≈ SOP 禁止的「机会词固定层级」用法 → 沿用 SOP 口径
- 文章未区分品牌词 → SOP 保持独立广告组要求

---

## [2026-04-22] ingest | POC对讲机品类关键词调研（US站）

**数据来源**：SIF MCP 实测（`market_get_keyword_demand` + `market_get_keyword_root_trend`）

**创建页面**：
- `poc-radio-category.md` — 品类全景，7个词完整分层
- `event-poc-radio-pulse-2025q4.md` — 2025年Q4脉冲事件记录

**更新页面**：无（首次建库）

**关键要点**：
- `poc radio` 确认为核心词（ABA 319K = 中词），年均增长+674%
- `two way radio` 为大类锚词（ABA 99K = 大词），覆盖率仅0.33
- `competition API` 全程 UNAUTHORIZED，竞争强度字段全部标注[缺失]
- 2025年11-12月发现 poc radio 脉冲异常（83K周量），首次记录

---

## [2026-04-22] ingest | 美国SIM卡品类关键词调研（US站）

**数据来源**：SIF MCP 实测（`market_get_keyword_demand` × 40词 + `market_get_keyword_root_trend` × 2词 + `market_get_keyword_competition` for "sim card"）

**创建页面**：
- `sim-card-us-category.md` — 品类全景，含大词/中词/长尾/小词分层，词根分类，否词库，旺季看板

**关键要点**：
- `sim card` ABA 46,616 = 大词，月均搜索量约2.7万，竞品133个，Top3集中度32.7%（中等）
- `esim` ABA 243,483 = 中词，1,434/周，唯一增长词（+25% YoY），年均+19%
- 配件否词4个必须精准否词：sim card reader（2,712/周）、sim card adapter（1,843/周）、sim ejector tool（464/周）、sim card tray（146/周）
- 品牌截流词：mint mobile（1,818/周）、verizon（954/周）、t-mobile（287/周）、att（277/周）
- 旺季：7-8月（暑假旅行季），international sim card 4周后到旺季（当前加量窗口）
- 品类结构性分裂：物理SIM词普遍下滑，eSIM方向增长
- 待补充：48+ 竞品 ASIN 多竞品拓词

---

## [2026-04-22] ingest | 广告策略与工具规范页面

**创建页面**：
- `strategy-new-product-ad-launch.md`
- `strategy-seasonal-keyword-planning.md`
- `strategy-keyword-listing-linkage.md`
- `tool-sif-mcp-capabilities.md`
- `tool-aba-rank-vs-search-volume.md`

**数据依据**：SKILL.md SOP规范 + 本次POC品类实跑验证
