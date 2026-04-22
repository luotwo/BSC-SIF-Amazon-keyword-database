# 美国SIM卡品类关键词全景（US站）

> 数据来源：SIF MCP 实测（market_get_keyword_demand + market_get_keyword_root_trend + market_get_keyword_competition）
> 数据截止日：2026-04-22
> 竞品 ASIN 拓词：competition API 已可用，待补充 48+ 竞品多竞品拓词

---

## 品类结构判断

美国 SIM 卡品类在亚马逊上呈现明显的**结构性分裂**：

- **实体 SIM 卡（Physical SIM）**：整体需求下滑，传统运营商预付费套件（T-Mobile、Verizon、AT&T、Mint Mobile、Visible）为主力竞品
- **eSIM（数字 SIM）**：唯一持续增长品类（+25% YoY），ABA 中词量级，尚处于成长期
- **SIM 卡配件**（否词区）：sim card adapter / sim card reader / sim ejector tool 是独立品类，不能混投

**核心结论**：主投词应以 `sim card`（大词锚定）+ `esim`（增长方向）+ 品牌截流词（Mint Mobile / T-Mobile / Verizon）构成三层架构。

---

## 第一层：ABA 分层 & 流量层级

### 大词（ABA < 10万）

| 关键词 | ABA 排名 | 周均搜索量 | 趋势 | YoY | 数据来源 |
|--------|---------|-----------|-----|-----|---------|
| sim card | 46,616 | 6,853 | 平稳走弱 | -22% | ABA实测 |

**注**：`sim card` ABA 46,616 确认为大词。月均搜索量约 2.7万（SIF competition 数据），竞品 133 个，Top3 集中度 32.7%（中等），可进入。

### 中词（ABA 10-50万 或 周均 2,500-12,500）[估算]

| 关键词 | ABA 估算 | 周均搜索量 | 趋势 | YoY | 词根类型 | 备注 |
|--------|---------|-----------|-----|-----|---------|-----|
| esim | 243,483 | 1,434 | 增长 | +25% | 共性词根 | ABA实测，唯一增长词 |
| mint mobile sim card | [估算]中词 | 1,818 | 峰值反转 | -32% | 品牌词根 | 历史增长，近期转负 |
| prepaid sim card | [估算]中词 | 1,464 | 走弱 | -45% | 共性词根 | 旺季6月，8周后到顶 |

> `esim` ABA 243,483 = 24.3万，属中词（10-50万区间）。

### 长尾词（ABA 50-100万 或 周均 500-2,500）[估算]

| 关键词 | 周均搜索量 | 趋势 | YoY | 词根类型 | 精准度 |
|--------|-----------|-----|-----|---------|-------|
| verizon sim card | 954 | 结构下滑 | -28% | 品牌词根 | 绝对精准 |
| nano sim card | 752 | 结构下滑 | -5% | 属性词根 | 绝对精准 |
| unlimited data sim card | 489 | 结构下滑 | -34% | 属性词根 | 绝对精准 |
| esim card | 393 | 走弱 | -54% | 属性词根 | 绝对精准 |
| t-mobile sim card | 287 | 下滑中恢复 | +58% | 品牌词根 | 绝对精准 |
| att sim card | 277 | 结构下滑 | +1% | 品牌词根 | 绝对精准 |
| international sim card | 257 | 结构下滑 | -34% | 受众词根 | 绝对精准 |
| data sim card | 237 | 结构下滑 | -14% | 属性词根 | 相对精准 |
| micro sim card | 242 | 结构下滑 | -8% | 属性词根 | 绝对精准 |

### 小词（ABA > 100万 或 周均 < 500）[估算]

