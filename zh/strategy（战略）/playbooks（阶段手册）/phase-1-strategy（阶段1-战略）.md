# 🏗️ 第 1 阶段 Playbook — 战略与架构

> **持续时间**：5-10 天 | **代理**：8 | **关卡守门人**：Studio Producer + Reality Checker

---

## 目标

在编写一行代码之前，定义我们要构建什么、如何构建结构以及成功的标准。每个架构决策都有文档记录。每个功能都有优先级排序。每一分钱都有据可查。

## 前置条件

- [ ] 第 0 阶段质量关卡已通过（执行决策）
- [ ] 第 0 阶段交接包已接收
- [ ] 利益相关方对项目范围已达成一致

## 代理激活序列

### 步骤 1：战略框架（第 1-3 天，并行）

#### 🎬 Studio Producer — 战略组合对齐
```
激活 Studio Producer 对 [项目] 进行战略组合对齐。

输入：第 0 阶段执行摘要 + 市场分析报告
所需交付物：
1. 战略组合计划及项目定位
2. 愿景、目标和 ROI 指标
3. 资源分配策略
4. 风险/收益评估
5. 成功标准和里程碑定义

对齐：与组织战略目标一致
格式：战略组合计划模板
时间线：3 天
```

#### 🎭 Brand Guardian — 品牌标识系统
```
激活 Brand Guardian 为 [项目] 进行品牌标识开发。

输入：第 0 阶段 UX 研究（用户画像、旅程映射）
所需交付物：
1. 品牌基础（目的、愿景、使命、价值观、个性）
2. 视觉标识系统（颜色、排版、间距以 CSS 变量形式提供）
3. 品牌声音和消息架构
4. Logo 系统规格（如果是新品牌）
5. 品牌使用指南

格式：品牌标识系统文档
时间线：3 天
```

#### 💰 Finance Tracker — 预算和资源规划
```
激活 Finance Tracker 为 [项目] 进行财务规划。

输入：Studio Producer 战略计划 + 第 0 阶段技术栈评估
所需交付物：
1. 按类别分类的综合项目预算
2. 资源成本预测（代理、基础设施、工具）
3. 带回本分析的 ROI 模型
4. 现金流时间线
5. 财务风险评估及应急储备

格式：财务计划及 ROI 预测
时间线：2 天
```

### 步骤 2：技术架构（第 3-7 天，并行，在步骤 1 输出可用后）

#### 🏛️ UX Architect — 技术架构 + UX 基础
```
激活 UX Architect 为 [项目] 进行技术架构设计。

输入：Brand Guardian 视觉标识 + 第 0 阶段 UX 研究
所需交付物：
1. CSS 设计系统（变量、标记、比例）
2. 布局框架（Grid/Flexbox 模式、响应式断点）
3. 组件架构（命名约定、层级结构）
4. 信息架构（页面流程、内容层级）
5. 主题系统（浅色/深色/系统切换）
6. 无障碍基础（WCAG 2.1 AA 基线）

需创建的文件：
- css/design-system.css
- css/layout.css
- css/components.css
- docs/ux-architecture.md

格式：开发者就绪的基础包
时间线：4 天
```

#### 🏗️ Backend Architect — 系统架构
```
激活 Backend Architect 为 [项目] 进行系统架构设计。

输入：第 0 阶段技术栈评估 + 合规需求
所需交付物：
1. 系统架构规格
   - 架构模式（微服务/单体/无服务器/混合）
   - 通信模式（REST/GraphQL/gRPC/事件驱动）
   - 数据模式（CQRS/事件溯源/CRUD）
2. 数据库模式设计及索引策略
3. API 设计规格及版本管理
4. 认证和授权架构
5. 安全架构（纵深防御）
6. 可扩展性计划（水平扩展策略）

格式：系统架构规格
时间线：4 天
```

#### 🤖 AI Engineer — ML 架构（如适用）
```
激活 AI Engineer 为 [项目] 进行 ML 系统架构设计。

输入：Backend Architect 系统架构 + 第 0 阶段数据审计
所需交付物：
1. ML 系统设计
   - 模型选择和训练策略
   - 数据管道架构
   - 推理策略（实时/批量/边缘）
2. AI 伦理和安全框架
3. 模型监控和再训练计划
4. 与主应用的集成点
5. ML 基础设施成本预测

条件：仅在项目包含 AI/ML 功能时激活
格式：ML 系统设计文档
时间线：3 天
```

