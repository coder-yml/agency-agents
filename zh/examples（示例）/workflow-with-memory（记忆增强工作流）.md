# 多 Agent 工作流：带持久化记忆的初创公司 MVP

> 与 [workflow-startup-mvp.md](workflow-startup-mvp（初创企业MVP工作流）.md) 相同的初创公司 MVP 工作流，但增加了 MCP 记忆服务器在 Agent 之间管理状态。不再需要复制粘贴式的交接。

## 手动交接的问题

在标准工作流中，每次 Agent 之间的切换都像是这样：

```
Activate Backend Architect.

Here's our sprint plan: [粘贴 Sprint Prioritizer 的输出]
Here's our research brief: [粘贴 UX Researcher 的输出]

Design the API and database schema for RetroBoard.
...
```

你是胶水层。你在 Agent 之间复制粘贴输出，跟踪已完成的工作，并希望在此过程中不会丢失上下文。这种方式对小型项目有效，但在以下情况下会崩溃：

- 会话超时导致输出丢失
- 多个 Agent 需要相同的上下文
- QA 失败需要回退到之前的状态
- 项目跨越数天或数周，涉及多个会话

## 解决方案

安装了 MCP 记忆服务器后，Agent 将交付成果存储在记忆中，并自动检索所需内容。交接变成：

```
Activate Backend Architect.

Project: RetroBoard. Recall previous context for this project
and design the API and database schema.
```

Agent 在记忆中搜索 RetroBoard 的上下文，找到之前 Agent 存储的 Sprint 计划和研究简报，然后继续推进。

## 设置

安装任何支持 `remember`、`recall` 和 `rollback` 操作的 MCP 兼容记忆服务器。参见 [integrations/mcp-memory/README.md](../integrations（集成）/mcp-memory（MCP记忆集成）/README（集成说明）.md) 了解设置方法。

## 场景

与标准工作流相同：一个 SaaS 团队回顾工具（RetroBoard），4 周完成 MVP，独立开发者。

## Agent 团队

| Agent | 在此工作流中的角色 |
|-------|---------------------|
| Sprint Prioritizer | 将项目分解为每周 Sprint |
| UX Researcher | 通过快速用户访谈验证想法 |
| Backend Architect | 设计 API 和数据模型 |
| Frontend Developer | 构建 React 应用 |
| Rapid Prototyper | 快速让第一版运行起来 |
| Growth Hacker | 在构建的同时规划发布策略 |
| Reality Checker | 在每个里程碑前把关 |

每个 Agent 的提示词中都有一个记忆集成部分（参见 [integrations/mcp-memory/README.md](../integrations（集成）/mcp-memory（MCP记忆集成）/README（集成说明）.md) 了解如何添加）。

## 工作流

### 第 1 周：发现 + 架构

**步骤 1 — 激活 Sprint Prioritizer**

```
Activate Sprint Prioritizer.

Project: RetroBoard — a real-time team retrospective tool for remote teams.
Timeline: 4 weeks to MVP launch.
Core features: user auth, create retro boards, add cards, vote, action items.
Constraints: solo developer, React + Node.js stack, deploy to Vercel + Railway.

Break this into 4 weekly sprints with clear deliverables and acceptance criteria.
Remember your sprint plan tagged for this project when done.
```

Sprint Prioritizer 生成 Sprint 计划并将其存储在记忆中，标记为 `sprint-prioritizer`、`retroboard` 和 `sprint-plan`。

**步骤 2 — 激活 UX Researcher（并行）**

```
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief. Remember it tagged for this project when done.
```

UX Researcher 将研究简报存储到记忆中，标记为 `ux-researcher`、`retroboard` 和 `research-brief`。

**步骤 3 — 交接给 Backend Architect**

```
Activate Backend Architect.

Project: RetroBoard. Recall the sprint plan and research brief from previous agents.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Design:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation

Remember each deliverable tagged for this project and for the frontend-developer.
```

Backend Architect 自动从记忆中召回 Sprint 计划和研究简报。无需复制粘贴。它将 schema 和 API 规范存储到记忆中，标记为 `backend-architect`、`retroboard`、`api-spec` 和 `frontend-developer`。

### 第 2 周：构建核心功能

**步骤 4 — 激活 Frontend Developer + Rapid Prototyper**