| 关键词 | 周均搜索量 | 趋势 | YoY | 词根类型 | 精准度 |
|--------|-----------|-----|-----|---------|-------|
| travel sim card | 161 | 数据不足 | +21% | 受众词根 | 绝对精准 |
| visible sim card | 181 | 结构下滑 | +1% | 品牌词根 | 绝对精准 |
| prepaid data sim card | 156 | 结构下滑 | -34% | 属性词根 | 绝对精准 |
| 5g sim card | 151 | 结构下滑 | -11% | 属性词根 | 相对精准 |
| us sim card | 151 | 结构下滑 | -48% | 地理词根 | 绝对精准 |
| esim usa | 136 | 结构下滑 | -7% | 地理词根 | 绝对精准 |
| phone sim card | 136 | 结构下滑 | -20% | 共性词根 | 相对精准 |
| gsm sim card | 141 | 结构下滑 | 0% | 属性词根 | 相对精准 |
| 4g sim card | 131 | 平稳走弱 | -12% | 属性词根 | 相对精准 |
| sim card usa | 131 | 结构下滑 | -9% | 地理词根 | 绝对精准 |
| sim card for iphone | 126 | 结构下滑 | +7% | 设备词根 | 相对精准 |

---

## 第二层：词根分类

| 词根类型 | 代表词 | 广告用途 |
|---------|-------|---------|
| **共性词根** | sim card, prepaid sim card, esim | 必须覆盖，分层投放 |
| **属性词根** | nano sim card, micro sim card, unlimited data sim card, 5g sim card, 4g sim card, esim card, data sim card | 精准匹配，小词带大词 |
| **品牌词根** | mint mobile, t-mobile, verizon, att, visible | 精准截流，独立广告组（品牌词单独预算）|
| **受众词根** | international sim card, travel sim card, sim card usa, us sim card, esim usa | 场景化投放，配合 SB 人群定向 |
| **设备词根** | sim card for iphone | 精准但数量小，谨慎纳入 |
| **否定词根** | reader, adapter, tray, ejector, tool, storage | **直接进否词库** |

---

## 第三层：竞争强度（"sim card" 词实测）

来源：`market_get_keyword_competition(keyword="sim card", marketplace="US")`

| 维度 | 数据 |
|-----|-----|
| 竞品总数 | 133 |
| 集中度 | 中等（Top3 = 32.7% 点击） |
| 竞争模式 | ad_dominant（品牌广告占主导） |
| 自然位壁垒 | 117+ 评论、3.6★ 以上 |
| 可进入性 | 高（Top3 只拿 32.7%，格局分散） |
| 领先 ASIN | B08H5SM9M9（稳定 15 周，点击+转化双效率领先） |
| 价格带 | $2.9-$49（入门 SIM 套件 $2.9-$5，数据套餐 $19-$49） |
| 月均搜索量 | 约 27,400 |

**Top3 竞品参考**：

| ASIN | 价格 | 评分 | 评论数 | 月单量 | 竞争模式 |
|------|-----|-----|------|------|---------|
| B01N9XPPGZ | $2.9 | 3.4★ | 5,089 | 200+ | 品牌广告主导 |
| B07G9P5ZBW | $5 | 3.4★ | 3,118 | 500+ | 品牌广告主导 |
| B015QOGLL6 | $19 | 3.9★ | 1,998 | 200+ | SP 广告主导 |
| B0741FV7ZV | $45 | 4.2★ | 18,494 | 1,000+ | SP 广告主导 |

> 其余关键词竞争强度因 API 未逐词查询，标注 [缺失]，匹配建议保守处理。

---

## 第四层：匹配类型建议矩阵

