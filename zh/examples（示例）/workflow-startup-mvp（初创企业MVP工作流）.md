# 多 Agent 工作流：初创公司 MVP

> 一个逐步演示的示例，展示如何协调多个 Agent 从想法到交付 MVP。

## 场景

你正在构建一个 SaaS MVP — 一个面向远程团队的团队回顾工具。你有 4 周时间交付一个可运行的产品，包含用户注册、核心功能和落地页。

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
```

**步骤 2 — 激活 UX Researcher（并行）**

```
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief.
```

**步骤 3 — 移交给 Backend Architect**

```
Activate Backend Architect.

Here's our sprint plan: [粘贴 Sprint Prioritizer 输出]
Here's our research brief: [粘贴 UX Researcher 输出]

Design the API and database schema for RetroBoard.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Deliver:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation
```

### 第 2 周：构建核心功能

**步骤 4 — 激活 Frontend Developer + Rapid Prototyper**

```
Activate Frontend Developer.

Here's the API spec: [粘贴 Backend Architect 输出]

Build the RetroBoard React app:
- Stack: React, TypeScript, Tailwind, Socket.io-client
- Pages: Login, Dashboard, Board view
- Components: RetroCard, VoteButton, ActionItem, BoardColumn

Start with the Board view — it's the core experience.
Focus on real-time: when one user adds a card, everyone sees it.
```

**步骤 5 — 中点 Reality Check**

```
Activate Reality Checker.

We're at week 2 of a 4-week MVP build for RetroBoard.

Here's what we have so far:
- Database schema: [粘贴]
- API endpoints: [粘贴]
- Frontend components: [粘贴]

Evaluate:
1. Can we realistically ship in 2 more weeks?
2. What should we cut to make the deadline?
3. Any technical debt that will bite us at launch?
```

### 第 3 周：打磨 + 落地页

**步骤 6 — Frontend Developer 继续，Growth Hacker 启动**

```
Activate Growth Hacker.

Product: RetroBoard — team retrospective tool, launching in 1 week.
Target: Engineering managers and scrum masters at remote-first companies.
Budget: $0 (organic launch only).

Create a launch plan:
1. Landing page copy (hero, features, CTA)
2. Launch channels (Product Hunt, Reddit, Hacker News, Twitter)
3. Day-by-day launch sequence
4. Metrics to track in week 1
```

### 第 4 周：发布

**步骤 7 — 最终 Reality Check**

```
Activate Reality Checker.

RetroBoard is ready to launch. Evaluate production readiness:

- Live URL: [url]
- Test accounts created: yes
- Error monitoring: Sentry configured
- Database backups: daily automated

Run through the launch checklist and give a GO / NO-GO decision.
Require evidence for each criterion.
```

## 关键模式

1. **顺序交接**：每个 Agent 的输出成为下一个 Agent 的输入
2. **并行工作**：UX Researcher 和 Sprint Prioritizer 可以在第 1 周同时运行
3. **质量门禁**：中点和发布前的 Reality Checker 防止交付有问题的代码
4. **上下文传递**：始终将前一个 Agent 的输出粘贴到下一个提示中 — Agent 不共享记忆

## 技巧

- 在步骤之间复制粘贴 Agent 输出 — 不要摘要，使用完整输出
- 如果 Reality Checker 标记了问题，循环回到相关专家进行修复
- 当你熟悉手动版本后，可以使用 Orchestrator Agent 自动化此流程
