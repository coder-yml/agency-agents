# ⚡ NEXUS 快速入门指南

> **5 分钟内从零到编排化多代理管道。**

---

## 什么是 NEXUS？

**NEXUS**（专家网络，战略统一）将 The Agency 的 AI 专家转变为协调的管道。NEXUS 精确定义了谁做什么、何时做，以及在每个步骤如何验证质量，而不是逐个激活代理并寄希望于它们能协作。

## 选择你的模式

| 我想要... | 使用 | 代理数量 | 时间 |
|-------------|-----|--------|------|
| 从零构建完整产品 | **NEXUS-Full** | 全部 | 12-24 周 |
| 构建功能或 MVP | **NEXUS-Sprint** | 15-25 | 2-6 周 |
| 执行特定任务（修复 bug、营销活动、审计） | **NEXUS-Micro** | 5-10 | 1-5 天 |

---

## 🚀 NEXUS-Full：启动完整项目

**复制此提示以激活完整管道：**

```
以 NEXUS-Full 模式激活 Agents Orchestrator。

项目：[你的项目名称]
规格说明：[描述你的项目或链接到规格文档]

执行完整的 NEXUS 管道：
- 第 0 阶段：发现（Trend Researcher、Feedback Synthesizer、UX Researcher、Analytics Reporter、Legal Compliance Checker、Tool Evaluator）
- 第 1 阶段：战略（Studio Producer、Senior Project Manager、Sprint Prioritizer、UX Architect、Brand Guardian、Backend Architect、Finance Tracker）
- 第 2 阶段：基础（DevOps Automator、Frontend Developer、Backend Architect、UX Architect、Infrastructure Maintainer）
- 第 3 阶段：构建（开发↔QA 循环 — 所有工程代理 + Evidence Collector）
- 第 4 阶段：加固（Reality Checker、Performance Benchmarker、API Tester、Legal Compliance Checker）
- 第 5 阶段：发布（Growth Hacker、Content Creator、所有营销代理、DevOps Automator）
- 第 6 阶段：运营（Analytics Reporter、Infrastructure Maintainer、Support Responder，持续进行）

每个阶段之间有质量关卡。所有评估需要证据。
每个任务最多重试 3 次，超出则升级。
```

---

## 🏃 NEXUS-Sprint：构建功能或 MVP

**复制此提示：**

```
以 NEXUS-Sprint 模式激活 Agents Orchestrator。

功能/MVP：[描述你要构建的内容]
时间线：[目标周数]
跳过第 0 阶段（市场已验证）。

Sprint 团队：
- PM：Senior Project Manager、Sprint Prioritizer
- 设计：UX Architect、Brand Guardian
- 工程：Frontend Developer、Backend Architect、DevOps Automator
- QA：Evidence Collector、Reality Checker、API Tester
- 支持：Analytics Reporter

从第 1 阶段开始，进行架构和冲刺规划。
对所有实现任务运行开发↔QA 循环。
发布前必须获得 Reality Checker 批准。
```

---

## 🎯 NEXUS-Micro：执行特定任务

**选择你的场景并复制提示：**

### 修复 Bug
```
激活 Backend Architect 调查并修复 [BUG 描述]。
修复后，激活 API Tester 验证修复。
然后激活 Evidence Collector 确认没有视觉回归。
```

### 运行营销活动
```
激活 Social Media Strategist 作为 [活动描述] 的活动负责人。
团队：Content Creator、Twitter Engager、Instagram Curator、Reddit Community Builder。
Brand Guardian 在发布前审查所有内容。
Analytics Reporter 每天跟踪绩效。
Growth Hacker 每周优化渠道。
```

### 进行合规审计
```
激活 Legal Compliance Checker 进行全面合规审计。
范围：[GDPR / CCPA / HIPAA / 全部]
审计后，激活 Executive Summary Generator 创建干系人报告。
```

### 调查性能问题
```
激活 Performance Benchmarker 诊断性能问题。
范围：[API 响应时间 / 页面加载 / 数据库查询 / 全部]
诊断后，激活 Infrastructure Maintainer 进行优化。
DevOps Automator 部署任何基础设施变更。
```

### 市场研究
```
激活 Trend Researcher 进行 [领域] 的市场情报。
交付物：竞争格局、市场估算、趋势预测。
研究后，激活 Executive Summary Generator 生成执行简报。
```