| 关键词 | 流量层级 | 词根类型 | 精准度 | 匹配类型建议 | 广告策略建议 |
|--------|---------|---------|-------|------------|------------|
| sim card | 大词 | 共性词根 | 绝对精准 | 广泛先行 | 高竞争大词，0评论期不打首页首位精准；先用长尾词带动自然权重 |
| esim | 中词 | 共性词根 | 绝对精准 | 广泛先行 | 唯一增长词，优先布局；季节性弱，全年可投 |
| mint mobile sim card | 中词 | 品牌词根 | 绝对精准 | 精准首选（独立预算）| 竞品品牌截流；单独广告组，不与普通词混投 |
| prepaid sim card | 中词 | 共性词根 | 绝对精准 | 广泛先行→词组过渡 | 主推词，6月旺季前 8 周布局 |
| verizon sim card | 长尾词 | 品牌词根 | 绝对精准 | 精准首选（独立预算）| 竞品品牌截流，独立组 |
| t-mobile sim card | 长尾词 | 品牌词根 | 绝对精准 | 精准首选（独立预算）| 近期恢复 +58% YoY，截流机会窗口 |
| att sim card | 长尾词 | 品牌词根 | 绝对精准 | 精准首选（独立预算）| 稳定量，截流机会 |
| nano sim card | 长尾词 | 属性词根 | 绝对精准 | 精准守位（小词带大词）| 属性词，先精准建权重 |
| unlimited data sim card | 长尾词 | 属性词根 | 绝对精准 | 精准守位 | 结构下滑但精准；匹配数据 SIM 产品形态 |
| esim card | 长尾词 | 属性词根 | 绝对精准 | 精准守位 | eSIM 产品形态词 |
| international sim card | 长尾词 | 受众词根 | 绝对精准 | 精准首选 | 旅行场景；4周后到旺季，当前加量 |
| micro sim card | 长尾词 | 属性词根 | 绝对精准 | 精准守位 | 旧规格词，结构下滑，保守入 |
| data sim card | 长尾词 | 属性词根 | 相对精准 | 词组过渡 | 结果包含其他类目，监控 CTR |
| visible sim card | 小词 | 品牌词根 | 绝对精准 | 精准首选（独立预算）| 竞品截流，预算小 |
| international sim card | 小词→长尾 | 受众词根 | 绝对精准 | 精准首选 | 旅行用户，场景化 |
| 5g sim card | 小词 | 属性词根 | 相对精准 | 精准首选 | 精准度中等，监控 CTR |
| us sim card | 小词 | 地理词根 | 绝对精准 | 精准首选 | 结构下滑快，保守预算 |
| travel sim card | 小词 | 受众词根 | 绝对精准 | 精准首选 | 数据不足，入库但预算保守 |
| sim card for iphone | 小词 | 设备词根 | 相对精准 | 谨慎纳入 | 设备特定词，精准度依产品兼容性 |
| gsm sim card | 小词 | 属性词根 | 相对精准 | 否词候选 | 技术标准词，前台出现其他类目概率高 |
| 4g sim card | 小词 | 属性词根 | 相对精准 | 否词候选 | 旧标准词，精准度一般 |

---

## 否定关键词库

### 品类边界否词（直接否词，不入主库）

| 否词 | 否词来源 | 否词类型 | 否词原因 |
|-----|---------|---------|---------|
| sim card reader | 词频统计 | 精准否定 | USB/智能卡读卡器，完全不同品类；2,712/周大体量需精准否定 |
| sim card adapter | 词频统计 | 精准否定 | SIM卡尺寸转换配件，不同品类；1,843/周 |
| sim ejector tool | 词频统计 | 精准否定 | 手机工具，不同品类；464/周 |
| sim card tray | 词频统计 | 精准否定 | 手机维修零件，不同品类；146/周 |
| sim card storage | 词频统计 | 词组否定 | 存储盒配件，不同品类 |

### 技术标准否词候选（建议前台验证后否定）

| 否词候选 | 来源 | 建议类型 | 否定原因 |
|---------|-----|---------|---------|
| gsm sim card | 词频统计 | 词组否定候选 | GSM是旧制式，前台结果精准度低，需验证 |
| 4g sim card | 词频统计 | 词组否定候选 | 4G规格词，前台出现非目标产品概率高 |
| esim for iphone | 词频统计 | 精准否定候选 | 系统功能词，非Amazon可购买实体产品 |
| esim for android | 词频统计 | 精准否定候选 | 同上 |
| burner sim card | 词频统计 | 精准否定候选 | 无数据，且可能带来低质流量 |
| disposable sim card | 词频统计 | 精准否定候选 | 无数据，定位不清晰 |

> 否词候选不自动入库，需人工前台验证后决策。

---

## 旺季备战看板

