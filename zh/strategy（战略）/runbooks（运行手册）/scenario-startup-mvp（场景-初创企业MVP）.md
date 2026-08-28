# 🚀 Runbook：创业 MVP 构建

> **模式**：NEXUS-Sprint | **持续时间**：4-6 周 | **代理**：18-22

---

## 场景

你正在构建一个创业 MVP —— 一个需要快速验证产品市场契合度的新产品。速度很重要，但质量也很重要。你需要在 4-6 周内从想法到拥有真实用户的线上产品。

## 代理名册

### 核心团队（始终活跃）
| 代理 | 角色 |
|-------|------|
| Agents Orchestrator | 管道控制器 |
| Senior Project Manager | 规格到任务的转换 |
| Sprint Prioritizer | 待办列表管理 |
| UX Architect | 技术基础 |
| Frontend Developer | UI 实现 |
| Backend Architect | API 和数据库 |
| DevOps Automator | CI/CD 和部署 |
| Evidence Collector | 每个任务的 QA |
| Reality Checker | 最终质量关卡 |

### 增长团队（第 3 周+ 激活）
| 代理 | 角色 |
|-------|------|
| Growth Hacker | 获客策略 |
| Content Creator | 发布内容 |
| Social Media Strategist | 社交活动 |

### 支持团队（按需）
| 代理 | 角色 |
|-------|------|
| Brand Guardian | 品牌标识 |
| Analytics Reporter | 指标和仪表盘 |
| Rapid Prototyper | 快速验证实验 |
| AI Engineer | 如果产品包含 AI 功能 |
| Performance Benchmarker | 发布前的负载测试 |
| Infrastructure Maintainer | 生产环境设置 |

## 逐周执行

### 第 1 周：发现 + 架构（第 0 阶段 + 第 1 阶段精简版）

```
第 1-2 天：精简版发现
├── Trend Researcher → 快速竞争扫描（1 天，非完整报告）
├── UX Architect → 关键用户流程的线框图
└── Senior Project Manager → 将规格转化为任务列表

第 3-4 天：架构
├── UX Architect → CSS 设计系统 + 组件架构
├── Backend Architect → 系统架构 + 数据库模式
├── Brand Guardian → 快速品牌基础（颜色、排版、声音）
└── Sprint Prioritizer → RICE 评分的待办列表 + 冲刺计划

第 5 天：基础设置
├── DevOps Automator → CI/CD 管道 + 环境
├── Frontend Developer → 项目脚手架
├── Backend Architect → 数据库 + API 脚手架
└── 质量关卡：架构包获批
```

### 第 2-3 周：核心构建（第 2 阶段 + 第 3 阶段）

```
冲刺 1（第 2 周）：
├── Agents Orchestrator 管理开发↔QA 循环
├── Frontend Developer → 核心 UI（认证、主视图、导航）
├── Backend Architect → 核心 API（认证、CRUD、业务逻辑）
├── Evidence Collector → 每个已完成任务的 QA
├── AI Engineer → 如适用，ML 功能
└── 周末冲刺评审

冲刺 2（第 3 周）：
├── 继续剩余功能的开发↔QA 循环
├── Growth Hacker → 设计病毒传播机制 + 推荐系统
├── Content Creator → 开始创建发布内容
├── Analytics Reporter → 设置跟踪和仪表盘
└── 周末冲刺评审
```

### 第 4 周：打磨 + 加固（第 4 阶段）

```
第 1-2 天：质量冲刺
├── Evidence Collector → 完整截图套件
├── Performance Benchmarker → 负载测试
├── Frontend Developer → 修复 QA 问题
├── Backend Architect → 修复 API 问题
└── Brand Guardian → 品牌一致性审计

第 3-4 天：真实性检查
├── Reality Checker → 最终集成测试
├── Infrastructure Maintainer → 生产就绪检查
└── DevOps Automator → 生产部署准备

第 5 天：关卡决策
├── Reality Checker 判定
├── 如果需要改进：快速修复周期（2-3 天）
├── 如果就绪：推进到发布
└── Executive Summary Generator → 利益相关方简报
```

### 第 5-6 周：发布 + 增长（第 5 阶段）

```
第 5 周：发布
├── DevOps Automator → 生产部署
├── Growth Hacker → 激活获客渠道
├── Content Creator → 发布发布内容
├── Social Media Strategist → 跨平台活动
├── Analytics Reporter → 实时监控
└── Support Responder → 用户支持激活

第 6 周：优化
├── Growth Hacker → 分析和优化渠道
├── Feedback Synthesizer → 收集早期用户反馈
├── Experiment Tracker → 启动 A/B 测试
├── Analytics Reporter → 第 1 周分析
└── Sprint Prioritizer → 规划迭代冲刺
```

## 关键决策

| 决策点 | 时间 | 谁决定 |
|---------------|------|-------------|
| 概念执行/不执行 | 第 2 天结束 | Studio Producer |
| 架构批准 | 第 4 天结束 | Senior Project Manager |
| MVP 功能范围 | 冲刺规划 | Sprint Prioritizer |
| 生产就绪 | 第 4 周第 5 天 | Reality Checker |
| 发布时间 | Reality Checker 就绪后 | Studio Producer |

## 成功标准

| 指标 | 目标 |
|--------|--------|
| 从零到线上产品的时间 | ≤ 6 周 |
| 核心功能完成 | MVP 范围的 100% |
| 首批用户入驻 | 发布后 48 小时内 |
| 系统正常运行时间 | 首周 > 99% |
| 用户反馈收集 | 前 2 周 ≥ 50 条回复 |

## 常见陷阱与缓解措施

| 陷阱 | 缓解措施 |
|---------|-----------|
| 构建期间范围蔓延 | Sprint Prioritizer 强制执行 MoSCoW — "Won't" 就是不做 |
| 为规模过度工程化 | Rapid Prototyper 思维 — 先验证，后扩展 |
| 为速度跳过 QA | Evidence Collector 在每个任务上运行 — 无例外 |
| 没有监控就发布 | Infrastructure Maintainer 在第 1 周设置监控 |
| 没有反馈机制 | 分析和反馈收集内置在冲刺 1 中 |