### UX 改进
```
激活 UX Researcher 识别 [功能/产品] 中的可用性问题。
研究后，激活 UX Architect 设计改进方案。
Frontend Developer 实现变更。
Evidence Collector 验证改进效果。
```

---

## 📁 战略文档

| 文档 | 用途 | 位置 |
|----------|---------|----------|
| **主策略** | 完整的 NEXUS 规范 | `strategy/nexus-strategy.md` |
| **第 0 阶段 Playbook** | 发现与情报 | `strategy/playbooks/phase-0-discovery.md` |
| **第 1 阶段 Playbook** | 战略与架构 | `strategy/playbooks/phase-1-strategy.md` |
| **第 2 阶段 Playbook** | 基础与脚手架 | `strategy/playbooks/phase-2-foundation.md` |
| **第 3 阶段 Playbook** | 构建与迭代 | `strategy/playbooks/phase-3-build.md` |
| **第 4 阶段 Playbook** | 质量与加固 | `strategy/playbooks/phase-4-hardening.md` |
| **第 5 阶段 Playbook** | 发布与增长 | `strategy/playbooks/phase-5-launch.md` |
| **第 6 阶段 Playbook** | 运营与演进 | `strategy/playbooks/phase-6-operate.md` |
| **激活提示** | 即用型代理提示 | `strategy/coordination/agent-activation-prompts.md` |
| **交接模板** | 标准化交接格式 | `strategy/coordination/handoff-templates.md` |
| **启动 MVP Runbook** | 4-6 周 MVP 构建 | `strategy/runbooks/scenario-startup-mvp.md` |
| **企业功能 Runbook** | 企业功能开发 | `strategy/runbooks/scenario-enterprise-feature.md` |
| **营销活动 Runbook** | 多渠道营销活动 | `strategy/runbooks/scenario-marketing-campaign.md` |
| **事件响应 Runbook** | 生产事件处理 | `strategy/runbooks/scenario-incident-response.md` |

---

## 🔑 30 秒掌握关键概念

1. **质量关卡** —— 未通过基于证据的批准，任何阶段都不能推进
2. **开发↔QA 循环** —— 每个任务先构建再测试；通过则继续，不通过则重试（最多 3 次）
3. **交接** —— 代理之间的结构化上下文传递（永不冷启动）
4. **Reality Checker** —— 最终质量权威；默认为"需要改进"
5. **Agents Orchestrator** —— 管理整个流程的管道控制器
6. **证据优于声明** —— 截图、测试结果和数据 —— 而非断言

---

## 🎭 代理一览

```
工程                 │ 设计                  │ 营销
Frontend Developer  │ UI Designer           │ Growth Hacker
Backend Architect   │ UX Researcher         │ Content Creator
Mobile App Builder  │ UX Architect          │ Twitter Engager
AI Engineer         │ Brand Guardian        │ TikTok Strategist
DevOps Automator    │ Visual Storyteller    │ Instagram Curator
Rapid Prototyper    │ Whimsy Injector       │ Reddit Community Builder
Senior Developer    │ Image Prompt Eng.     │ App Store Optimizer
                    │                       │ Social Media Strategist
────────────────────┼───────────────────────┼──────────────────────
产品                 │ 项目管理              │ 测试
Sprint Prioritizer  │ Studio Producer       │ Evidence Collector
Trend Researcher    │ Project Shepherd      │ Reality Checker
Feedback Synthesizer│ Studio Operations     │ Test Results Analyzer
                    │ Experiment Tracker    │ Performance Benchmarker
                    │ Senior Project Mgr    │ API Tester
                    │                       │ Tool Evaluator
                    │                       │ Workflow Optimizer
────────────────────┼───────────────────────┼──────────────────────
支持                 │ 空间计算              │ 专项
Support Responder   │ XR Interface Arch.    │ Agents Orchestrator
Analytics Reporter  │ macOS Spatial/Metal   │ Analytics Reporter
Finance Tracker     │ XR Immersive Dev      │ LSP/Index Engineer
Infra Maintainer    │ XR Cockpit Spec.      │ Sales Data Extraction
Legal Compliance    │ visionOS Spatial      │ Data Consolidation
Exec Summary Gen.   │ Terminal Integration  │ Report Distribution
```

---

<div align="center">

**从选择模式开始。遵照 playbook。信任管道。**

`strategy/nexus-strategy.md` — 完整规范

</div>
