# Nexus Spatial：全 Agency 发现练习

> **练习类型：** 多 Agent 产品发现
> **日期：** 2026年3月5日
> **部署的 Agent：** 8 个（并行）
> **耗时：** 约10分钟（实际时间）
> **目的：** 演示从机会识别到全面规划的全 Agency 协作编排

---

## 目录

1. [机会](#1-机会)
2. [市场验证](#2-市场验证)
3. [技术架构](#3-技术架构)
4. [品牌策略](#4-品牌策略)
5. [市场推广与增长](#5-市场推广与增长)
6. [客户支持蓝图](#6-客户支持蓝图)
7. [用户研究与设计方向](#7-用户研究与设计方向)
8. [项目执行计划](#8-项目执行计划)
9. [空间界面架构](#9-空间界面架构)
10. [跨 Agent 综合](#10-跨-agent-综合)

---

## 1. 机会

### 发现过程

跨多个来源的网络研究发现了三个融合趋势：

- **AI 基础设施/编排** 是增长最快的软件类别（AI 编排市场2026年估值约135亿美元，年复合增长率22%以上）
- **空间计算**（Vision Pro、WebXR）正在成熟，但缺乏杀手级企业应用
- 所有现有 AI 工作流工具（LangSmith、n8n、Flowise、CrewAI）都是 **扁平的2D仪表板**

### 概念：Nexus Spatial

空间计算中的 AI Agent 指挥中心——一个 VisionOS + WebXR 应用，提供沉浸式3D指挥中心来编排、监控和交互 AI Agent。用户将 Agent 管道可视化为3D节点图，在空间面板中监控实时输出，在3D空间中通过拖放构建工作流，并在共享空间环境中协作。

### 为什么这个 Agency 具有独特优势

Agency 拥有深厚的空间计算专业知识（XR 开发者、VisionOS 工程师、Metal 专家、界面架构师），以及完整的工程、设计、营销和运营技术栈——对于一个同时需要空间计算精通和企业软件严谨性的产品来说，这是罕见的组合。

### 来源

- [Profitable SaaS Ideas 2026 (273K+ Reviews)](https://bigideasdb.com/profitable-saas-micro-saas-ideas-2026)
- [2026 SaaS and AI Revolution: 20 Top Trends](https://fungies.io/the-2026-saas-and-ai-revolution-20-top-trends/)
- [Top 21 Underserved Markets 2026](https://mktclarity.com/blogs/news/list-underserved-niches)
- [Fastest Growing Products 2026 - G2](https://www.g2.com/best-software-companies/fastest-growing)
- [PwC 2026 AI Business Predictions](https://www.pwc.com/us/en/tech-effect/ai-analytics/ai-predictions.html)

---

## 2. 市场验证

**Agent：** Product Trend Researcher

### 结论：有条件推进——先2D，后空间

### 市场规模

| 细分市场 | 2026年估值 | 增长率 |
|---------|-----------|--------|
| AI 编排工具 | $13.5B | 22.3% 年复合增长率 |
| 自主 AI Agent | $8.5B | 45.8% 年复合增长率，2030年达 $50.3B |
| 扩展现实 | $10.64B | 40.95% 年复合增长率 |
| 空间计算（广义） | $170-220B | 因定义不同而异 |

### 竞争格局

**AI Agent 编排（全部2D）：**

| 工具 | 优势 | 用户体验差距 |
|------|------|------------|
| LangChain/LangSmith | 基于图的编排，$39/用户/月 | 扁平仪表板；复杂图表在大规模下不可读 |
| CrewAI | 10万+开发者，执行速度快 | 命令行优先，最小化的可视化工具 |
| Microsoft Agent Framework | 企业集成 | 嵌入在 Azure 门户中，无独立 UI |
| n8n | 可视化工作流构建器，$20-50/月 | 2D画布难以处理 Agent 关系 |
| Flowise | 拖放 AI 流程 | 仅限于线性流程，无多 Agent 监控 |

**"任务控制"产品（新兴，全部2D）：**
- cmd-deck：AI 编码 Agent 的看板
- Supervity Agent Command Center：企业可观测性
- OpenClaw Command Center：Agent 车队管理
- Mission Control AI：合成工作者管理
- Mission Control HQ：基于小队的协调

**差距：** 产品要么是空间计算但不关注 AI，要么是 AI 但是扁平的2D。没有产品处于两者的交叉点。

### Vision Pro 现实检验

- 装机量：全球约100万台（销量较发布时下降95%）
- Apple 已将重心转向轻量级 AR 眼镜
- 仅约3,000个 VisionOS 专属应用
- **启示：** 不要以 VisionOS 为先导。以 Web 为先导，然后添加 WebXR，最后是原生 VisionOS。

### WebXR 作为分发解锁

- Safari 于2025年末采纳了 WebXR Device API
- 2026年 WebXR 采用率增长40%
- WebGPU 在浏览器中提供接近原生的渲染
- Android XR 支持 WebXR 和 OpenXR 标准

### 目标用户画像与定价

| 层级 | 价格 | 目标 |
|------|------|------|
| Explorer | 免费 | 开发者、独立构建者（3个 Agent，WebXR 查看器） |
| Pro | $99/用户/月 | 小型团队（25个 Agent，协作） |
| Team | $249/用户/月 | 中型市场 AI 团队（无限 Agent，分析） |
| Enterprise | 定制（$2K-10K/月） | 大型企业（SSO、RBAC、私有部署、SLA） |

### 推荐的分阶段策略

1. **第1-6月：** 构建高级2D Web仪表板，具备 Three.js 2.5D 能力。目标：50个付费团队，$60K MRR。
2. **第6-12月：** 添加可选的 WebXR 空间模式（基于浏览器）。目标：200个团队，$300K MRR。
3. **第12-18月：** 仅在空间需求得到验证时推出原生 VisionOS 应用。目标：500个团队，$1M+ MRR。

### 关键风险

| 风险 | 严重性 |
|------|--------|
| Vision Pro 装机量极小 | 高 |
| "寻找问题的空间解决方案"——3D 真的比 2D 好10倍吗？ | 高 |
| "任务控制"定位拥挤（已有5+产品） | 中 |
| 企业空间计算采用仍处于早期 | 中 |
| 跨 AI 框架的集成复杂性 | 中 |

### 来源

- [MarketsandMarkets - AI Orchestration Market](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Deloitte - AI Agent Orchestration Predictions 2026](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/ai-agent-orchestration.html)
- [Mordor Intelligence - Extended Reality Market](https://www.mordorintelligence.com/industry-reports/extended-reality-xr-market)
- [Fintool - Vision Pro Production Halted](https://fintool.com/news/apple-vision-pro-production-halt)
- [MadXR - WebXR Browser-Based Experiences 2026](https://www.madxr.io/webxr-browser-immersive-experiences-2026.html)

---

## 3. 技术架构

**Agent：** Backend Architect

### 系统概述

8个服务的架构，具有清晰的所有权边界，为水平扩展和供应商无关的 AI 集成而设计。

```
+------------------------------------------------------------------+
|                     客户端层                                       |
|  VisionOS 原生 (Swift/RealityKit)  |  WebXR (React Three Fiber)   |
+------------------------------------------------------------------+
                              |
+-----------------------------v------------------------------------+
|                      API 网关 (Kong / AWS API GW)                 |
|  限流 | JWT 验证 | WebSocket 升级 | TLS                           |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      服务层                                        |
|  Auth | Workspace | Workflow | Orchestration (Rust) |             |
|  Collaboration (Yjs CRDT) | Streaming (WS) | Plugin | Billing    |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      数据层                                        |
|  PostgreSQL 16 | Redis 7 Cluster | S3 | ClickHouse | NATS        |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                    AI 提供商层                                     |
|  OpenAI | Anthropic | Google | 本地模型 | 自定义插件               |
+------------------------------------------------------------------+
```

### 技术栈

| 组件 | 技术 | 理由 |
|------|------|------|
| 编排引擎 | **Rust** | 亚毫秒调度，零 GC 暂停，Agent 沙箱的内存安全 |
| API 服务 | TypeScript / NestJS | CRUD 密集型服务的开发者效率 |
| VisionOS 客户端 | Swift 6, SwiftUI, RealityKit | 一流的 Liquid Glass 空间计算体验 |
| WebXR 客户端 | TypeScript, React Three Fiber | 生产级 WebXR 与 React 组件模型 |
| 消息代理 | NATS JetStream | 轻量级，精确一次传递，比 Kafka 更简单 |
| 协作 | Yjs (CRDT) + WebRTC | 无冲突的并发3D图编辑 |
| 主数据库 | PostgreSQL 16 | JSONB 灵活配置，行级安全实现租户隔离 |

### 核心数据模型

14张表，涵盖：
- **身份与访问：** users、workspaces、team_memberships、api_keys
- **工作流：** workflows、workflow_versions、nodes、edges
- **执行：** executions、execution_steps、step_output_chunks
- **协作：** collaboration_sessions、session_participants
- **凭证：** provider_credentials（AES-256-GCM 加密）
- **计费：** subscriptions、usage_records
- **审计：** audit_log（仅追加）

### 节点类型注册表

```
内置节点类型：
  ai_agent          -- 使用提示词调用 AI 提供商
  prompt_template   -- 使用变量渲染模板
  conditional       -- 基于表达式路由
  transform         -- 沙箱化代码片段 (JS/Python)
  input / output    -- 工作流入口/出口点
  human_review      -- 暂停等待人工审批
  loop              -- 重复子图
  parallel_split    -- 扇出到分支
  parallel_join     -- 等待分支汇合
  webhook_trigger   -- 外部 HTTP 触发器
  delay             -- 定时暂停
```

### WebSocket 通道

通过 WSS 实现实时流式传输，具备：
- 每通道序列号保证有序
- 间隙检测与重放请求
- 落后超过1000个事件时的快照恢复
- 低性能设备的客户端侧节流

### 安全架构

| 层级 | 机制 |
|------|------|
| 用户认证 | OAuth 2.0 (GitHub, Google, Apple) + 邮箱/密码 + 可选 TOTP MFA |
| API 密钥 | SHA-256 哈希，作用域限制，可选过期时间 |
| 服务间通信 | 通过服务网格的 mTLS |
| WebSocket 认证 | 一次性票据，30秒过期 |
| 凭证存储 | 信封加密 (AES-256-GCM + AWS KMS) |
| 代码沙箱 | gVisor/Firecracker 微虚拟机 (无网络，256MB 内存，30秒 CPU) |
| 租户隔离 | PostgreSQL 行级安全 + S3 IAM 策略 + NATS 主题作用域 |

### 扩展目标

| 指标 | 第1年 | 第2年 |
|------|-------|-------|
| 并发 Agent 执行 | 5,000 | 50,000 |
| WebSocket 连接 | 10,000 | 100,000 |
| P95 API 延迟 | < 150ms | < 100ms |
| P95 WS 事件延迟 | < 80ms | < 50ms |

### MVP 阶段

1. **第1-6周：** 2D Web 编辑器，顺序执行，OpenAI + Anthropic 适配器
2. **第7-12周：** WebXR 3D 模式，并行执行，手部追踪，RBAC
3. **第13-20周：** 多用户协作，VisionOS 原生，计费
4. **第21-30周：** 企业 SSO，插件 SDK，SOC 2，扩展加固

---

## 4. 品牌策略

**Agent：** Brand Guardian

### 定位

**品类创建优于品类竞争。** Nexus Spatial 定义了一个新品类——**空间 AI 运维 (SpatialAIOps)**——而不是在拥挤的 AI 可观测性仪表板空间中争夺位置。

**定位声明：** 对于管理复杂 AI Agent 工作流的技术团队，Nexus Spatial 是沉浸式3D指挥中心，为 Agent 编排提供空间感知能力，不同于扁平的2D仪表板，因为空间计算将监控从阅读仪表板转变为置身于你的基础设施中。

### 名称验证

"Nexus Spatial" **经验证为强力名称：**
- "Nexus" 与 NEXUS 编排框架关联 (Network of EXperts, Unified in Strategy)
- "Nexus" 独立含义为"中心连接点"——非常适合指挥中心
- "Spatial" 是 Apple 和行业已规范化的行业标准描述符
- 语音韵律平衡：三个音节，然后两个音节
- **需要的行动：** 在尼斯分类第9、42、38类进行商标清查

### 品牌个性：指挥官

| 特质 | 表达 | 避免 |
|------|------|------|
| **权威** | 清晰、直接、技术精确 | 炒作、夸张、模糊的未来主义 |
| **沉稳** | 干净的设计、有节制的节奏、留白 | 为紧迫而紧迫、混乱 |
| **先锋** | 安静的自豪感，对新范式的低调暗示 | "革命性的"、"颠覆式的" |
| **精确** | 精确规格、真实指标、诚实需求 | 模糊宣称、营销流行语 |
| **亲和** | 自然的交互语言、空间隐喻 | 居高临下、设置门槛 |

### 标语（排名）

1. **"Mission Control for the Agent Era"** — 推荐使用
2. "See Your Agents in Space"
3. "Orchestrate in Three Dimensions"
4. "Where AI Operations Become Spatial"
5. "Command Center. Reimagined in Space."
6. "The Dimension Your Dashboards Are Missing"
7. "AI Agents Deserve More Than Flat Screens"

### 色彩系统

| 颜色 | 十六进制 | 用途 |
|------|---------|------|
| Deep Space Indigo | `#1B1F3B` | 基础暗色画布，背景 |
| Nexus Blue | `#4A7BF7` | 标志性品牌色，主要操作 |
| Signal Cyan | `#00D4FF` | 空间高亮，数据连接 |
| Command Green | `#00E676` | 系统健康，成功 |
| Alert Amber | `#FFB300` | 警告，需要关注 |
| Critical Red | `#FF3D71` | 错误，失败 |

使用比例：Deep Space Indigo 60%，Nexus Blue 25%，Signal Cyan 10%，语义色 5%。

### 字体

- **主要：** Inter (UI、正文、标签)
- **等宽：** JetBrains Mono (代码、日志、Agent 输出)
- **展示：** Space Grotesk (仅用于营销标题)

### Logo 概念

三个探索方向：

1. **空间 Nexus 标记** — 汇聚线在一个发光的中心节点交汇，带有微妙的透视深度
2. **维度窗口** — 带透视线的风格化视口，创造看向3D空间的效果
3. **轨道阵列** — 围绕中心点的轨道环，暗示协调运动的 Agent

### 品牌价值观

- **空间真实性** — 系统状态的诚实表示，不做表面修饰
- **运维重力** — 为生产环境构建，而非演示
- **维度慷慨** — WebXR 确保空间价值对所有人可达
- **复杂中的沉稳** — 系统越复杂，界面越冷静

### 设计令牌

```css
:root {
  --nxs-deep-space:       #1B1F3B;
  --nxs-blue:             #4A7BF7;
  --nxs-cyan:             #00D4FF;
  --nxs-green:            #00E676;
  --nxs-amber:            #FFB300;
  --nxs-red:              #FF3D71;
  --nxs-void:             #0A0E1A;
  --nxs-slate-900:        #141829;
  --nxs-slate-700:        #2A2F45;
  --nxs-slate-500:        #4A5068;
  --nxs-slate-300:        #8B92A8;
  --nxs-slate-100:        #C8CCE0;
  --nxs-cloud:            #E8EBF5;
  --nxs-white:            #F8F9FC;
  --nxs-font-primary:     'Inter', sans-serif;
  --nxs-font-mono:        'JetBrains Mono', monospace;
  --nxs-font-display:     'Space Grotesk', sans-serif;
}
```

---

## 5. 市场推广与增长

**Agent：** Growth Hacker

### 北极星指标

**周活跃管道数 (WAP)** — 过去7天内至少有一次空间交互的唯一 Agent 管道数。同时捕捉创建和参与，与价值相关，且不可作弊。

### 定价

| 层级 | 年付 | 月付 | 目标 |
|------|------|------|------|
| Explorer | 免费 | 免费 | 3个管道，WebXR 预览，社区 |
| Pro | $29/用户/月 | $39/用户/月 | 无限管道，VisionOS，30天历史 |
| Team | $59/用户/月 | $79/用户/月 | 协作，RBAC，SSO，90天历史 |
| Enterprise | 定制 (~$150+) | 定制 | 专属基础设施，SLA，私有部署选项 |

策略：14天反向试用（Pro 功能，然后降级为免费）。目标 5-8% 免费转付费转化率。

### 3阶段 GTM

**第1阶段：创始人主导销售（第1-3月）**
- 目标：使用 LangChain/CrewAI 并拥有 Vision Pro 的初创公司 AI 工程师
- 策略：私信200位知名 AI 工程师，每周 build-in-public 帖子，30秒演示片段
- 渠道：X/Twitter、LinkedIn、AI 主题 Discord 服务器、Reddit

**第2阶段：开发者社区（第4-6月）**
- Product Hunt 发布（在此阶段，而非第1阶段）
- Hacker News Show HN、Dev.to 文章、会议演讲
- 与热门 AI 框架的集成公告

**第3阶段：企业（第7-12月）**
- Apple 企业推荐管道，LinkedIn ABM 活动
- 企业案例研究，分析师简报（Gartner、Forrester）
- 首位企业 AE 招聘，SOC 2 合规

### 增长循环

1. **"惊叹因素" 演示循环** — 空间演示天然具有可分享性。一键"分享空间预览"生成 WebXR 链接或视频。目标 K = 0.3-0.5。
2. **模板市场** — 高级用户发布管道模板，可通过搜索发现，带来新注册。
3. **协作席位扩展** — 一个工程师采用，分享给队友，团队扩展到付费计划（Slack/Figma 策略）。
4. **集成驱动发现** — 在 LangChain、n8n、OpenAI/Anthropic 合作伙伴目录中的列表。

### 开源策略

**开源 (Apache 2.0)：**
- `nexus-spatial-sdk` — TypeScript/Python SDK，用于连接 Agent 框架
- `nexus-webxr-components` — React Three Fiber 3D管道组件库
- `nexus-agent-schemas` — 在3D中表示 Agent 管道的标准化架构

**保持专有：** VisionOS 原生应用、协作引擎、企业功能、托管基础设施。

### 收入目标

| 指标 | 第6月 | 第12月 |
|------|-------|--------|
| MRR | $8K-15K | $50K-80K |
| 免费账户 | 5,000 | 15,000 |
| 付费席位 | 300 | 1,200 |
| Discord 成员 | 2,000 | 5,000 |
| GitHub stars (SDK) | 500 | 2,000 |

### 首期 $50K 预算

| 类别 | 金额 | % |
|------|------|---|
| 内容制作 | $12,000 | 24% |
| 开发者关系 | $10,000 | 20% |
| 付费获客测试 | $8,000 | 16% |
| 社区与工具 | $5,000 | 10% |
| Product Hunt 与发布 | $3,000 | 6% |
| 开源维护 | $3,000 | 6% |
| 公关与推广 | $4,000 | 8% |
| 合作伙伴关系 | $2,000 | 4% |
| 储备金 | $3,000 | 6% |

### 关键合作伙伴关系

- **一级（关键）：** Anthropic、OpenAI — 一流 API 集成，合作伙伴项目列表
- **二级（采用）：** LangChain、CrewAI、n8n — 框架集成，社区交叉传播
- **三级（平台）：** Apple — Vision Pro 开发者套件、App Store 推荐、WWDC
- **四级（生态）：** GitHub、Hugging Face、Docker — 开发者平台集成

### 来源

- [AI Orchestration Market Size - MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Spatial Computing Market - Precedence Research](https://www.precedenceresearch.com/spatial-computing-market)
- [How to Price AI Products - Aakash Gupta](https://www.news.aakashg.com/p/how-to-price-ai-products)
- [Product Hunt Launch Guide 2026](https://calmops.com/indie-hackers/product-hunt-launch-guide/)

---

## 6. 客户支持蓝图

**Agent：** Support Responder

### 支持层级结构

| 属性 | Explorer (免费) | Builder (Pro) | Command (Enterprise) |
|------|----------------|---------------|---------------------|
| 首次响应 SLA | 尽力而为 (48小时) | 4小时（工作时间） | 30分钟 (P1)，2小时 (P2) |
| 解决 SLA | 5个工作日 | 24小时 (P1/P2)，72小时 (P3) | 4小时 (P1)，12小时 (P2) |
| 渠道 | 社区、知识库、AI 助手 | + 实时聊天、邮件、视频 (2次/月) | + 专属 Slack、指定 CSE、24/7 |
| 范围 | 一般问题、文档 | 技术故障排查、集成 | 完整集成、定制设计、合规 |

### 优先级定义

- **P1 紧急：** 编排宕机，数据丢失风险，安全漏洞
- **P2 高：** 主要功能降级，存在变通方案
- **P3 中：** 非阻塞问题，小故障
- **P4 低：** 功能请求，界面问题

### Nexus 指南：AI 驱动的产品内支持

突出的设计决策：支持 Agent 作为可见节点存在于**用户的空间工作区内**。它拥有用户布局、活跃 Agent 和最近错误的完整上下文。

**能力：**
- 关于功能的自然语言问答
- 实时 Agent 诊断（"为什么 Agent X 这么慢？"）
- 配置建议（"你的拓扑结构如果改为网格结构性能会更好"）
- 引导式空间故障排查演练
- 带自动上下文附加的工单创建

**自愈：**

| 场景 | 检测 | 自动解决 |
|------|------|----------|
| Agent 无限循环 | CPU/令牌峰值 | 终止并使用最后良好配置重启 |
| 渲染帧率下降 | FPS 低于阈值 | 降低视觉保真度，建议关闭面板 |
| 凭证过期 | API 401 响应 | 提示重新认证，优雅暂停 Agent |
| 通信超时 | 延迟峰值 | 通过备用路径重路由消息 |

### 入职流程

基于用户画像的自适应入职：

| AI 经验 | 空间经验 | 路径 |
|---------|---------|------|
| 低 | 低 | 完整引导之旅 (20分钟) |
| 高 | 低 | 空间聚焦 (12分钟) |
| 低 | 高 | Agent 聚焦 (12分钟) |
| 高 | 高 | 快速设置 (5分钟) |

关键第一步：在任何产品交互之前进行60秒的空间校准（手部追踪、视线、舒适度检查）。

**激活里程碑**（用户达到以下条件即为"已入职"）：
- 创建了至少一个自定义 Agent
- 在拓扑中连接了两个或更多 Agent
- 锚定了至少一个监控仪表板
- 返回了第三次会话

### 团队建设

| 阶段 | 人数 | 角色 |
|------|------|------|
| 第0-6月 | 4 | CX 负责人、2位支持工程师、技术作者 |
| 第6-12月 | 8 | + 2位支持工程师、CSE、社区经理、运维分析师 |
| 第12-24月 | 16 | + 4位工程师 (24/7)、空间专家、集成专家、知识库经理、工程经理 |

### 社区：Discord 优先

```
NEXUS SPATIAL DISCORD
  信息: #announcements, #changelog, #status
  支持: #help-getting-started, #help-agents, #help-spatial
  讨论: #general, #show-your-workspace, #feature-requests
  平台: #visionos, #webxr, #api-and-sdk
  活动: office-hours (每周语音), community-demos (每月)
  PRO 会员: #pro-lounge, #beta-testing
  企业: 每个客户私人频道
```

**冠军计划 ("Nexus Navigators")：** 5-10位初始高级用户，拥有 Navigator 徽章，与产品团队直接 Slack 沟通，免费 Pro 层级，早期功能访问，和年度峰会。

---

## 7. 用户研究与设计方向

**Agent：** UX Researcher

### 用户画像

**Maya Chen — AI 平台工程师（32岁，旧金山）**
- 管理 15-30 个活跃 Agent 工作流，使用 n8n + LangSmith
- 40% 的时间通过日志检查调试 Agent 故障
- 对空间计算持怀疑态度："这真的更快，还是只是更酷？"
- 主要需求：将平均诊断时间从45分钟降到10分钟以下

**David Okoro — 技术产品经理（38岁，伦敦）**
- 审核和批准 Agent 工作流设计，向高管汇报
- 无法有意义地参与工作流评审，因为工具需要代码级理解
- 主要需求：在不读代码的情况下理解和沟通 Agent 架构

**Dr. Amara Osei — 研究科学家（45岁，苏黎世）**
- 设计带 A/B 对比的多 Agent 研究工作流
- 同一管道有12个变体，没有好的对比方法
- 主要需求：在3D空间中并排对比变体管道

**Jordan Rivera — 创意技术专家（27岁，奥斯汀）**
- 每天使用 Vision Pro，构建 AI 驱动的艺术装置
- 希望工具感觉像乐器，而不是仪表板
- 主要需求：快速构建 Agent 工作流并获得即时的空间反馈

### 关键发现：调试是杀手级用例

运行时跟踪在工作流结构上的空间叠加解决了一个真实的、可量化的痛点，没有2D工具能很好地处理这个问题。这个工作流应该获得最多的设计和工程投资。

### 关键设计洞察

空间计算为**结构性**任务（放置、连接、重新排列节点）增加价值，但为**参数性**任务（文本输入、配置）创造摩擦。界面必须无缝融合空间和2D模式——2D面板锚定在空间位置上。

### 7条设计原则

1. **空间证明其价值** — 如果2D更清晰，就用2D。每次评审都应问："这如果是扁平的会更好吗？"
2. **先可瞥见，后可检查** — 通过颜色、大小、运动、位置在2秒内感知关键信息
3. **免手操作是基线** — 视线 + 语音覆盖所有阅读/导航操作；双手增加精度但不是必需的
4. **尊重认知重力** — 扩展2D心智模型（从左到右的流程），而不是替换它们；z轴增加分层
5. **渐进式空间复杂性** — 新用户从近乎2D开始；空间能力随信心增长而展现
6. **物理隐喻，数字能力** — 节点被"拿起"（物理）但也可以复制和版本化（数字）
7. **沉默是功能** — 健康的系统感觉平静；颜色和运动信号偏离正常

### 导航范式：4级语义缩放

| 层级 | 看到的内容 |
|------|----------|
| 车队视图 | 所有工作流作为抽象形状，按状态颜色编码 |
| 工作流视图 | 带标签和连接的节点图 |
| 节点视图 | 展开的配置，最近的输入/输出，状态指标 |
| 跟踪视图 | 完整的执行跟踪和数据检查 |

### 竞品 UX 总结

| 能力 | n8n | Flowise | LangSmith | Langflow | Nexus Spatial 目标 |
|------|-----|---------|-----------|----------|---------------------|
| 可视化工作流构建 | A | B+ | N/A | A | A+ (空间) |
| 调试/跟踪 | C+ | C | A | B | A+ (空间叠加) |
| 监控 | B | C | A | B | A (空间车队) |
| 协作 | D | D | C | D | A (空间共同存在) |
| 大型工作流可扩展性 | C | C | B | C | A (3D空间) |

### 无障碍要求

- 每个交互可通过至少两种模态完成
- 不单独通过颜色传达信息
- 高对比度模式、减少运动模式、深度扁平化模式
- 屏幕阅读器与空间元素描述兼容
- 每20-30分钟的会话长度警告
- 所有核心任务可坐着、单手、在30度运动锥内完成

### 研究计划（16周）

| 阶段 | 周数 | 研究 |
|------|------|------|
| 基础 | 1-4 | 心智模型访谈 (15-20位参与者)，竞品任务分析 |
| 概念验证 | 5-8 | 绿野仙踪空间原型测试，3D卡片分类用于信息架构 |
| 可用性测试 | 9-14 | 首次使用体验 (20位用户)，4周纵向日记研究，配对协作测试 |
| 无障碍审计 | 12-16 | 专家启发式评估，与残障用户的测试 |

---

## 8. 项目执行计划

**Agent：** Project Shepherd

### 时间线：35周（2026年3月9日 - 11月6日）

| 阶段 | 周数 | 时长 | 目标 |
|------|------|------|------|
| 发现与研究 | W1-3 | 3周 | 验证可行性，定义范围 |
| 基础 | W4-9 | 6周 | 核心基础设施，两个平台外壳，设计系统 |
| MVP 构建 | W10-19 | 10周 | 单用户 Agent 指挥中心与编排 |
| Beta | W20-27 | 8周 | 协作、打磨、加固，50-100个 Beta 用户 |
| 发布 | W28-31 | 4周 | App Store + Web 发布，营销推广 |
| 扩展 | W32-35+ | 持续 | 插件市场、高级功能、增长 |

### 关键里程碑：第12周（5月29日）

**首次端到端工作流执行。** 用户在3D中创建并运行一个3节点的 Agent 工作流。这是产品证明其核心价值主张的时刻。如果这个节点延迟，所有下游都会受到影响。

### 前6个 Sprint（65个工单）

**Sprint 1（3月9-20日）：** VisionOS SDK 审计，WebXR 兼容性矩阵，编排引擎可行性研究，利益相关者访谈，两个平台的一次性原型。

**Sprint 2（3月23日-4月3日）：** 架构决策记录，MVP 范围用 MoSCoW 锁定，PRD v1.0，空间 UI 模式研究，交互模型定义，设计系统启动。

**Sprint 3（4月6-17日）：** Monorepo 设置，认证服务 (OAuth2)，数据库 schema，API 网关，VisionOS Xcode 项目初始化，WebXR 项目初始化，CI/CD 管道。

**Sprint 4（4月20日-5月1日）：** WebSocket 服务器 + 客户端 SDK，空间窗口管理，3D组件库，手部追踪输入层，团队 CRUD，集成测试。

**Sprint 5（5月4-15日）：** 编排引擎核心 (Rust)，Agent 状态机，节点图渲染器（两个平台），插件接口 v0，OpenAI 提供商插件。

**Sprint 6（5月18-29日）：** 工作流持久化 + 版本控制，DAG 执行，实时执行可视化，Anthropic 提供商插件，视线跟踪集成，空间音频。

### 团队分配

5个小队跨阶段运作：

| 小队 | 核心成员 | 活跃阶段 |
|------|----------|----------|
| 核心架构 | Backend Architect, XR Interface Architect, Senior Dev, VisionOS Engineer | 发现到 MVP |
| 空间体验 | XR Immersive Dev, XR Cockpit Specialist, Metal Engineer, UX Architect, UI Designer | 基础到 Beta |
| 编排 | AI Engineer, Backend Architect, Senior Dev, API Tester | MVP 到 Beta |
| 平台交付 | Frontend Dev, Mobile App Builder, VisionOS Engineer, DevOps | MVP 到发布 |
| 发布 | Growth Hacker, Content Creator, App Store Optimizer, Visual Storyteller, Brand Guardian | Beta 到扩展 |

### 前5大风险

| 风险 | 概率 | 影响 | 缓解措施 |
|------|------|------|----------|
| Apple 拒绝 VisionOS 应用 | 中 | 关键 | 第4周联系 Apple 开发者关系，第20周前预审 |
| WebXR 浏览器碎片化 | 高 | 高 | 第1周制定浏览器支持矩阵，自动化跨浏览器测试 |
| 多用户同步冲突 | 中 | 高 | 从一开始就使用基于 CRDT 的同步 (Yjs)，在基础阶段原型化 |
| 编排无法扩展 | 中 | 关键 | 从第一天起水平扩展，第22周前进行10倍负载测试 |
| RealityKit 100+节点性能 | 中 | 高 | 早期性能分析，实现 LOD 剔除，实例化渲染 |

### 预算：$121,500 — $155,500（非人员）

| 类别 | 估算成本 |
|------|----------|
| 云基础设施（35周） | $35,000 - $45,000 |
| 硬件（3台 Vision Pro，2台 Quest 3，Mac Studio） | $17,500 |
| 许可证和服务 | $15,000 - $20,000 |
| 外部服务（法律、安全、公关） | $30,000 - $45,000 |
| AI API 成本（开发/测试） | $8,000 |
| 应急费用 (15%) | $16,000 - $20,000 |

---

## 9. 空间界面架构

**Agent：** XR Interface Architect

### 指挥剧场

工作区围绕用户组织为弧形剧场：

```
                        概览天篷
                     (管道拓扑)
                    ~~~~~~~~~~~~~~~~~~~~~~~~
                   /                        \
                  /     焦点弧 (120度)      \
                 /    主要节点图工作         \
                /________________________________\
               |                                  |
    左侧       |        用户位置               |       右侧
    工具       |        (原点 0,0,0)            |       工具
    栏         |                                  |       栏
               |__________________________________|
                \                                /
                 \      层架（低于视线）       /
                  \   Agent 状态，快速工具   /
                   \_________________________ /
```

- **焦点弧**（120度，1.2-2.0m）：主要节点图工作区
- **概览天篷**（上方，2.5-4.0m）：微型管道拓扑 + 健康热图
- **工具栏**（左/右侧翼）：Agent 库、监控、日志
- **层架**（低于视线，0.8-1.0m）：运行/停止、撤销/重做、快速工具

### 三层深度系统

| 层 | 深度 | 内容 | 不透明度 |
|---|------|------|--------|
| 前景 | 0.8 - 1.2m | 活动面板、检查器、模态框 | 100% |
| 中景 | 1.2 - 2.5m | 节点图、连接、工作区 | 100% |
| 背景 | 2.5 - 5.0m | 概览地图、环境状态 | 40-70% |

### 3D 节点图

**数据向用户流动。** 节点按执行顺序沿 z 轴排列：

```
用户 (此处)
  z=0.0m   [输出节点]     -- 结果
  z=0.3m   [转换节点]   -- 处理器
  z=0.6m   [Agent 节点]    -- LLM 调用
  z=0.9m   [检索节点]   -- RAG, API
  z=1.2m   [输入节点]     -- 触发器
```

并行分支水平展开 (x轴)。条件分支垂直展开 (y轴)。

**节点表示（3个 LOD）：**
- **LOD-0**（静止，>1.5m）：12x8cm 磨砂玻璃矩形，带类型图标、名称、状态光晕
- **LOD-1**（悬停，400ms 注视）：扩展为 14x10cm，显示端口、上次运行信息
- **LOD-2**（选中）：滑到前景，扩展为 30x40cm 详情面板，带实时配置编辑

**连接作为发光管道：**
- 静止时4mm直径，携带数据时8mm
- 按数据类型颜色编码 (白色=文本, 青色=结构化, 品红=图像, 琥珀=音频, 绿色=工具调用)
- 动画粒子显示流动方向和速度
- 当 >3 条在同一层之间并行时自动捆绑

### 7种 Agent 状态

| 状态 | 边缘光晕 | 内部 | 声音 | 粒子 |
|------|----------|------|------|------|
| 空闲 | 稳定绿色，低 | 静态磨砂玻璃 | 无 | 无 |
| 排队 | 脉冲琥珀色，1Hz | 微弱旋转 | 无 | 输入端缓慢漂移 |
| 运行 | 稳定蓝色，中 | 动画微光 | 柔和空间哆音 | 连接上快速流动 |
| 流式传输 | 蓝色 + 输出流 | 微光 + 文本片段 | 哆音 | 文本片段向前流动 |
| 完成 | 闪烁白色，然后绿色 | 静态 | 完成提示音 | 无 |
| 错误 | 脉冲红色，2Hz | 红色色调 | 警报音 (一次) | 无 |
| 暂停 | 稳定琥珀色 | 冻结帧 + 暂停图标 | 无 | 原位冻结 |

### 交互模型

| 操作 | VisionOS | WebXR 控制器 | 语音 |
|------|----------|---------------|------|
| 选择节点 | 注视 + 捏合 | 指向光线 + 触发器 | "选择 [名称]" |
| 移动节点 | 捏合 + 拖拽 | 抓取 + 移动 | — |
| 连接端口 | 捏合端口 + 拖拽 | 触发端口 + 拖拽 | "连接 [A] 到 [B]" |
| 平移工作区 | 双手拖拽 | 摇杆 | "向左/右平移" |
| 缩放 | 双手展开/捏合 | 摇杆推/拉 | "放大/缩小" |
| 检查节点 | 捏合 + 向自己拉 | 双击触发器 | "检查 [名称]" |
| 运行管道 | 点击层架按钮 | 触发按钮 | "运行管道" |
| 撤销 | 双指双击 | B 按钮 | "撤销" |

### 协作存在

每个协作者由以下元素代表：
- **头部代理：** 半透明球体，带个人资料图像，随头部方向旋转
- **手部代理：** 显示捏合/抓取状态的幽影手部模型
- **视线锥：** 微妙的10度锥形，显示他们正在看的位置
- **名称标签：** 公告板渲染，显示当前操作 ("正在编辑节点 X")

**冲突解决：** 第一个编辑者获得写锁；第二个看到"被 [名称] 锁定"，可选择请求访问或复制节点。

### 自适应布局

| 环境 | 节点比例 | 最大 LOD-2 节点 | 图 Z 展开 |
|------|----------|-----------------|-----------|
| VisionOS 窗口 | 4x3cm | 5 | 0.05m/层 |
| VisionOS 沉浸式 | 12x8cm | 15 | 0.3m/层 |
| WebXR 桌面 | 120x80px | 8 (叠加层) | 透视投影 |
| WebXR 沉浸式 | 12x8cm | 12 | 0.3m/层 |

### 过渡编排

所有过渡服务于寻路。主要过渡最大600ms，次要200ms，选择0ms。

| 过渡 | 时长 | 关键动作 |
|------|------|----------|
| 概览到焦点 | 600ms | 相机漂移到目标，其他区域淡化到30% |
| 焦点到详情 | 500ms | 节点向前滑动，展开，连接高亮 |
| 详情到概览 | 600ms | 面板折叠，节点回退，完整拓扑可见 |
| 区域切换 | 500ms | 当前向侧面滑出，新的滑入 |
| 窗口到沉浸式 | 1000ms | 边框溶解，节点扩展到完整空间位置 |

### 舒适度措施

- 没有用户操作时不发起相机移动
- 稳定地平线（水平面不倾斜）
- 主要交互在 0.8-2.5m 内，视线上下15度
- 45分钟后休息提示（环境光照变化，非模态框）
- 快速移动时的周边暗角
- 所有常用控件可在手臂自然下垂时访问 (手腕/手指操作)

---

## 10. 跨 Agent 综合

### 8个 Agent 的共识点

1. **先2D，后空间。** 每个 Agent 都独立得出了这个结论。先构建优秀的 Web 仪表板，然后逐步添加空间能力。

2. **调试是杀手级用例。** Product Researcher、UX Researcher 和 XR Interface Architect 都汇聚于此：运行时跟踪在工作流结构上的空间叠加是3D真正超过2D的地方。

3. **WebXR 优于 VisionOS 作为初始覆盖。** Vision Pro 的约100万装机量无法支撑一个业务。浏览器中的 WebXR 是分发解锁。

4. **"作战室" 协作场景。** 多个 Agent 强调了协作事件响应作为最强空间价值主张——团队进入共享3D空间一起调试故障管道。

5. **渐进式披露至关重要。** UX Research、Spatial UI 和 Support 都强调空间复杂性必须逐步展现，绝不能让首次用户感到不知所措。

6. **语音作为高级用户加速器。** UX Researcher 和 XR Interface Architect 都将语音命令识别为"空间计算的命令行"——对无障碍和专家效率至关重要。

### 需要解决的关键张力

| 张力 | 立场 A | 立场 B | 需要的解决方案 |
|------|---------|---------|---------------|
| **定价** | Growth Hacker: $29-59/用户/月 | Trend Researcher: $99-249/用户/月 | Beta 中 A/B 测试 |
| **VisionOS 优先级** | 架构：第3阶段（第13周+） | 空间 UI：完整规格已就绪 | 先构建 WebXR，验证后再做 VisionOS |
| **编排语言** | 架构：Rust | 项目计划：未指定 | Rust 对性能关键的 DAG 执行是正确的 |
| **MVP 范围** | 架构：第1阶段仅2D | 品牌：以空间为先导 | 2D 为先，但确保每个演示中都有空间 |
| **社区平台** | 支持：Discord 优先 | 营销：Discord + 开源 | 两者都——Discord 用于社区，GitHub 用于开发者参与 |

### 这个练习展示了什么

这个发现文档由8个并行运行的专业化 Agent 产出，每个都为共同目标带来了深厚的领域专业知识。这些 Agent 独立得出了一致的结论，同时 surfaced 了任何单一通才难以产出的领域特定洞察：

- **Product Trend Researcher** 发现了令人清醒的 Vision Pro 销售数据，重新定义了整个策略
- **Backend Architect** 设计了 Rust 编排引擎，这是任何以营销为中心的团队都不会考虑的
- **Brand Guardian** 创造了一个品类 ("SpatialAIOps")，而不是在现有品类中竞争
- **UX Researcher** 发现空间计算为参数性任务创造摩擦——这是一个反直觉的发现
- **XR Interface Architect** 设计了"数据向你流动"的拓扑，映射到自然空间认知
- **Project Shepherd** 识别了三个可能打乱整个时间线的关键瓶颈角色
- **Growth Hacker** 设计了针对空间计算固有可分享性的病毒循环
- **Support Responder** 将产品自身的 AI 能力转化为支持差异化优势

结果是一个全面的、跨职能的产品计划，可以作为实际开发的基础——由一个 AI Agent 组成的 Agency 在单次会议中协同工作产出。
