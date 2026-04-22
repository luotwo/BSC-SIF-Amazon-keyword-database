---
tags: [strategy, seasonal, keyword-planning, peak-season]
type: concept
date: 2026-04-22
---

# 旺季关键词备战框架

> 来源：SKILL.md SOP规范 + POC品类实跑数据（2026-04-22）

---

## 四个备战窗口

| 窗口 | 距旺季 | 核心动作 | 预算状态 |
|-----|-------|--------|--------|
| ⚡ **立即行动** | 0–4周 | 全力冲量，广告预算拉满，守住排名 | 高预算 |
| 🔥 **旺季准备** | 4–12周 | 加大SP投入锁定排名，铺评价提升CVR | 中偏高 |
| 📈 **提前布局** | 12–32周 | 广泛先行建立权重，入场成本最低 | 中等 |
| 💤 **长线观察** | 32周+ | 精准小预算测CTR，低成本卡位 | 低预算 |

---

## 入场时机原则

**淡季是入场最佳时机**，原因：
1. CPC竞价低（竞争者减少出价）
2. 自然排名积累成本低（广告转化带动自然排名）
3. 旺季到来时已建立权重，CPC和ACOS都更优

---

## POC品类（2026-04-22）各词备战状态

| 关键词 | 备战窗口 | 距旺季 | 推荐动作 |
|--------|--------|-------|--------|
| `two way radio` | 🔥旺季准备 | 12周（7月旺季） | 加大SP广泛投入，锁定排名 |
| `4g walkie talkie` | 🔥旺季准备 | 12周（7月旺季） | 维持精准守位，养自然排名 |
| `walkie talkie long range` | 📈提前布局 | 28周（11月旺季） | 精准守位积累权重 |
| `poc radio` | 📈提前布局 | 32周（11月旺季） | 广泛先行建权重，入场成本最低 |
| `ptt radio` | 💤长线观察 | 40周（2月旺季） | 精准小预算测CTR |
| `lte walkie talkie` | ⚡立即行动 | 0周（当前旺季） | 维持最低预算守住曝光 |

---

## 脉冲型旺季的特殊处理

> 适用：事件驱动型需求词（如 `poc radio` 的Q4脉冲）

- 区别于季节性旺季，脉冲旺季**不可预测**，但有规律性（台风/灾害季）
- 备战策略：
  1. 每年10月初预设脉冲备用预算（正常月预算的2-3倍）
  2. 监控 ABA 排名，`poc radio` ABA 突破 50K 时触发预警
  3. 脉冲结束后（约4周）主动降回预算
- 详见 [[event-poc-radio-pulse-2025q4]]

---

## 旺季结束后的处理

- 旺季后自然订单占比上升时，优先评估是否释放预算保利润，**不要机械继续扩量**
- 广告关键词自然排名已稳固的词，可降低广泛匹配出价，重点维持精准匹配守位
- 旺季期产出的高转化词，及时回写 Listing（见 [[strategy-keyword-listing-linkage]]）

---

## 数据获取方式

用 `market_get_keyword_demand` 获取 `weeks_to_peak` 字段：

```python
demand_result["action_phase"]   # prepare / ramp_up / harvest / prepare
demand_result["weeks_to_peak"]  # 距下次旺季周数
demand_result["action_hint"]    # 具体建议文本
```

---

## 相关页面

- [[poc-radio-category]] — POC品类各词备战状态
- [[event-poc-radio-pulse-2025q4]] — 脉冲型旺季案例
- [[strategy-new-product-ad-launch]] — 新品广告启动路径
- [[tool-sif-mcp-capabilities]] — demand API字段说明