#### 👔 Senior Project Manager — 规格到任务的转换
```
激活 Senior Project Manager 为 [项目] 创建任务列表。

输入：所有第 0 阶段文档 + 架构规格（在可用时）
所需交付物：
1. 综合任务列表
   - 从规格中引用确切的 EXACT 需求（不添加奢侈功能）
   - 每个任务具有明确的验收标准
   - 任务之间的依赖关系已映射
   - 工作量估算（故事点或小时）
2. 工作分解结构
3. 关键路径识别
4. 实现风险登记册

规则：
- 不要添加规格中没有的功能
- 从需求中引用确切的文本
- 对工作量估算要实事求是

格式：带验收标准的任务列表
时间线：3 天
```

### 步骤 3：优先级排序（第 7-10 天，顺序执行，在步骤 2 后）

#### 🎯 Sprint Prioritizer — 功能优先级排序
```
激活 Sprint Prioritizer 为 [项目] 进行待办列表优先级排序。

输入：
- Senior Project Manager → 任务列表
- Backend Architect → 系统架构
- UX Architect → UX 架构
- Finance Tracker → 预算框架
- Studio Producer → 战略计划

所需交付物：
1. RICE 评分的待办列表（Reach、Impact、Confidence、Effort）
2. 基于速率估算的冲刺分配
3. 带关键路径的依赖关系图
4. MoSCoW 分类（Must/Should/Could/Won't）
5. 带里程碑映射的发布计划

验证：Studio Producer 确认战略对齐
格式：优先排序的冲刺计划
时间线：2 天
```

## 质量关卡检查清单

| # | 标准 | 证据来源 | 状态 |
|---|-----------|----------------|--------|
| 1 | 架构覆盖 100% 的规格需求 | Senior PM 任务列表与架构交叉引用 | ☐ |
| 2 | 品牌系统完整（Logo、颜色、排版、声音） | Brand Guardian 交付物 | ☐ |
| 3 | 所有技术组件都有实现路径 | Backend Architect + UX Architect 规格 | ☐ |
| 4 | 预算已批准且在约束范围内 | Finance Tracker 计划 | ☐ |
| 5 | 冲刺计划基于速率且切合实际 | Sprint Prioritizer 待办列表 | ☐ |
| 6 | 安全架构已定义 | Backend Architect 安全规格 | ☐ |
| 7 | 合规要求已集成到架构中 | 法律需求已映射到技术决策 | ☐ |

## 关卡决策

**需要双重签署**：Studio Producer（战略） + Reality Checker（技术）

- **批准**：携带完整架构包推进到第 2 阶段
- **修订**：特定项目需要返工（返回到相应步骤）
- **重组**：根本性的架构问题（重新启动第 1 阶段）

## 交接给第 2 阶段

```markdown
## 第 1 阶段 → 第 2 阶段交接包

### 架构包：
1. 战略组合计划（Studio Producer）
2. 品牌标识系统（Brand Guardian）
3. 财务计划（Finance Tracker）
4. CSS 设计系统 + UX 架构（UX Architect）
5. 系统架构规格（Backend Architect）
6. ML 系统设计（AI Engineer — 如适用）
7. 综合任务列表（Senior Project Manager）
8. 优先排序的冲刺计划（Sprint Prioritizer）

### 给 DevOps Automator：
- 来自 Backend Architect 的部署架构
- 来自系统架构的环境需求
- 来自基础设施需求的监控要求

### 给 Frontend Developer：
- 来自 UX Architect 的 CSS 设计系统
- 来自 Brand Guardian 的品牌标识
- 来自 UX Architect 的组件架构
- 来自 Backend Architect 的 API 规格

### 给 Backend Architect（继续）：
- 准备好部署的数据库模式
- 准备好实现的 API 脚手架
- 已定义的身份认证系统架构
```

---

*当 Studio Producer 和 Reality Checker 双方都签署批准架构包时，第 1 阶段即告完成。*
