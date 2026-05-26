# 📅 2026-05-26 线上活动笔记：Cobo Agentic Wallet

> 活动主题：Product manager of Cobo Agentic Wallet
> 活动日期：2026-05-26
> 记录时间：2026-05-26

---

## 🎯 会议概要

会议讨论了 AI Agent 在资金操作方面存在的风险及 Cobo 提出的解决方案，涵盖 Agent 发展历程、资金风险分析和完整产品方案。

---

## 📖 AI Agent 发展历程

### 1. 初期问答阶段
常用聊天机器人进入大众视野，AI 主要用于回答问题，如 ChatGPT 让 AI 成为大众生活一部分。

### 2. 提出建议阶段
2024 年 Copilot 概念涌现，AI 开始提出建议和制定复杂行动计划，但仍需人类批准和完成。

### 3. Agent 主流阶段
2025 年 Agent 概念成为 AI 世界主流，AI 能留存后台解决复杂工作流。

### 4. 自主探索阶段
2026 年自主性智能体进入人们生活，AI 不仅能执行工作流，还能自主探索和完成任务。

---

## ⚠️ AI Agent 动钱的痛点与风险

### 资金管理痛点
- 链上资金管理存在**资金归属安全**和**确定性**问题
- 基础设施是否到位也影响 Agent 代币消费

### 四类失控风险

| 风险类型 | 说明 |
|---|---|
| **Prompt Injection** | 因 prompt 受影响或模型幻觉导致执行未经授权交易 |
| **Shadow Operations** | Agent 在人类看不见的地方创建子账户和执行潜在路径 |
| **Unscoped Authority** | Agent 对链上资金有无限掌控能力 |
| **Zombie Permissions** | 授权未撤销导致交易处于系统性风险 |

---

## 🛡️ Cobo 的解决方案

### 1. MPC 钱包方案

采用 MPC 解决钱包底层安全性问题：
- **三方分片**：Cobo、Agent 和 Human 各自持有私钥分片
- **任意一方无独立掌控资金转移权限**
- **开放私钥导出功能**
- **2-2 threshold 模式**：
  - Agent + Cobo 共管（Agent 日常操作）
  - Human + Cobo 配合（人类审批操作）

### 2. Pact 授权协议

Pact 是一份结构化授权协议，包含四个核心组件：

| 组件 | 作用 |
|---|---|
| **Intent** | 期待 Agent 完成的具体任务或目标 |
| **Execution Plan** | AI 将 intent 转译成的具体执行计划 |
| **Policy** | 风控约束：预算审批、白名单链/TOKEN/合约限制等 |
| **Completion Condition** | 避免 Zombie permission：设定交易时效和数量上限 |

执行流程：
1. 用户表达意图
2. Agent 转译信息，封装成 Pact 推到 APP
3. 人类审阅批准
4. Agent 在可控范围内完成交易

### 3. Recipe 知识胶囊

解决「Agent 如何把事情做对」的问题：
- 预加载知识库，封装合约授权、特殊接口调用等知识
- 已上线 AaveV3、UniswapV3 等主流 Recipe
- 帮助 Agent 更好完成链上动作

---

## 🏦 产品应用与讨论

### 多 Agent 共管资产
- 单个用户可创建多个钱包，委托多个 Agent 管理理财资产
- 不同 Agent 资金彼此独立，更细颗粒度管理资金安全

### 小额免密支付
- 支持 X402 微支付协议
- 计划支持 Gasless 场景
- 可实现小额免密支付
- 在 Pact 体系下将转账行为限制在小风险敞口内

### 支付场景分析
- 主流支付场景目前偏向 Web2
- Agent Economy 未来更多基于链上自主、可追溯的交易形式
- 链上支付有快速、高效结算优势
- 短期内不会完全颠覆 Web2 支付
- 国内链上支付可能有联盟链或企业内部区块链基础设施场景

---

## 💬 Q&A 精华

| 问题 | 回答要点 |
|---|---|
| 首次执行 vs 重复操作 | 首次需授权，后续相同操作在条件不变时可自动执行 |
| Agent Wallet 与主钱包 | 操作同一账户，但 Agent 操作需人类审批且有资金上限 |
| Human-in-the-loop 趋势 | 短期是主流，未来 agent 足够智能时可能自发完成意图决策和支付 |
| Agent 掉线兜底 | MPC 钱包创建恢复有冗余设计 |
| 防范意图传递攻击 | 通过 Recipe 和 AI 助手审计 Pact |
| 高风险合约 | 需用户自行管理或提交需求添加约束条件 |
| 多跳风控 | 从合约地址、代币数量等参数层面进行风控管理 |

---

## 💡 个人收获

### 与 Week 1-2 学习的串联

1. **Agent 发展阶段的递进** — 从问答→建议→Agent→自主探索，和 Week 1 学的 Agent 第一性原则（"Agent 是被约束的执行循环"）形成了张力：越自主，约束越重要

2. **四类风险与 Bridge 概念对照**：
   - Prompt Injection → Week 1 Agent 章节的"幻觉"问题
   - Shadow Operations → Agent Workflow 的可观测性需求
   - Unscoped Authority → Agent Wallet 的权限分层
   - Zombie Permissions → Machine Payment 的时效性

3. **Pact = Payment Intent 的工程实现** — 昨天（05-25）学的 Payment Intent 是理论框架，Cobo 的 Pact 就是它的产品级实现！
   - Intent → Pact.intent
   - Budget Control → Pact.policy（预算审批、白名单）
   - Completion Condition → Pact.completion condition（时效+数量上限）

4. **Recipe = Web3 Tool Use 的知识封装** — Recipe 本质上就是把"如何调用 AaveV3/UniswapV3"这类链上操作知识，打包成 Agent 可直接使用的工具描述——这就是 Week 2 学的 Web3 Tool Use 概念在产品层的落地

5. **MPC 2-2 模式与 Account Abstraction 的关系** — MPC 分片替代了单私钥风险，2-2 threshold 相当于一种"双签"机制。这和 Week 1 概念卡片中的多签、智能账户形成了对照

### 踩坑预感

1. **Pact 的表达能力边界** — Policy 越细致，用户体验越复杂。和昨天分析的 Budget Control granularity 问题一致
2. **Recipe 的覆盖度** — 只覆盖主流协议（AaveV3、UniswapV3），长尾 DeFi 协议怎么办？Agent 能不能自己"学会"新协议？
3. **Human-in-the-loop 的体验瓶颈** — 如果每笔交易都要人批准，效率比手动操作还低。关键在于"条件不变时自动执行"的规则设计

---

## ❓ 待深入

- Cobo Agent Wallet 的 MPC 技术细节（TSS 算法、分片生成与恢复）
- Pact 协议是否开放标准？能否跨平台使用？
- Recipe 如何扩展到非 EVM 链？
- X402 微支付协议与 Cobo Pact 的集成方式
- Agent 自主阶段的安全边界设计
