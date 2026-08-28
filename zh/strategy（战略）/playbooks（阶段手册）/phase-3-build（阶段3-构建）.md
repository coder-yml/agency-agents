# 🔨 第 3 阶段 Playbook — 构建与迭代

> **持续时间**：2-12 周（视范围而定） | **代理**：15-30+ | **关卡守门人**：Agents Orchestrator

---

## 目标

通过持续的开发↔QA 循环实现所有功能。每个任务在开始下一个之前都经过验证。这是大部分工作发生的地方 —— 也是 NEXUS 编排提供最大价值的地方。

## 前置条件

- [ ] 第 2 阶段质量关卡已通过（基础已验证）
- [ ] Sprint Prioritizer 待办列表可用，含 RICE 评分
- [ ] CI/CD 管道可操作
- [ ] 设计系统和组件库就绪
- [ ] 带认证系统的 API 脚手架就绪

## 开发↔QA 循环 — 核心机制

Agents Orchestrator 管理每个任务通过此循环：

```
对冲刺待办列表中的每个任务（按 RICE 评分排序）：

  1. 将任务分配给适当的开发者代理（参见分配矩阵）
  2. 开发者实现任务
  3. Evidence Collector 测试任务
     - 视觉截图（桌面、平板、移动）
     - 对照验收标准的功能验证
     - 品牌一致性检查
  4. 如果判定 == 通过：
       标记任务完成
       移至下一个任务
     否则如果判定 == 不通过 且 尝试次数 < 3：
       将 QA 反馈发送给开发者
       开发者修复具体问题
       返回步骤 3
     否则如果尝试次数 >= 3：
       升级至 Agents Orchestrator
       Orchestrator 决定：重新分配、分解、推迟或接受
  5. 更新管道状态报告
```

## 代理分配矩阵

### 主要开发者分配

| 任务类别 | 主要代理 | 备份代理 | QA 代理 |
|--------------|--------------|-------------|----------|
| **React/Vue/Angular UI** | Frontend Developer | Rapid Prototyper | Evidence Collector |
| **REST/GraphQL API** | Backend Architect | Senior Developer | API Tester |
| **数据库操作** | Backend Architect | — | API Tester |
| **移动端 (iOS/Android)** | Mobile App Builder | — | Evidence Collector |
| **ML 模型/管道** | AI Engineer | — | Test Results Analyzer |
| **CI/CD/基础设施** | DevOps Automator | Infrastructure Maintainer | Performance Benchmarker |
| **高级/复杂功能** | Senior Developer | Backend Architect | Evidence Collector |
| **快速原型/POC** | Rapid Prototyper | Frontend Developer | Evidence Collector |
| **WebXR/沉浸式** | XR Immersive Developer | — | Evidence Collector |
| **visionOS** | visionOS Spatial Engineer | macOS Spatial/Metal Engineer | Evidence Collector |
| **驾驶舱控制** | XR Cockpit Interaction Specialist | XR Interface Architect | Evidence Collector |
| **CLI/终端工具** | Terminal Integration Specialist | — | API Tester |
| **代码智能** | LSP/Index Engineer | — | Test Results Analyzer |
| **性能优化** | Performance Benchmarker | Infrastructure Maintainer | Performance Benchmarker |

### 专家支持（按需激活）

| 专家 | 何时激活 | 触发器 |
|-----------|-----------------|---------|
| UI Designer | 组件需要视觉优化 | 开发者请求设计指导 |
| Whimsy Injector | 功能需要趣味性/个性 | UX 评审识别出机会 |
| Visual Storyteller | 需要视觉叙事内容 | 内容需要视觉素材 |
| Brand Guardian | 品牌一致性疑虑 | QA 发现品牌偏差 |
| XR Interface Architect | 需要空间交互设计 | XR 功能需要 UX 指导 |
| Analytics Reporter | 需要深度数据分析 | 功能需要分析集成 |

## 并行构建轨道

对于 NEXUS-Full 部署，四个轨道同时运行：

### 轨道 A：核心产品开发
```
管理者：Agents Orchestrator（开发↔QA 循环）
代理：Frontend Developer、Backend Architect、AI Engineer、
       Mobile App Builder、Senior Developer
QA：Evidence Collector、API Tester、Test Results Analyzer

冲刺节奏：2 周冲刺
每日：任务实现 + QA 验证
冲刺结束：冲刺评审 + 回顾
```

### 轨道 B：增长与营销准备
```
管理者：Project Shepherd
代理：Growth Hacker、Content Creator、Social Media Strategist、
       App Store Optimizer

冲刺节奏：与轨道 A 的里程碑对齐
活动：
- Growth Hacker → 设计病毒传播循环和推荐机制
- Content Creator → 构建发布内容管道
- Social Media Strategist → 规划跨平台营销活动
- App Store Optimizer → 准备应用商店列表（如为移动端）
```

### 轨道 C：质量与运营
```
管理者：Agents Orchestrator
代理：Evidence Collector、API Tester、Performance Benchmarker、
       Workflow Optimizer、Experiment Tracker

持续活动：
- Evidence Collector → 每个任务的截图 QA
- API Tester → 每个 API 任务的端点验证
- Performance Benchmarker → 定期负载测试
- Workflow Optimizer → 流程改进识别
- Experiment Tracker → 已验证功能的 A/B 测试设置
```

