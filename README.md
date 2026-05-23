# 🧠⛓️ AI × Web3 School — 个人学习记录

> **AI × Web3 School** 是由 LXDAO 与 ETHPanda 联合发起、Z.AI 领衔赞助的面向 AI × Web3 Builder 的共学与实践计划。
> 本仓库是我在第 0 期（Cohort 0）的个人学习日志与 Proof of Work。

- **Handbook**：https://aiweb3.school/zh/handbook/
- **WCB 课程页**：https://web3career.build/programs/AI-Web3-School
- **起始日期**：2026-05-19
- **学习周期**：4 周（Week 1 共学营 → Week 4 Hackathon Demo）

> ⚠️ 本仓库为 **Public**，请勿提交任何私钥、API Key、密码、.env 文件或他人隐私信息。

---

## 👤 学员画像

- **AI 基础**：有一定基础，日常使用 LLM / Agent / AI Coding
- **Web3 基础**：有一定基础，有钱包和合约操作经验
- **目标方向**：AI × Web3 交叉项目 / Hackathon
- **学习策略**：Bridge-first，4 周对齐官方大纲，按需补 AI/Web3 盲点

详细画像见 → [profile.md](./profile.md)

---

## 🤖 Learning Agent 说明

本仓库使用 **Hermes Agent** 作为 Learning Agent 辏助初始化和维护：

- **Agent 职责**：阅读 Handbook 章节内容、生成学习笔记、更新 learning-plan 进度、commit & push
- **人工确认**：所有 git commit/push 操作均由人工确认后才执行；笔记内容经人工审核
- **Agent 选择原因**：Hermes Agent 支持持久会话、定时任务、多工具调用（浏览器、终端、文件操作），适合长周期学习陪伴

---

## 🗺️ Week 1 学习目标

- 完成 AI 基础 5 章：LLM / Context / Agent / MCP / AI Coding
- 完成 Web3 基础 4 章：Wallet / Transaction & Gas / Smart Contract / Testnet
- 完成 Hermes Agent / Vibe Coding 实践
- 创建测试钱包，完成测试网转账
- 完成合约部署或调用（测试网）
- 记录打卡：成功案例 + 失败案例 + 人工修正经历

详细计划见 → [learning-plan.md](./learning-plan.md)

---

## 📁 目录结构

```
.
├── README.md                  # 本文件 — 项目简介、学习目标、目录说明
├── profile.md                 # 学员画像（技能背景、学习风格、兴趣方向）
├── learning-plan.md           # 4 周学习计划（含进度跟踪）
├── daily/                     # 每日学习笔记 (YYYY-MM-DD.md)
├── tasks/                     # 课程任务 & 实践练习记录
├── experiments/               # 代码实验 & 动手练习
├── handbook-feedback/         # Handbook 反馈收集
├── hackathon/                 # Hackathon 项目文件（Proposal、计划、最终提交）
├── submissions/               # 最终提交材料
└── templates/
    ├── daily-note.md          # 每日打卡模板
    └── task-note.md           # 任务笔记模板
```

---

## 📊 学习进度

### AI 基础

| 章节 | 状态 | 笔记 | 完成日期 |
|------|------|------|----------|
| [LLM](https://aiweb3.school/zh/handbook/ai/llm/) | ✅ | [05-20](./daily/2026-05-20.md) | 05-20 |
| [Context](https://aiweb3.school/zh/handbook/ai/context/) | ✅ | [05-21](./daily/2026-05-21.md) | 05-21 |
| [Agent](https://aiweb3.school/zh/handbook/ai/agent/) | ✅ | [05-22](./daily/2026-05-22.md) | 05-22 |
| [MCP](https://aiweb3.school/zh/handbook/ai/mcp/) | ⬜ | - | - |
| [AI Coding](https://aiweb3.school/zh/handbook/ai/ai-coding/) | ⬜ | - | - |

### Web3 基础

| 章节 | 状态 | 笔记 | 完成日期 |
|------|------|------|----------|
| [Wallet](https://aiweb3.school/zh/handbook/web3/wallet/) | ✅ | [05-20](./daily/2026-05-20.md) | 05-20 |
| [Transaction & Gas](https://aiweb3.school/zh/handbook/web3/transaction/) | ✅ | [05-21](./daily/2026-05-21.md) | 05-21 |
| [Smart Contract](https://aiweb3.school/zh/handbook/web3/smart-contract/) | ✅ | [05-22](./daily/2026-05-22.md) | 05-22 |
| [Testnet](https://aiweb3.school/zh/handbook/web3/testnet/) | ⬜ | - | - |

### AI × Web3 Bridge ⭐

| 章节 | 状态 | 笔记 | 完成日期 |
|------|------|------|----------|
| [Chain-aware Context](https://aiweb3.school/zh/handbook/bridge/chain-aware-context/) | ⬜ | - | - |
| [Web3 Tool Use](https://aiweb3.school/zh/handbook/bridge/web3-tool-use/) | ⬜ | - | - |
| [Agent Workflow](https://aiweb3.school/zh/handbook/bridge/agent-workflow/) | ⬜ | - | - |
| [Agent Wallet](https://aiweb3.school/zh/handbook/bridge/agent-wallet/) | ⬜ | - | - |
| [Machine Payment](https://aiweb3.school/zh/handbook/bridge/machine-payment/) | ⬜ | - | - |
| [Agent Identity](https://aiweb3.school/zh/handbook/bridge/agent-identity/) | ⬜ | - | - |
| [Agent Trust & Reputation](https://aiweb3.school/zh/handbook/bridge/agent-trust-and-reputation/) | ⬜ | - | - |
| [Settlement & Escrow](https://aiweb3.school/zh/handbook/bridge/settlement-and-escrow/) | ⬜ | - | - |
| [Verifiable AI](https://aiweb3.school/zh/handbook/bridge/verifiable-ai/) | ⬜ | - | - |
| [AI Security](https://aiweb3.school/zh/handbook/bridge/ai-security/) | ⬜ | - | - |

> 状态图例：⬜ 未开始 | 🔄 进行中 | ✅ 完成 | 📝 待复习

---

## 🔗 快速链接

- [Handbook 首页](https://aiweb3.school/zh/handbook/)
- [WCB Learning 页面](https://web3career.build/programs/AI-Web3-School)
- [4 周学习计划](./learning-plan.md)
- [每日打卡模板](./templates/daily-note.md)
- [任务笔记模板](./templates/task-note.md)
- [Handbook 反馈](./handbook-feedback/README.md)
- [Hackathon 项目](./hackathon/)