```
Activate Frontend Developer.

Project: RetroBoard. Recall the API spec and schema from the Backend Architect.

Build the RetroBoard React app:
- Stack: React, TypeScript, Tailwind, Socket.io-client
- Pages: Login, Dashboard, Board view
- Components: RetroCard, VoteButton, ActionItem, BoardColumn

Start with the Board view — it's the core experience.
Focus on real-time: when one user adds a card, everyone sees it.
Remember your progress tagged for this project.
```

Frontend Developer 从记忆中提取 API 规范并据此构建。

**步骤 5 — 中期 Reality Check**

```
Activate Reality Checker.

Project: RetroBoard. We're at week 2 of a 4-week MVP build.

Recall all deliverables from previous agents for this project.

Evaluate:
1. Can we realistically ship in 2 more weeks?
2. What should we cut to make the deadline?
3. Any technical debt that will bite us at launch?

Remember your verdict tagged for this project.
```

Reality Checker 对目前所有产出拥有完整的可见性——Sprint 计划、研究简报、schema、API 规范和前端进度——无需你手动收集和粘贴。

### 第 3 周：打磨 + 落地页

**步骤 6 — Frontend Developer 继续，Growth Hacker 启动**

```
Activate Growth Hacker.

Product: RetroBoard — team retrospective tool, launching in 1 week.
Target: Engineering managers and scrum masters at remote-first companies.
Budget: $0 (organic launch only).

Recall the project context and Reality Checker's verdict.

Create a launch plan:
1. Landing page copy (hero, features, CTA)
2. Launch channels (Product Hunt, Reddit, Hacker News, Twitter)
3. Day-by-day launch sequence
4. Metrics to track in week 1

Remember the launch plan tagged for this project.
```

### 第 4 周：发布

**步骤 7 — 最终 Reality Check**

```
Activate Reality Checker.

Project: RetroBoard, ready to launch.

Recall all project context, previous verdicts, and the launch plan.

Evaluate production readiness:
- Live URL: [url]
- Test accounts created: yes
- Error monitoring: Sentry configured
- Database backups: daily automated

Run through the launch checklist and give a GO / NO-GO decision.
Require evidence for each criterion.
```

### 当 QA 失败时：回滚

在标准工作流中，当 Reality Checker 拒绝某个交付成果时，你需要回到负责的 Agent 那里并解释出了什么问题。有了记忆，恢复循环更紧凑：

```
Activate Backend Architect.

Project: RetroBoard. The Reality Checker flagged issues with the API design.
Recall the Reality Checker's feedback and your previous API spec.
Roll back to your last known-good schema and address the specific issues raised.
Remember the updated deliverables when done.
```

Backend Architect 可以准确看到 Reality Checker 标记了什么问题，召回自己之前的工作，回滚到检查点，并产出修复——全部无需你手动跟踪版本。

## 前后对比

| 方面 | 标准工作流 | 使用记忆 |
|------|-----------|---------|
| **交接** | 在 Agent 之间复制粘贴完整输出 | Agent 自动召回所需内容 |
| **上下文丢失** | 会话超时导致一切丢失 | 记忆跨会话持久化 |
| **多 Agent 上下文** | 手动从 N 个 Agent 汇总上下文 | Agent 按项目标签搜索记忆 |
| **QA 失败恢复** | 手动描述出了什么问题 | Agent 召回反馈 + 回滚 |
| **跨天项目** | 每次会话重新建立上下文 | Agent 从上次离开处继续 |
| **所需设置** | 无 | 安装 MCP 记忆服务器 |

## 关键模式

1. **用项目名标记一切**：这是让召回生效的关键。每条记忆都标记为 `retroboard`（或你的项目名称）。
2. **为接收方 Agent 标记交付成果**：当 Backend Architect 完成 API 规范后，将记忆标记为 `frontend-developer`，以便 Frontend Developer 在召回时找到。
3. **Reality Checker 获得完整可见性**：因为所有 Agent 都将工作存储在记忆中，Reality Checker 可以召回项目的所有内容，无需你手动汇总。
4. **回滚替代手动撤销**：当某件事失败时，回滚到最后一个检查点，而不是试图弄清楚改了什么。

## 提示

- 你不需要一次性修改所有 Agent。从最常用的 Agent 开始添加记忆集成，然后逐步扩展。
- 记忆指令是提示词，不是代码。LLM 会解释这些指令并按需调用 MCP 工具。你可以调整措辞以匹配你的风格。
- 任何支持 `remember`、`recall`、`rollback` 和 `search` 工具的 MCP 兼容记忆服务器都可以配合此工作流使用。