| 关键词 | 当前距旺季（周）| 旺季月份 | 备战窗口 | 执行动作 |
|--------|--------------|---------|---------|---------|
| international sim card | 4周 | 5月 | ⚡立即行动 | 加大SP投入，锁定排名 |
| att sim card | 4周 | 5月 | ⚡立即行动 | 品牌组加量，守位 |
| prepaid data sim card | 4周 | 5月 | ⚡立即行动 | SP加量 |
| phone sim card | 4周 | 5月 | ⚡立即行动 | SP加量 |
| prepaid sim card | 8周 | 6月 | 🔥旺季准备 | 养权重，铺评价，旺季靠自然流量 |
| sim card adapter（否词）| — | — | — | 精准否词，全年生效 |
| sim card | 12周 | 7月 | 🔥旺季准备 | 布局自然排名，养权重 |
| us sim card | 12周 | 7月 | 🔥旺季准备 | 地理词，保守预算 |
| mint mobile sim card | 16周 | 8月 | 📈提前布局 | 品牌截流组提前建立 |
| verizon sim card | 16周 | 8月 | 📈提前布局 | 品牌截流组 |
| esim usa | 16周 | 7月 | 📈提前布局 | eSIM地理词，轻量投入 |
| esim | 20周 | 9月 | 📈提前布局 | 增长词，全年布局 |
| t-mobile sim card | 24周 | 10月 | 💤长线观察 | 恢复中，持续观察 |
| nano sim card | 32周 | 12月 | 💤长线观察 | 提前布局，入场成本低 |
| micro sim card | 32周 | 12月 | 💤长线观察 | 结构下滑，保守入 |
| esim card | 36周 | 1月 | 💤长线观察 | eSIM形态词，冬旺季布局 |

---

## 关键洞察（品类战略级）

### 1. 品类正在从物理SIM → eSIM迁移

- 几乎所有物理SIM词汇均处于结构性下滑（-15% ~ -48% YoY）
- `esim` 是唯一核心增长词（+25% YoY，年均+19%），且季节性低
- 建议：如产品支持eSIM，优先在 `esim` 上建立权重

### 2. 品牌词是SIM卡品类的特殊流量入口

- Mint Mobile（1,818/周）、Verizon（954/周）、T-Mobile（287/周）、AT&T（277/周）为主要品牌截流机会
- 需独立广告组，不与通用词混投
- Mint Mobile 近期由增长转为下滑(-32% YoY)，需跟踪

### 3. 旅行SIM是季节性场景词

- 旺季：5-7月（暑假旅行季）
- `international sim card` 距旺季仅4周，当前是加量窗口
- `travel sim card` 数据不足但趋势向上，轻量投入

### 4. 配件词是高风险否词区

以下词必须精准否定，否则浪费大量预算：
- `sim card reader`（2,712/周）
- `sim card adapter`（1,843/周）
- `sim ejector tool`（464/周）
- `sim card tray`（146/周）

### 5. 广告格局分散，可进入

- `sim card` Top3 仅拿 32.7% 点击，广告能买到位置
- 入场门槛：117+ 评论、3.6★ 以上可进自然位
- 新品策略：从 `esim`、属性词（nano/micro/unlimited data）的长尾切入，带动大词 `sim card` 权重

---

## Listing 联动建议

| 优先级 | 词类型 | 回写位置 |
|-------|-------|---------|
| P1 | sim card, prepaid sim card, esim | 标题前部词位 |
| P2 | nano sim card, unlimited data sim card, esim card | 五条卖点首行 |
| P3 | international sim card, travel sim card | A+ 文案 / Search Terms |
| 不回写 | mint mobile, t-mobile, verizon, att, visible（品牌截流词） | — |

---

## 竞品 ASIN 复用提示

本次 competition 数据中已拿到 20 个竞品 ASIN（B01N9XPPGZ、B07G9P5ZBW、B0741FV7ZV 等），完成 48+ 竞品拓词后，这批 ASIN 可**直接作为 SP 商品投放（ASIN 定投）候选池**，无需重新筛选。优先选评分与定价接近的竞品页面截流。

详见：[[strategy-new-product-ad-launch]] — 竞品 ASIN 的二次复用章节

---

## 待补充项

- [ ] 48+ 竞品 ASIN 多竞品拓词（当前仅靠关键词驱动，置信度受限）
- [ ] 品牌词单独 competition 查询（mint mobile / t-mobile / verizon 竞争强度）
- [ ] esim 词根下的长尾词（esim prepaid / esim data 等目前无数据）
- [ ] 月度数据更新：每月重拉 market_get_keyword_history，更新旺季距离