### 轨道 D：品牌与体验打磨
```
管理者：Brand Guardian
代理：UI Designer、Brand Guardian、Visual Storyteller、
       Whimsy Injector

触发式活动：
- UI Designer → 当 QA 识别出视觉问题时进行组件优化
- Brand Guardian → 定期品牌一致性审计
- Visual Storyteller → 随功能完成创建视觉叙事素材
- Whimsy Injector → 微交互和趣味时刻
```

## 冲刺执行模板

### 冲刺规划（第 1 天）

```
Sprint Prioritizer 激活：
1. 审查待办列表及更新的 RICE 评分
2. 根据团队速率选择冲刺任务
3. 将任务分配给开发者代理
4. 识别依赖关系和排序
5. 设置冲刺目标和成功标准

输出：含任务分配的冲刺计划
```

### 每日执行（第 2 天到第 N-1 天）

```
Agents Orchestrator 管理：
1. 当前任务状态检查
2. 开发↔QA 循环执行
3. 阻塞识别和解决
4. 进度跟踪和报告

状态报告格式：
- 今日已完成任务：[列表]
- QA 中的任务：[列表]
- 开发中的任务：[列表]
- 阻塞的任务：[列表及原因]
- QA 通过率：[X/Y]
```

### 冲刺评审（第 N 天）

```
Project Shepherd 主持：
1. 演示已完成的功能
2. 审查每个任务的 QA 证据
3. 收集利益相关方反馈
4. 根据学习更新待办列表

参与者：所有活动代理 + 利益相关方
输出：冲刺评审摘要
```

### 冲刺回顾

```
Workflow Optimizer 主持：
1. 哪些做得好？
2. 哪些可以改进？
3. 下个冲刺我们将改变什么？
4. 流程效率指标

输出：回顾行动项
```

## Orchestrator 决策逻辑

### 任务失败处理

```
当任务 QA 不通过时：
  如果尝试次数 == 1：
    → 将具体 QA 反馈发送给开发者
    → 开发者仅修复所识别的问题
    → 重新提交 QA
    
  如果尝试次数 == 2：
    → 发送累计的 QA 反馈
    → 考虑：开发者代理是否合适？
    → 开发者根据额外上下文进行修复
    → 重新提交 QA
    
  如果尝试次数 == 3：
    → 升级
    → 选项：
      a) 重新分配给不同的开发者代理
      b) 将任务分解为较小的子任务
      c) 修改方案/架构
      d) 接受并记录已知限制
      e) 推迟到未来的冲刺
    → 记录决策和理由
```

### 并行任务管理

```
当多个任务没有依赖关系时：
  → 同时分配给不同的开发者代理
  → 每个代理运行独立的开发↔QA 循环
  → Orchestrator 并发跟踪所有循环
  → 按依赖顺序合并已完成的任务

当任务有依赖关系时：
  → 等待依赖任务通过 QA
  → 然后分配依赖任务
  → 在交接中包含依赖上下文
```

## 质量关卡检查清单

| # | 标准 | 证据来源 | 状态 |
|---|-----------|----------------|--------|
| 1 | 所有冲刺任务通过 QA（100% 完成） | 每个任务的 Evidence Collector 截图 | ☐ |
| 2 | 所有 API 端点已验证 | API Tester 回归报告 | ☐ |
| 3 | 性能基线已满足（P95 < 200ms） | Performance Benchmarker 报告 | ☐ |
| 4 | 品牌一致性已验证（95%+ 一致性） | Brand Guardian 审计 | ☐ |
| 5 | 无严重 bug（零个 P0/P1 开放问题） | Test Results Analyzer 摘要 | ☐ |
| 6 | 所有验收标准已满足 | 逐任务验证 | ☐ |
| 7 | 所有 PR 代码审查已完成 | Git 历史证据 | ☐ |

## 关卡决策

**关卡守门人**：Agents Orchestrator

- **通过**：功能完整的应用 → 激活第 4 阶段
- **继续**：需要更多冲刺 → 继续第 3 阶段
- **升级**：系统性问题 → Studio Producer 干预

## 交接给第 4 阶段

```markdown
## 第 3 阶段 → 第 4 阶段交接包

### 给 Reality Checker：
- 完整的应用（所有功能已实现）
- 所有开发↔QA 循环的 QA 证据
- API Tester 回归结果
- Performance Benchmarker 基线数据
- Brand Guardian 一致性审计
- 已知问题列表（如有任何已接受的限制）

### 给 Legal Compliance Checker：
- 数据处理实现细节
- 隐私政策实现
- 同意管理实现
- 已实施的安全措施

### 给 Performance Benchmarker：
- 用于负载测试的应用 URL
- 预期流量模式
- 来自架构的性能预算

### 给 Infrastructure Maintainer：
- 生产环境需求
- 扩缩配置需求
- 监控告警阈值
```

---

*当所有冲刺任务通过 QA、所有 API 端点已验证、性能基线已满足且无严重 bug 存在时，第 3 阶段即告完成。*
