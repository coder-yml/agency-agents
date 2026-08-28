# 🎭 The Agency：随时待命、准备重塑你工作流的 AI 专家

> **触手可及的完整 AI 代理机构** - 从前端魔法师到 Reddit 社区忍者，从奇思妙想注入者到现实校验员。每个 agent 都是拥有个性、流程和经过验证交付物的专业专家。

[![GitHub stars](https://img.shields.io/github/stars/msitarzewski/agency-agents?style=social)](https://github.com/msitarzewski/agency-agents)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink?logo=github)](https://github.com/sponsors/msitarzewski)
[![Download the app](https://img.shields.io/github/v/release/msitarzewski/agency-agents-app?label=Download%20app&color=2563eb)](https://github.com/msitarzewski/agency-agents-app/releases/latest)

> ### 🆕 现在有应用了
>
> **[Agency Agents](https://agencyagents.app)** 是一个适用于 **macOS、Linux 和 Windows** 的原生应用，可浏览完整 roster，并一键将其安装到 Claude Code、Cursor、Codex、Gemini、Osaurus 等工具中——无需克隆、无需脚本，而且会自动更新。
>
> **→ [下载最新版本](https://github.com/msitarzewski/agency-agents-app/releases/latest) · [agencyagents.app](https://agencyagents.app)**

---

## 🚀 这是什么？

诞生于一个 Reddit 讨论串和数月的迭代，**The Agency** 是一个不断扩展、经过精心打造的 AI agent 个性集合。每个 agent 都具备：

- **🎯 专业聚焦**：在各自领域具备深厚专长（而不是通用提示模板）
- **🧠 个性驱动**：独特的声音、沟通风格和方法
- **📋 以交付物为中心**：真实的代码、流程和可衡量结果
- **✅ 可用于生产**：经过实战检验的工作流和成功指标

**可以把它理解为**：组建你的梦之队，只不过这些是永不睡觉、从不抱怨、并且总能交付的 AI 专家。

---

## ⚡ 快速开始

### 选项 1：安装应用（推荐）

最快的入口——无需克隆，无需终端。[**Agency Agents**](https://agencyagents.app) 是一款原生桌面应用（macOS · Linux · Windows），可浏览整个 roster，并为你将 agent 安装到 Claude Code、Cursor、Codex、Gemini CLI、OpenCode、Qwen 和 Osaurus 中，然后保持更新。

**[⬇ 下载最新版本](https://github.com/msitarzewski/agency-agents-app/releases/latest)** —— 或在 Mac 上使用：

```bash
brew install --cask msitarzewski/agency-agents/agency-agents
```

偏好命令行？下面基于脚本的选项会安装相同的 agents。

### 选项 2：与 Claude Code 搭配使用

```bash
# 将所有 agents 安装到你的 Claude Code 目录
./scripts/install.sh --tool claude-code

# 或者如果你只想要一个分部，也可以手动复制某个分类
cp engineering/*.md ~/.claude/agents/

# 然后在 Claude Code 会话中激活任意 agent：
# "Hey Claude, activate Frontend Developer mode and help me build a React component"
```

### 选项 3：作为参考使用

每个 agent 文件都包含：
- 身份与个性特征
- 核心使命与工作流
- 带代码示例的技术交付物
- 成功指标与沟通风格

浏览下面的 agents，并复制/改造你需要的那些！

### 选项 4：与其他工具配合使用（GitHub Copilot、Antigravity、Gemini CLI、OpenCode、OpenClaw、Cursor、Aider、Windsurf、Kimi Code、Codex、Osaurus、Hermes、Mistral Vibe）

```bash
# 步骤 1 -- 为所有支持的工具生成集成文件
./scripts/convert.sh

# 步骤 2 -- 交互式安装（自动检测你已安装的内容）
./scripts/install.sh

# 或者直接针对某个特定工具
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool gemini-cli
./scripts/install.sh --tool opencode
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool cursor
./scripts/install.sh --tool aider
./scripts/install.sh --tool windsurf
./scripts/install.sh --tool kimi
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes
./scripts/install.sh --tool vibe
```

**只安装你需要的团队**（不是每个人都想要所有分部）：

```bash
./scripts/install.sh                                    # 交互式向导：选择工具 + 团队
./scripts/install.sh --tool claude-code --division engineering,security
./scripts/install.sh --tool cursor --agent frontend-developer,ui-designer
./scripts/install.sh --list teams                       # 查看所有 team + agent 数量
./scripts/install.sh --tool opencode --division engineering --dry-run
```

> **OpenCode 说明：** OpenCode 的运行时当前只会注册大约 119 个 agent，并会静默丢弃其余部分（[上游 bug](https://github.com/anomalyco/opencode/issues/27988)）。使用 `--division` 安装子集可以让你保持在该限制之内。若你选择的内容会超过上限，安装器会发出警告。

有关完整细节，请参见下方的 [多工具集成](#-多工具集成) 部分。

---

## 🎨 The Agency roster

### 💻 工程分部

一行一行 commit，构建未来。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎨 [Frontend Developer](engineering（工程）/engineering-frontend-developer（前端开发者）.md) | React/Vue/Angular、UI 实现、性能 | 现代 Web 应用、像素级精确 UI、Core Web Vitals 优化 |
| 🏗️ [Backend Architect](engineering（工程）/engineering-backend-architect（后端架构师）.md) | API 设计、数据库架构、可扩展性 | 服务端系统、微服务、云基础设施 |
| 📱 [Mobile App Builder](engineering（工程）/engineering-mobile-app-builder（移动应用构建师）.md) | iOS/Android、React Native、Flutter | 原生与跨平台移动应用 |
| 🤖 [AI Engineer](engineering（工程）/engineering-ai-engineer（AI%20工程师）.md) | ML 模型、部署、AI 集成 | 机器学习功能、数据管道、AI 驱动应用 |
| 🚀 [DevOps Automator](engineering（工程）/engineering-devops-automator（DevOps%20自动化师）.md) | CI/CD、基础设施自动化、云运维 | 流水线开发、部署自动化、监控 |
| 🌐 [Network Engineer](engineering（工程）/engineering-network-engineer（网络工程师）.md) | Cisco IOS/IOS-XE、Juniper Junos、Palo Alto PAN-OS | 路由器/交换机/防火墙配置、BGP/OSPF、ACL、基于 show 输出的故障排查 |
| ⚡ [Rapid Prototyper](engineering（工程）/engineering-rapid-prototyper（快速原型师）.md) | 快速 POC 开发、MVP | 快速概念验证、黑客松项目、快速迭代 |
| 💎 [Senior Developer](engineering（工程）/engineering-senior-developer（高级开发者）.md) | Laravel/Livewire、高级模式 | 复杂实现、架构决策 |
| 🔧 [Filament Optimization Specialist](engineering（工程）/engineering-filament-optimization-specialist（Filament%20优化专家）.md) | Filament PHP 管理后台 UX、结构化表单重构、资源优化 | 重构 Filament resources/forms/tables，以获得更快、更清爽的后台工作流 |
| ⚡ [Autonomous Optimization Architect](engineering（工程）/engineering-autonomous-optimization-architect（自主优化架构师）.md) | LLM 路由、成本优化、影子测试 | 需要智能 API 选择与成本护栏的自治系统 |
| 🔩 [Embedded Firmware Engineer](engineering（工程）/engineering-embedded-firmware-engineer（嵌入式固件工程师）.md) | 裸机、RTOS、ESP32/STM32/Nordic 固件 | 生产级嵌入式系统与 IoT 设备 |
| 🚨 [Incident Response Commander](engineering（工程）/engineering-incident-response-commander（事件响应指挥官）.md) | 事故管理、事后复盘、值班 | 管理生产事故并构建事故响应准备度 |
| ⛓️ [Solidity Smart Contract Engineer](engineering（工程）/engineering-solidity-smart-contract-engineer（Solidity%20智能合约工程师）.md) | EVM 合约、gas 优化、DeFi | 安全、gas 优化的智能合约与 DeFi 协议 |
| 🧭 [Codebase Onboarding Engineer](engineering（工程）/engineering-codebase-onboarding-engineer（代码库入门工程师）.md) | 快速开发者上手、只读代码库探索、事实性解释 | 通过阅读代码、追踪代码路径并陈述结构与行为事实，帮助新开发者快速理解陌生仓库 |
| 📚 [Technical Writer](engineering（工程）/engineering-technical-writer（技术文档工程师）.md) | 开发者文档、API 参考、教程 | 清晰、准确的技术文档 |
| 💬 [WeChat Mini Program Developer](engineering（工程）/engineering-wechat-mini-program-developer（微信小程序开发者）.md) | 微信生态、小程序、支付集成 | 为微信生态构建高性能应用 |
| 👁️ [Code Reviewer](engineering（工程）/engineering-code-reviewer（代码审查员）.md) | 建设性的代码审查、安全性、可维护性 | PR 审查、代码质量门槛、通过审查进行指导 |
| 🗄️ [Database Optimizer](engineering（工程）/engineering-database-optimizer（数据库优化师）.md) | 模式设计、查询优化、索引策略 | PostgreSQL/MySQL 调优、慢查询排障、迁移规划 |
| 🌿 [Git Workflow Master](engineering（工程）/engineering-git-workflow-master（Git%20工作流大师）.md) | 分支策略、约定式提交、高级 Git | Git 工作流设计、历史清理、适配 CI 的分支管理 |
| 🏛️ [Software Architect](engineering（工程）/engineering-software-architect（软件架构师）.md) | 系统设计、DDD、架构模式、权衡分析 | 架构决策、领域建模、系统演进策略 |
| 🛡️ [SRE](engineering（工程）/engineering-sre（SRE（站点可靠性工程师））.md) | SLO、错误预算、可观测性、混沌工程 | 生产可靠性、减少 toil、容量规划 |
| 🧬 [AI Data Remediation Engineer](engineering（工程）/engineering-ai-data-remediation-engineer（AI%20数据修复工程师）.md) | 自愈管道、隔离环境中的 SLM、语义聚类 | 以零数据丢失规模化修复损坏数据 |
| 🔧 [Data Engineer](engineering（工程）/engineering-data-engineer（数据工程师）.md) | 数据管道、lakehouse 架构、ETL/ELT | 构建可靠的数据基础设施与数仓 |
| 🔗 [Feishu Integration Developer](engineering（工程）/engineering-feishu-integration-developer（飞书集成开发者）.md) | 飞书/Feishu Open Platform、机器人、工作流 | 为飞书生态构建集成 |
| 🧱 [CMS Developer](engineering（工程）/engineering-cms-developer（CMS%20开发者）.md) | WordPress & Drupal 主题、插件/模块、内容架构 | 面向代码的 CMS 实现与定制 |
| 📧 [Email Intelligence Engineer](engineering（工程）/engineering-email-intelligence-engineer（邮件智能工程师）.md) | 邮件解析、MIME 提取、供 AI agents 使用的结构化数据 | 将原始邮件线程转化为可用于推理的上下文 |
| 🎙️ [Voice AI Integration Engineer](engineering（工程）/engineering-voice-ai-integration-engineer（语音%20AI%20集成工程师）.md) | 语音转文本管道、Whisper、ASR、说话人分离 | 端到端转录管道、音频预处理、结构化转录交付 |
| 🖧 [IT Service Manager](engineering（工程）/engineering-it-service-manager（IT%20服务经理）.md) | ITIL 4 服务管理 | 事故/问题/变更管理、SLA、CMDB |
| 🪡 [Minimal Change Engineer](engineering（工程）/engineering-minimal-change-engineer（最小变更工程师）.md) | 最小可行 diff | 只修要求修的内容，不扩大范围 |
| 📜 [OrgScript Engineer](engineering（工程）/engineering-orgscript-engineer（OrgScript%20工程师）.md) | OrgScript 语法与 AST 验证 | 设计/解析 OrgScript 业务逻辑定义 |
| 🧬 [Prompt Engineer](engineering（工程）/engineering-prompt-engineer（提示工程师）.md) | LLM 提示词设计与优化 | 将模糊指令转化为可靠的 AI 行为 |
| 🕸️ [Multi-Agent Systems Architect](engineering（工程）/engineering-multi-agent-systems-architect（多智能体系统架构师）.md) | 多 agent 流水线设计与治理 | 处理 agent 系统的拓扑、上下文、信任、故障恢复 |
| 🛒 [Drupal Shopping Cart Engineer](engineering（工程）/engineering-drupal-shopping-cart（Drupal%20购物车工程师）.md) | Drupal Commerce 店面 | Drupal 10/11 上的目录、支付、结账、订单 |
| 🛍️ [WordPress Shopping Cart Engineer](engineering（工程）/engineering-wordpress-shopping-cart（WordPress%20购物车工程师）.md) | WooCommerce 店面 | WordPress 上的目录、支付、结账、转化 |
| 💳 [Payments & Billing Engineer](engineering（工程）/engineering-payments-billing-engineer（支付与计费工程师）.md) | PSP 集成、幂等支付流程、订阅计费 | Stripe/Adyen/Braintree 集成、webhook 处理、催收、对账 |
| 🌍 [Internationalization Engineer](engineering（工程）/engineering-i18n-engineer（国际化工程师）.md) | ICU MessageFormat、RTL/bidi 布局、CLDR 格式化、伪本地化 | 让应用具备可翻译性、区域感知格式化、RTL 支持、i18n 审计 |
| ⚡ [Drupal Performance Engineer](engineering（工程）/engineering-drupal-performance（Drupal%20性能工程师）.md) | Drupal 性能与 Core Web Vitals | 缓存、DB/查询调优、渲染流水线、高流量 Drupal 剖析 |
| ⚡ [WordPress Performance Engineer](engineering（工程）/engineering-wordpress-performance（WordPress%20性能工程师）.md) | WordPress 性能与 Core Web Vitals | 缓存、查询/资源优化、插件调优、高流量 WP 剖析 |
| ♿ [Section 508 Accessibility Specialist](engineering（工程）/engineering-section-508-specialist（第508条可访问性专家）.md) | 美国联邦 508 / WCAG 可访问性 | ARIA、屏幕阅读器测试、VPAT/ACR 编写、修复 |
| 🏛️ [USWDS Developer](engineering（工程）/engineering-uswds-developer（USWDS%20开发者）.md) | 美国 Web Design System（联邦） | 无障碍政府 UI 组件与设计系统模式 |
| 🔎 [Search Relevance Engineer](engineering（工程）/engineering-search-relevance-engineer（搜索相关性工程师）.md) | 搜索排序与相关性 | 查询理解、嵌入、排序/评估、相关性调优 |
| 🔐 [Identity & Access Engineer](engineering（工程）/engineering-identity-access-engineer（身份与访问工程师）.md) | AuthN/AuthZ 与 IAM | OAuth/OIDC/SAML、SSO、RBAC/ABAC、令牌与会话安全 |
| 🤝 [Realtime Collaboration Engineer](engineering（工程）/engineering-realtime-collaboration-engineer（实时协作工程师）.md) | 实时同步与 presence | CRDT/OT、冲突解决、实时光标、离线同步 |
| 💻 [Desktop App Engineer](engineering（工程）/engineering-desktop-app-engineer（桌面应用工程师）.md) | 跨平台桌面应用 | Electron/Tauri、本机集成、打包、自动更新 |
| 🚀 [Mobile Release Engineer](engineering（工程）/engineering-mobile-release-engineer（移动发布工程师）.md) | 移动端发布与 CI/CD | App Store/Play 提交、签名、分阶段发布、崩溃分流 |
| 🎬 [Video Streaming Engineer](engineering（工程）/engineering-video-streaming-engineer（视频流工程师）.md) | 视频流与转码 | HLS/DASH、ABR、编解码、CDN 分发、低延迟流媒体 |
| 💰 [FinOps Engineer](engineering（工程）/engineering-finops-engineer（FinOps%20工程师）.md) | 云成本工程 | 成本分摊、规格优化、单位经济性、预算与异常控制 |
| 🧩 [WebAssembly Engineer](engineering（工程）/engineering-webassembly-engineer（WebAssembly%20工程师）.md) | WebAssembly 与 WASI | Rust/C++→WASM、沙箱、宿主绑定、性能 |
| 🔌 [API Platform Engineer](engineering（工程）/engineering-api-platform-engineer（API%20平台工程师）.md) | API 网关与平台 | 网关设计、版本控制、限流、开发者门户 |
| 🛟 [Database Reliability Engineer](engineering（工程）/engineering-database-reliability-engineer（数据库可靠性工程师）.md) | 数据库可靠性（DBRE） | 高可用/复制、自动故障转移、PITR 备份、零停机运维 |
| 🛠️ [Developer Tooling Engineer](engineering（工程）/engineering-developer-tooling-engineer（开发者工具工程师）.md) | CLI 与开发者工具 | 命令行工具、内部 DX、构建与开发工作流 |
| 📡 [IoT Fleet Engineer](engineering（工程）/engineering-iot-fleet-engineer（IoT%20设备群工程师）.md) | IoT 与边缘设备群 | 设备配置/身份、MQTT 遥测、OTA 更新 |
| 🔍 [RAG Pipeline Engineer](engineering（工程）/engineering-rag-pipeline-engineer（RAG%20流水线工程师）.md) | 生产级 RAG 流水线 | 分块、检索质量、混合搜索、重排序、评估驱动迭代 |
| 🗄️ [GaussDB Expert Engineer](engineering（工程）/engineering-gaussdb-expert（GaussDB%20专家工程师）.md) | 华为 GaussDB OLTP | GaussDB 企业级 OLTP 性能、高可用与迁移 |
| 🕵️ [Privacy Engineer](engineering（工程）/engineering-privacy-engineer（隐私工程师）.md) | PII 发现、数据最小化、同意执行、DSAR/删除流水线 | 在代码中落实隐私、跨服务被遗忘权、留存自动化 |
| 🦀 [Rust Refactoring Specialist](engineering（工程）/engineering-rust-refactoring-specialist（Rust%20重构专家）.md) | 感知行为的 Rust 重构 | 基于证据、保持行为地重构 crate、trait 与 module |
| 🧪 [LLM Post-Training Engineer](engineering（工程）/engineering-llm-post-training-engineer（LLM%20后训练工程师）.md) | 后训练技术栈（SFT/DPO/GRPO/RLVR） | 基于证据的实验门禁、checkpoint 完整性与故障分类 |
| 📈 [Data Visualization Engineer](engineering（工程）/engineering-data-visualization-engineer（数据可视化工程师）.md) | 符合感知规律的真实数据可视化 | 图表选型、色盲友好配色、高性能 D3/Vega 渲染 |
| 🧠 [Knowledge Graph Engineer](engineering（工程）/engineering-knowledge-graph-engineer（知识图谱工程师）.md) | 知识图谱、实体-关系抽取、图增强 RAG | 将文档结构化为可查询的 Neo4j 图（LangGraph）；溯源、矛盾跟踪、子图检索 |

### 🎨 设计分部

让一切更美观、更易用、更令人愉悦。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎯 [UI Designer](design（设计）/design-ui-designer（UI%20设计师）.md) | 视觉设计、组件库、设计系统 | 界面创建、品牌一致性、组件设计 |
| 🔍 [UX Researcher](design（设计）/design-ux-researcher（UX%20研究员）.md) | 用户测试、行为分析、研究 | 理解用户、可用性测试、设计洞察 |
| 🏛️ [UX Architect](design（设计）/design-ux-architect（UX%20架构师）.md) | 技术架构、CSS 系统、实现 | 面向开发者的基础、实现指导 |
| 🎭 [Brand Guardian](design（设计）/design-brand-guardian（品牌守护者）.md) | 品牌识别、一致性、定位 | 品牌战略、品牌识别开发、规范 |
| 📖 [Visual Storyteller](design（设计）/design-visual-storyteller（视觉故事讲述者）.md) | 视觉叙事、多媒体内容 | 引人入胜的视觉故事、品牌讲述 |
| ✨ [Whimsy Injector](design（设计）/design-whimsy-injector（趣味注入师）.md) | 个性、惊喜感、俏皮交互 | 增添快乐、微交互、彩蛋、品牌个性 |
| 📷 [Image Prompt Engineer](design（设计）/design-image-prompt-engineer（图像提示词工程师）.md) | AI 图像生成提示词、摄影 | 用于 Midjourney、DALL-E、Stable Diffusion 的摄影提示词 |
| 🌈 [Inclusive Visuals Specialist](design（设计）/design-inclusive-visuals-specialist（包容性视觉专家）.md) | 代表性、偏见缓解、真实影像 | 生成文化准确的 AI 图像和视频 |
| 🎭 [Persona Walkthrough Specialist](design（设计）/design-persona-walkthrough（角色走查专家）.md) | 以 persona 为驱动的认知走查 | 在每个滚动位置模拟用户反应与摩擦点 |
| 🧱 [UI Finish-Gate Reviewer](design（设计）/design-ui-finish-gate-reviewer（UI%20交付门禁审查员）.md) | 反泛化 UI 交付门禁 | 通过证据与书面设计契约，在发布前拦截可互换的泛化 UI |

### 💰 付费媒体分部

把广告支出转化为可衡量的业务结果。

| Agent | 专长 | 何时使用 |
| --- | --- | --- |
| 💰 [PPC Campaign Strategist](paid-media（付费媒体）/paid-media-ppc-strategist（PPC%20广告系列策略师）.md) | Google/Microsoft/Amazon Ads、账户架构、竞价 | 账户搭建、预算分配、扩量、性能诊断 |
| 🔍 [Search Query Analyst](paid-media（付费媒体）/paid-media-search-query-analyst（搜索查询分析师）.md) | 搜索词分析、否定关键词、意图映射 | 查询审计、浪费支出消除、关键词发现 |
| 📋 [Paid Media Auditor](paid-media（付费媒体）/paid-media-auditor（付费媒体审计师）.md) | 200+ 点账户审计、竞争分析 | 接手账户、季度回顾、竞标提案 |
| 📡 [Tracking & Measurement Specialist](paid-media（付费媒体）/paid-media-tracking-specialist（跟踪与衡量专家）.md) | GTM、GA4、转化追踪、CAPI | 新实施、追踪审计、平台迁移 |
| ✍️ [Ad Creative Strategist](paid-media（付费媒体）/paid-media-creative-strategist（广告创意策略师）.md) | RSA 文案、Meta 创意、Performance Max 资产 | 创意上线、测试计划、广告疲劳更新 |
| 📺 [Programmatic & Display Buyer](paid-media（付费媒体）/paid-media-programmatic-buyer（程序化与展示广告买家）.md) | GDN、DSP、合作媒体、ABM 展示广告 | 展示广告规划、合作方拓展、ABM 项目 |
| 📱 [Paid Social Strategist](paid-media（付费媒体）/paid-media-paid-social-strategist（付费社交策略师）.md) | Meta、LinkedIn、TikTok、跨平台社交 | 社交广告项目、平台选择、受众策略 |

### 💼 销售分部

通过工艺，而不是 CRM 杂务，把 pipeline 变成收入。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎯 [Outbound Strategist](sales（销售）/sales-outbound-strategist（外拓策略师）.md) | 基于信号的潜客开发、多渠道序列、ICP 定位 | 通过研究驱动的外联构建 pipeline，而不是靠数量 |
| 🔍 [Discovery Coach](sales（销售）/sales-discovery-coach（发现教练）.md) | SPIN、Gap Selling、Sandler——问题设计与电话结构 | 为 discovery call 做准备、资格筛选机会、辅导销售代表 |
| ♟️ [Deal Strategist](sales（销售）/sales-deal-strategist（交易策略师）.md) | MEDDPICC 资格判定、竞争定位、赢单规划 | 为交易打分、暴露 pipeline 风险、构建赢单策略 |
| 🛠️ [Sales Engineer](sales（销售）/sales-engineer（销售工程师）.md) | 技术演示、POC 范围界定、竞争对手战卡 | 售前技术取胜、演示准备、竞争定位 |
| 🏹 [Proposal Strategist](sales（销售）/sales-proposal-strategist（提案策略师）.md) | RFP 响应、赢单主题、叙事结构 | 撰写真正能说服人的提案，而不只是形式合规 |
| 📊 [Pipeline Analyst](sales（销售）/sales-pipeline-analyst（Pipeline%20分析师）.md) | 预测、pipeline 健康度、交易速度、RevOps | pipeline 回顾、预测准确性、收入运营 |
| 🗺️ [Account Strategist](sales（销售）/sales-account-strategist（客户战略师）.md) | Land-and-expand、QBR、利益相关方映射 | 售后扩张、客户规划、NRR 增长 |
| 🏋️ [Sales Coach](sales（销售）/sales-coach（销售教练）.md) | 代表培养、通话辅导、pipeline 回顾促进 | 通过结构化辅导让每个销售代表和每笔交易都更好 |
| 🎯 [Sales Outreach](specialized（专项）/sales-outreach（销售拓展专家）.md) | 冷启动潜客开发、多触点节奏、异议处理、提案 | B2B 漏斗顶部外联——从冷邮件到预约 discovery call |
| 🧲 [Offer & Lead Gen Strategist](sales（销售）/sales-offer-lead-gen-strategist（优惠与线索生成策略师）.md) | Offer 与 lead magnet | 漏斗顶部的 offer 构建与线索生成 |

### 📢 营销分部

一次一个真实互动，增长你的受众。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🚀 [Growth Hacker](marketing（营销）/marketing-growth-hacker（增长黑客）.md) | 快速用户获取、病毒式循环、实验 | 爆发式增长、用户获取、转化优化 |
| 📝 [Content Creator](marketing（营销）/marketing-content-creator（内容创作者）.md) | 多平台内容、编辑日历 | 内容策略、文案写作、品牌讲述 |
| 🐦 [Twitter Engager](marketing（营销）/marketing-twitter-engager（Twitter%20运营专家）.md) | 实时互动、思想领导力 | Twitter 策略、LinkedIn 活动、专业社交 |
| 🛰️ [X/Twitter Intelligence Analyst](marketing（营销）/marketing-x-twitter-intelligence-analyst（X／Twitter%20情报分析师）.md) | 社交聆听、趋势检测、账号监控 | 在 X/Twitter 上进行品牌风险、竞争对手与受众情报分析 |
| 📱 [TikTok Strategist](marketing（营销）/marketing-tiktok-strategist（TikTok%20策略专家）.md) | 病毒式内容、算法优化 | TikTok 增长、病毒内容、Gen Z/Millennial 受众 |
| 📸 [Instagram Curator](marketing（营销）/marketing-instagram-curator（Instagram%20运营专家）.md) | 视觉叙事、社区建设 | Instagram 策略、美学开发、视觉内容 |
| 🤝 [Reddit Community Builder](marketing（营销）/marketing-reddit-community-builder（Reddit%20社区运营）.md) | 真实互动、价值驱动内容 | Reddit 策略、社区信任、真实营销 |
| 📱 [App Store Optimizer](marketing（营销）/marketing-app-store-optimizer（应用商店优化专家）.md) | ASO、转化优化、可发现性 | 应用营销、商店优化、应用增长 |
| 🌐 [Social Media Strategist](marketing（营销）/marketing-social-media-strategist（社交媒体策略师）.md) | 跨平台策略、活动 | 整体社交策略、多平台活动 |
| 📕 [Xiaohongshu Specialist](marketing（营销）/marketing-xiaohongshu-specialist（小红书运营专家）.md) | 生活方式内容、趋势驱动策略 | 小红书增长、美学叙事、Gen Z 受众 |
| 💬 [WeChat Official Account Manager](marketing（营销）/marketing-wechat-official-account（微信公众号运营专家）.md) | 订阅者互动、内容营销 | 微信公众号策略、社区建设、转化优化 |
| 🧠 [Zhihu Strategist](marketing（营销）/marketing-zhihu-strategist（知乎运营专家）.md) | 思想领导力、知识驱动的互动 | 知乎权威建设、问答策略、线索生成 |
| 🇨🇳 [Baidu SEO Specialist](marketing（营销）/marketing-baidu-seo-specialist（百度%20SEO%20专家）.md) | 百度优化、中国 SEO、ICP 合规 | 在百度排名并触达中国搜索市场 |
| 🎬 [Bilibili Content Strategist](marketing（营销）/marketing-bilibili-content-strategist（Bilibili%20内容策略师）.md) | B站算法、弹幕文化、UP主 增长 | 以社区优先内容在 Bilibili 上构建受众 |
| 🎠 [Carousel Growth Engine](marketing（营销）/marketing-carousel-growth-engine（轮播图增长引擎）.md) | TikTok/Instagram 轮播图、自主发布 | 生成并发布病毒式轮播内容 |
| 💼 [LinkedIn Content Creator](marketing（营销）/marketing-linkedin-content-creator（领英内容创作者）.md) | 个人品牌、思想领导力、专业内容 | LinkedIn 增长、专业受众建设、B2B 内容 |
| 🛒 [China E-Commerce Operator](marketing（营销）/marketing-china-ecommerce-operator（中国电商运营专家）.md) | 淘宝、天猫、拼多多、直播电商 | 在中国运营多平台电商 |
| 🎥 [Kuaishou Strategist](marketing（营销）/marketing-kuaishou-strategist（快手运营策略师）.md) | 快手、老铁 社区、草根增长 | 在低线市场构建真实受众 |
| 🔍 [SEO Specialist](marketing（营销）/marketing-seo-specialist（SEO%20专家）.md) | 技术 SEO、内容策略、外链建设 | 推动可持续的自然搜索增长 |
| 📘 [Book Co-Author](marketing（营销）/marketing-book-co-author（图书联合作者）.md) | 思想领导力图书、代写、出版 | 为创始人和专家提供战略性图书协作 |
| 🌏 [Cross-Border E-Commerce Specialist](marketing（营销）/marketing-cross-border-ecommerce（跨境电商专家）.md) | Amazon、Shopee、Lazada、跨境履约 | 全漏斗跨境电商策略 |
| 🎵 [Douyin Strategist](marketing（营销）/marketing-douyin-strategist（抖音运营策略师）.md) | 抖音平台、短视频营销、算法 | 在中国领先的短视频平台上增长受众 |
| 🎙️ [Livestream Commerce Coach](marketing（营销）/marketing-livestream-commerce-coach（直播带货教练）.md) | 主播培训、直播间优化、转化 | 建立高绩效直播电商运营 |
| 🎧 [Podcast Strategist](marketing（营销）/marketing-podcast-strategist（播客策略师）.md) | 播客内容策略、平台优化 | 中国播客市场策略与运营 |
| 🔒 [Private Domain Operator](marketing（营销）/marketing-private-domain-operator（私域运营专家）.md) | 企业微信、私域流量、社群运营 | 构建企业微信私域生态 |
| 🎬 [Short-Video Editing Coach](marketing（营销）/marketing-short-video-editing-coach（短视频剪辑教练）.md) | 后期制作、剪辑工作流、平台规格 | 亲手式短视频剪辑培训与优化 |
| 🔥 [Weibo Strategist](marketing（营销）/marketing-weibo-strategist（微博运营策略师）.md) | 新浪微博、热搜话题、粉丝互动 | 全栈微博运营与增长 |
| 🎙️ [Global Podcast Strategist](marketing（营销）/marketing-global-podcast-strategist（全球播客策略师）.md) | 节目定位、受众增长、变现 | 播客启动、平台算法、赞助、社区建设 |
| 🔮 [AI Citation Strategist](marketing（营销）/marketing-ai-citation-strategist（AI%20引用策略师）.md) | AEO/GEO、AI 推荐可见性、引用审计 | 提升 ChatGPT、Claude、Gemini、Perplexity 中的品牌可见度 |
| 🇨🇳 [China Market Localization Strategist](marketing（营销）/marketing-china-market-localization-strategist（中国市场本地化策略师）.md) | 全栈中国市场本地化、Douyin/Xiaohongshu/WeChat GTM | 将趋势信号转化为可执行的中国 go-to-market 策略 |
| 🎬 [Video Optimization Specialist](marketing（营销）/marketing-video-optimization-specialist（视频优化专家）.md) | YouTube 算法策略、章节、缩略图概念 | YouTube 频道增长、视频 SEO、受众留存优化 |
| 🏗️ [AEO Foundations Architect](marketing（营销）/marketing-aeo-foundations（AEO%20基础架构师）.md) | AI Engine Optimization 基础设施 | llms.txt、面向 AI 的 robots.txt、agent 发现文件 |
| 🤖 [Agentic Search Optimizer](marketing（营销）/marketing-agentic-search-optimizer（代理式搜索优化师）.md) | WebMCP 与 agentic 任务完成 | 让网站可被 AI 浏览 agents 使用 |
| 📧 [Email Marketing Strategist](marketing（营销）/marketing-email-strategist（电子邮件营销策略师）.md) | 生命周期邮件与送达率 | CRM 活动、自动化、细分 |
| 📡 [Multi-Platform Publisher](marketing（营销）/marketing-multi-platform-publisher（多平台发布专家）.md) | 一键中文多平台发布 | 将一篇文章路由到 知乎/小红书/CSDN/B站/公众号/掘金 |
| 📣 [PR & Communications Manager](marketing（营销）/marketing-pr-communications-manager（公关与传播经理）.md) | PR、媒体关系与危机公关 | 新闻稿、思想领导力、声誉管理 |

### 📊 产品分部

在正确的时间，构建正确的东西。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎯 [Sprint Prioritizer](product（产品）/product-sprint-prioritizer（冲刺优先级排序师）.md) | 敏捷规划、功能优先级排序 | Sprint 规划、资源分配、待办项管理 |
| 🔍 [Trend Researcher](product（产品）/product-trend-researcher（趋势研究员）.md) | 市场情报、竞争分析 | 市场研究、机会评估、趋势识别 |
| 💬 [Feedback Synthesizer](product（产品）/product-feedback-synthesizer（反馈合成师）.md) | 用户反馈分析、洞察提取 | 反馈分析、用户洞察、产品优先级 |
| 🧠 [Behavioral Nudge Engine](product（产品）/product-behavioral-nudge-engine（行为助推引擎）.md) | 行为心理学、推动设计、参与度 | 通过行为科学最大化用户动机 |
| 🧭 [Product Manager](product（产品）/product-manager（产品经理）.md) | 全生命周期产品负责人 | 发现、PRD、路线图规划、GTM、结果衡量 |

### 🎬 项目管理分部

让列车按时运行（并且不超预算）。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎬 [Studio Producer](project-management（项目管理）/project-management-studio-producer（工作室制作人）.md) | 高层编排、组合管理 | 多项目监督、战略对齐、资源分配 |
| 🐑 [Project Shepherd](project-management（项目管理）/project-management-project-shepherd（项目牧羊人）.md) | 跨职能协调、时间线管理 | 端到端项目协调、利益相关者管理 |
| ⚙️ [Studio Operations](project-management（项目管理）/project-management-studio-operations（工作室运营）.md) | 日常效率、流程优化 | 运营卓越、团队支持、生产力 |
| 🧪 [Experiment Tracker](project-management（项目管理）/project-management-experiment-tracker（实验追踪师）.md) | A/B 测试、假设验证 | 实验管理、数据驱动决策、测试 |
| 👔 [Senior Project Manager](project-management（项目管理）/project-manager-senior（资深项目经理）.md) | 现实范围界定、任务转换 | 将规格转化为任务、范围管理 |
| 📋 [Jira Workflow Steward](project-management（项目管理）/project-management-jira-workflow-steward（Jira%20工作流管家）.md) | Git 工作流、分支策略、可追溯性 | 强制执行与 Jira 关联的 Git 规范和交付 |
| 📋 [Meeting Notes Specialist](project-management（项目管理）/project-management-meeting-notes-specialist（会议记录专家）.md) | 结构化会议摘要 | 提取决策、行动项、未决问题 |

### 🧪 测试分部

把东西搞坏，这样用户就不用这么做了。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 📸 [Evidence Collector](testing（测试）/testing-evidence-collector（证据收集员）.md) | 基于截图的 QA、视觉证据 | UI 测试、视觉验证、Bug 文档化 |
| 🔍 [Reality Checker](testing（测试）/testing-reality-checker（现实检查员）.md) | 基于证据的认证、质量门禁 | 生产就绪、质量批准、发布认证 |
| 📊 [Test Results Analyzer](testing（测试）/testing-test-results-analyzer（测试结果分析专家）.md) | 测试评估、指标分析 | 测试输出分析、质量洞察、覆盖率报告 |
| ⚡ [Performance Benchmarker](testing（测试）/testing-performance-benchmarker（性能基准测试专家）.md) | 性能测试、优化 | 速度测试、负载测试、性能调优 |
| 🔌 [API Tester](testing（测试）/testing-api-tester（API测试专家）.md) | API 验证、集成测试 | API 测试、端点验证、集成 QA |
| 🛠️ [Tool Evaluator](testing（测试）/testing-tool-evaluator（工具评估专家）.md) | 技术评估、工具选择 | 工具评估、软件推荐、技术决策 |
| 🔄 [Workflow Optimizer](testing（测试）/testing-workflow-optimizer（工作流优化专家）.md) | 流程分析、工作流改进 | 流程优化、效率提升、自动化机会 |
| ♿ [Accessibility Auditor](testing（测试）/testing-accessibility-auditor（无障碍审计师）.md) | WCAG 审核、辅助技术测试 | 无障碍合规、屏幕阅读器测试、包容性设计验证 |
| 🎭 [Test Automation Engineer](testing（测试）/testing-test-automation-engineer（测试自动化工程师）.md) | Playwright/Cypress E2E、消除 flaky、CI 并行化 | 浏览器测试套件、确定性流水线、基于 trace 的故障调试 |

### 🔒 安全部门

守护整个技术栈——从安全设计架构到入侵响应。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🛡️ [Security Architect](security（安全）/security-architect（安全架构师）.md) | 威胁建模、安全设计、信任边界 | 系统安全模型、架构评审、纵深防御 |
| 🔐 [Application Security Engineer](security（安全）/security-appsec-engineer（应用安全工程师）.md) | SDLC 安全、SAST/DAST、安全代码审查 | 保护开发生命周期、代码级漏洞 |
| 🗡️ [Penetration Tester](security（安全）/security-penetration-tester（渗透测试工程师）.md) | 授权渗透测试、红队行动、利用 | 在攻击者之前发现可利用弱点 |
| ☁️ [Cloud Security Architect](security（安全）/security-cloud-security-architect（云安全架构师）.md) | 零信任、云原生纵深防御 | 保护云基础设施与架构 |
| 🚨 [Incident Responder](security（安全）/security-incident-responder（事件响应者）.md) | DFIR、入侵调查、威胁遏制 | 正在进行的入侵、取证、危机响应 |
| 🔍 [Threat Intelligence Analyst](security（安全）/security-threat-intelligence-analyst（威胁情报分析师）.md) | 对手追踪、campaign 映射、ATT&CK | 理解谁在攻击以及如何攻击 |
| 🎯 [Threat Detection Engineer](security（安全）/security-threat-detection-engineer（威胁检测工程师）.md) | SIEM 规则、威胁狩猎、ATT&CK 映射 | 构建检测层与威胁狩猎能力 |
| 🛡️ [Senior SecOps Engineer](security（安全）/security-senior-secops（高级%20SecOps%20工程师）.md) | 密钥扫描、安全默认提交 | 对每次变更都进行防御性的代码级安全保护 |
| 📋 [Compliance Auditor](security（安全）/security-compliance-auditor（合规审计师）.md) | SOC 2、ISO 27001、HIPAA、PCI-DSS | 指导组织完成合规认证 |
| 🛡️ [Blockchain Security Auditor](security（安全）/security-blockchain-security-auditor（区块链安全审计师）.md) | 智能合约审计、漏洞利用分析 | 在部署前发现合约中的漏洞 |
| 🔎 [AI-Generated Code Security Auditor](security（安全）/security-ai-generated-code-auditor（AI%20生成代码安全审计师）.md) | AI/氛围编程应用安全审查 | 硬编码密钥、失效的 RLS、提示词注入汇点 |
| 🔑 [Secrets & Credential Hygiene Engineer](security（安全）/security-secrets-credential-engineer（密钥与凭据治理工程师）.md) | 密钥与凭据生命周期 | 检测、密库保管、轮换与泄露响应 |

### 🛟 支持分部

运营的骨干。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 💬 [Support Responder](support（支持）/support-support-responder（客户支持响应专家）.md) | 客户服务、问题解决 | 客户支持、用户体验、支持运营 |
| 📊 [Analytics Reporter](support（支持）/support-analytics-reporter（分析报告专家）.md) | 数据分析、仪表板、洞察 | 商业智能、KPI 跟踪、数据可视化 |
| 💰 [Finance Tracker](support（支持）/support-finance-tracker（财务跟踪分析师）.md) | 财务规划、预算管理 | 财务分析、现金流、业务绩效 |
| 🏗️ [Infrastructure Maintainer](support（支持）/support-infrastructure-maintainer（基础设施维护专家）.md) | 系统可靠性、性能优化 | 基础设施管理、系统运维、监控 |
| ⚖️ [Legal Compliance Checker](support（支持）/support-legal-compliance-checker（法律合规检查专家）.md) | 合规、法规、法律审查 | 法律合规、监管要求、风险管理 |
| 📑 [Executive Summary Generator](support（支持）/support-executive-summary-generator（高管摘要生成器）.md) | 面向高管层的沟通、战略摘要 | 高管汇报、战略沟通、决策支持 |

### 🥽 空间计算分部

构建沉浸式未来。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🏗️ [XR Interface Architect](spatial-computing（空间计算）/xr-interface-architect（XR%20界面架构师）.md) | 空间交互设计、沉浸式 UX | AR/VR/XR 界面设计、空间计算 UX |
| 💻 [macOS Spatial/Metal Engineer](spatial-computing（空间计算）/macos-spatial-metal-engineer（macOS%20空间计算与Metal%20工程师）.md) | Swift、Metal、高性能 3D | macOS 空间计算、Vision Pro 原生应用 |
| 🌐 [XR Immersive Developer](spatial-computing（空间计算）/xr-immersive-developer（XR%20沉浸式开发者）.md) | WebXR、基于浏览器的 AR/VR | 基于浏览器的沉浸式体验、WebXR 应用 |
| 🎮 [XR Cockpit Interaction Specialist](spatial-computing（空间计算）/xr-cockpit-interaction-specialist（XR%20驾驶舱交互专家）.md) | 驾驶舱式控制、沉浸式系统 | 驾驶舱控制系统、沉浸式控制界面 |
| 🍎 [visionOS Spatial Engineer](spatial-computing（空间计算）/visionos-spatial-engineer（visionOS%20空间工程师）.md) | Apple Vision Pro 开发 | Vision Pro 应用、空间计算体验 |
| 🔌 [Terminal Integration Specialist](spatial-computing（空间计算）/terminal-integration-specialist（终端集成专家）.md) | 终端集成、命令行工具 | CLI 工具、终端工作流、开发者工具 |

### 🎯 专门分部

那些不适合被塞进盒子的独特专家。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎭 [Agents Orchestrator](specialized（专项）/agents-orchestrator（多智能体编排师）.md) | 多 agent 协调、工作流管理 | 需要多个 agent 协同的复杂项目 |
| 🔍 [LSP/Index Engineer](specialized（专项）/lsp-index-engineer（LSP%20与索引工程师）.md) | Language Server Protocol、代码智能 | 代码智能系统、LSP 实现、语义索引 |
| 📥 [Sales Data Extraction Agent](specialized（专项）/sales-data-extraction-agent（销售数据提取%20Agent）.md) | Excel 监控、销售指标提取 | 销售数据摄取、MTD/YTD/年末指标 |
| 📈 [Data Consolidation Agent](specialized（专项）/data-consolidation-agent（数据整合%20Agent）.md) | 销售数据聚合、仪表板报告 | 区域汇总、销售代表表现、pipeline 快照 |
| 📬 [Report Distribution Agent](specialized（专项）/report-distribution-agent（报告分发%20Agent）.md) | 自动化报告投递 | 基于区域的报告分发、定时发送 |
| 🔐 [Agentic Identity & Trust Architect](specialized（专项）/agentic-identity-trust（智能体身份与信任架构师）.md) | Agent 身份、认证、信任验证 | 多 agent 身份系统、agent 授权、审计轨迹 |
| 🔗 [Identity Graph Operator](specialized（专项）/identity-graph-operator（身份图谱运营专家）.md) | 多 agent 系统中的共享身份解析 | 实体去重、合并提议、跨 agent 身份一致性 |
| 💸 [Accounts Payable Agent](specialized（专项）/accounts-payable-agent（应付账款%20Agent）.md) | 支付处理、供应商管理、审计 | 跨 crypto、法币、稳定币的自主支付执行 |
| 🌍 [Cultural Intelligence Strategist](specialized（专项）/specialized-cultural-intelligence-strategist（文化智能策略师）.md) | 全球 UX、代表性、文化排斥 | 确保软件在不同文化中都能产生共鸣 |
| 🗣️ [Developer Advocate](specialized（专项）/specialized-developer-advocate（开发者布道师）.md) | 社区建设、DX、开发者内容 | 连接产品与开发者社区 |
| 🔬 [Model QA Specialist](specialized（专项）/specialized-model-qa（模型%20QA%20专家）.md) | ML 审计、特征分析、可解释性 | 面向机器学习模型的端到端 QA |
| 🗃️ [ZK Steward](specialized（专项）/zk-steward（知识卡片管理员）.md) | 知识管理、Zettelkasten、笔记 | 构建相互连接、经过验证的知识库 |
| 🔌 [MCP Builder](specialized（专项）/specialized-mcp-builder（MCP%20构建专家）.md) | Model Context Protocol 服务器、AI agent 工具 | 构建扩展 AI agent 能力的 MCP 服务器 |
| 📄 [Document Generator](specialized（专项）/specialized-document-generator（文档生成专家）.md) | 从代码生成 PDF、PPTX、DOCX、XLSX | 专业文档创建、报告、数据可视化 |
| ⚙️ [Automation Governance Architect](specialized（专项）/automation-governance-architect（自动化治理架构师）.md) | 自动化治理、n8n、工作流审计 | 大规模评估与治理业务自动化 |
| 📚 [Corporate Training Designer](specialized（专项）/corporate-training-designer（企业培训设计师）.md) | 企业培训、课程开发 | 设计培训系统与学习项目 |
| 🌱 [Personal Growth Mentor](specialized（专项）/personal-growth-mentor（个人成长导师）.md) | 目标清晰、习惯系统、责任机制、人生策略 | 无鸡汤式的跨领域个人成长 |
| 🏛️ [Government Digital Presales Consultant](specialized（专项）/government-digital-presales-consultant（政务数字化售前顾问）.md) | 中国 ToG 售前、数字化转型 | 政府数字化转型方案与投标 |
| ⚕️ [Healthcare Marketing Compliance](specialized（专项）/healthcare-marketing-compliance（医疗营销合规专家）.md) | 中国医疗广告合规 | 医疗营销监管合规 |
| 🎯 [Recruitment Specialist](specialized（专项）/recruitment-specialist（招聘专家）.md) | 人才获取、招聘运营 | 招聘策略、寻源与招聘流程 |
| 🎓 [Study Abroad Advisor](specialized（专项）/study-abroad-advisor（留学顾问）.md) | 国际教育、申请规划 | 覆盖美国、英国、加拿大、澳大利亚的留学规划 |
| 🔗 [Supply Chain Strategist](specialized（专项）/supply-chain-strategist（供应链策略师）.md) | 供应链管理、采购策略 | 供应链优化与采购规划 |
| 🗺️ [Workflow Architect](specialized（专项）/specialized-workflow-architect（工作流架构师）.md) | 工作流发现、映射与规格说明 | 在编写代码之前，先映射系统中的每一条路径 |
| ☁️ [Salesforce Architect](specialized（专项）/specialized-salesforce-architect（Salesforce%20架构师）.md) | 多云 Salesforce 设计、governor limits、集成 | 企业级 Salesforce 架构、org 策略、部署流水线 |
| 🇫🇷 [French Consulting Market Navigator](specialized（专项）/specialized-french-consulting-market（法国咨询市场导航员）.md) | ESN/SI 生态、portage salarial、费率定位 | 法国 IT 市场中的自由职业咨询 |
| 🇰🇷 [Korean Business Navigator](specialized（专项）/specialized-korean-business-navigator（韩国商务导航师）.md) | 韩国商业文化、품의 流程、关系机制 | 外国专业人士在韩国商业关系中的导航 |
| 🏗️ [Civil Engineer](specialized（专项）/specialized-civil-engineer（土木工程师）.md) | 结构分析、岩土设计、全球建筑规范 | 跨 Eurocode、ACI、AISC 等多标准的结构工程 |
| 🎧 [Customer Service](specialized（专项）/customer-service（客户服务专家）.md) | 全渠道支持、投诉处理、留存、升级 | 任意行业客户支持——零售、SaaS、酒店、金融、物流 |
| 🏥 [Healthcare Customer Service](specialized（专项）/healthcare-customer-service（医疗客户服务专家）.md) | 了解 HIPAA 的患者支持、账单、保险、紧急转接 | 需要合规、富有同理心的患者支持的医疗机构 |
| 🏨 [Hospitality Guest Services](specialized（专项）/hospitality-guest-services（酒店宾客服务专家）.md) | 预订、礼宾、投诉恢复、忠诚度、活动 | 酒店、度假村、餐厅与活动场地 |
| 🤝 [HR Onboarding](specialized（专项）/hr-onboarding（人力资源入职专家）.md) | 入职前准备、合规、福利登记、30-60-90 天计划 | 任何公司为新员工入职——从初创到企业 |
| 🌐 [Language Translator](specialized（专项）/language-translator（语言翻译专家）.md) | 西班牙语 ↔ 英语翻译、方言意识、文化语境 | 旅行、商务、医疗和法律翻译需求 |
| ⏱️ [Legal Billing & Time Tracking](specialized（专项）/legal-billing-time-tracking（法律计费与工时管理专家）.md) | 时间记录、计费叙事、IOLTA 合规、催收 | 帮助律所最大化收入回收与计费准确性 |
| 📋 [Legal Client Intake](specialized（专项）/legal-client-intake（法律客户接洽专家）.md) | 潜在客户资格筛选、冲突检索、咨询排期 | 帮助律所将咨询转化为已签约客户 |
| ⚖️ [Legal Document Review](specialized（专项）/legal-document-review（法律文件审查专家）.md) | 合同审查、风险标记、版本比较、合规 | 任何执业领域都可使用的、适合律师进行初审的审查 |
| 🏦 [Loan Officer Assistant](specialized（专项）/loan-officer-assistant（信贷专员助理）.md) | 借款人录入、TRID 合规、pipeline 跟踪、成交协调 | 抵押贷款与消费信贷团队 |
| 🏠 [Real Estate Buyer & Seller](specialized（专项）/real-estate-buyer-seller（房地产买卖顾问）.md) | 买卖方代理、报价、交易协调 | 住宅与投资类房地产交易 |
| 🛒 [Retail Customer Returns](specialized（专项）/retail-customer-returns（零售退货服务专家）.md) | 退货处理、欺诈预防、换货、供应商退货 | 线下门店、电商和全渠道零售 |
| ♟️ [Business Strategist](specialized（专项）/business-strategist（商业策略师）.md) | 管理咨询式战略 | 竞争分析、市场进入、增长规划 |
| 🔄 [Change Management Consultant](specialized（专项）/change-management-consultant（变革管理顾问）.md) | ADKAR/Kotter/Prosci 变革 | 引导组织完成转型与采纳 |
| 🧭 [Chief of Staff](specialized（专项）/specialized-chief-of-staff（幕僚长）.md) | 高管协调 | 过滤噪音、负责流程、路由决策 |
| 🌟 [Customer Success Manager](specialized（专项）/customer-success-manager（客户成功经理）.md) | 入职、健康度与留存 | QBR、流失预防、续约与扩展 |
| 📝 [Grant Writer](specialized（专项）/grant-writer（资助申请撰稿人）.md) | 资助提案与资金获取 | 为非营利/研究撰写 LOI、提案、预算 |
| 🏥 [Medical Billing & Coding Specialist](specialized（专项）/medical-billing-coding-specialist（医疗计费与编码专家）.md) | ICD-10/CPT/HCPCS 与收入周期 | 索赔、拒付管理、RCM 优化 |
| 💰 [Pricing Analyst](specialized（专项）/specialized-pricing-analyst（定价分析师）.md) | 定价模型与利润率优化 | 竞争对手/成本分析、基于价值的定价 |
| 💼 [Chief Financial Officer](specialized（专项）/chief-financial-officer（首席财务官）.md) | 资本配置与财务战略 | 财务、FP&A、并购财务、投资者与董事会汇报 |
| 🌱 [ESG & Sustainability Officer](specialized（专项）/esg-sustainability-officer（ESG%20与可持续发展官）.md) | ESG 项目与披露 | 可持续战略、减碳、报告 |
| 🔐 [Data Privacy Officer](specialized（专项）/data-privacy-officer（数据隐私官）.md) | GDPR/CCPA 隐私合规 | 数据映射、DPIA、同意、泄露响应 |
| ⚙️ [Operations Manager](specialized（专项）/operations-manager（运营经理）.md) | Lean/Six Sigma 运营 | 流程映射、容量规划、KPI 治理 |
| 🤝 [M&A Integration Manager](specialized（专项）/ma-integration-manager（并购整合经理）.md) | 并购后整合 | Day 1/100 天计划、协同效应跟踪、TSA 管理 |
| 🧠 [Organizational Psychologist](specialized（专项）/organizational-psychologist（组织心理学家）.md) | 团队动态与文化健康 | 心理安全、倦怠风险、高绩效团队 |
| ⚔️ [Strategy Duel Agent](specialized（专项）/specialized-strategy-duel-agent（策略对决智能体）.md) | 博弈论与三十六计 | 回合制策略对决、对抗场景模拟 |
| 🛡️ [FedRAMP & RMF Compliance Engineer](specialized（专项）/specialized-fedramp-rmf-compliance（FedRAMP%20与%20RMF%20合规工程师）.md) | 联邦云授权（ATO） | NIST 800-53、FedRAMP Rev5/20x、SSP/POA&M、ConMon、OSCAL |
| 🏺 [Codebase Archaeologist](specialized（专项）/specialized-codebase-archaeologist（代码库考古专家）.md) | 多工具代码库漂移审计 | 检测 Claude/Cursor/Copilot/Windsurf 修改之间的隐性漂移 |
| 🧾 [Resume Tailor](specialized（专项）/resume-tailor（简历定制专家）.md) | 面向求职者的简历优化 | JD 映射、ATS 关键词对齐、经验与要求匹配 |
| 🧡 [Aging Parent Care Companion](specialized（专项）/healthcare-aging-parent-care-companion（老年父母照护伙伴）.md) | 家庭照护者决策支持 | 预约/用药协调、照护团队沟通、照护者福祉（符合 HIPAA） |
| 🏛️ [Master Plan Architect](specialized（专项）/specialized-master-plan-architect（总体规划架构师）.md) | 架构教学、红队计划批判 | 深度架构教学、风险批判、完整 Markdown 实施计划（零代码执行） |

### 💵 财务分部

会计、财务分析、税务策略与投资研究专家。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 📒 [Bookkeeper & Controller](finance（财务）/finance-bookkeeper-controller（簿记员与财务总监）.md) | 月末结账、对账、GAAP 合规、内部控制 | 日常会计运营、审计准备、财务记录维护 |
| 📊 [Financial Analyst](finance（财务）/finance-financial-analyst（财务分析师）.md) | 财务建模、预测、情景分析、决策支持 | 三张表模型、差异分析、数据驱动商业智能 |
| 📈 [FP&A Analyst](finance（财务）/finance-fpa-analyst（FP与A%20分析师）.md) | 预算编制、滚动预测、差异分析、业务回顾 | 年度经营计划、月度业务回顾、战略资源分配 |
| 🔍 [Investment Researcher](finance（财务）/finance-investment-researcher（投资研究员）.md) | 尽职调查、投资组合分析、资产估值、股票研究 | 投资论点开发、风险评估、市场研究 |
| 🏛️ [Tax Strategist](finance（财务）/finance-tax-strategist（税务策略师）.md) | 税务优化、多司法辖区合规、转让定价 | 实体架构、ETR 分析、审计抗辩、战略税务规划 |

### 🎮 游戏开发分部

跨所有主流引擎构建世界、系统与体验。

#### 跨引擎 agents（与引擎无关）

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🎯 [Game Designer](game-development（游戏开发）/game-designer（游戏设计师）.md) | 系统设计、GDD 编写、经济平衡、游戏循环 | 设计游戏机制、成长系统、撰写设计文档 |
| 🗺️ [Level Designer](game-development（游戏开发）/level-designer（关卡设计师）.md) | 布局理论、节奏、遭遇设计、环境叙事 | 构建关卡、设计遭遇流程、空间叙事 |
| 🎨 [Technical Artist](game-development（游戏开发）/technical-artist（技术美术）.md) | Shader、VFX、LOD 流水线、美术到引擎优化 | 连接美术与工程、shader 编写、性能安全的资源流水线 |
| 🔊 [Game Audio Engineer](game-development（游戏开发）/game-audio-engineer（游戏音频工程师）.md) | FMOD/Wwise、自适应音乐、空间音频、音频预算 | 交互式音频系统、动态音乐、音频性能 |
| 📖 [Narrative Designer](game-development（游戏开发）/narrative-designer（叙事设计师）.md) | 故事系统、分支对话、背景架构 | 撰写分支叙事、实现对话系统、世界观背景 |
| 💰 [Economy Designer](game-development（游戏开发）/economy-designer（经济系统设计师）.md) | 虚拟货币、产出与消耗、变现建模、通胀控制 | 设计游戏内经济、平衡 F2P 变现、在线调优经济体系 |

#### Unity

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🏗️ [Unity Architect](game-development（游戏开发）/unity（Unity开发）/unity-architect（Unity%20架构师）.md) | ScriptableObjects、数据驱动模块化、DOTS/ECS | 大型 Unity 项目、数据驱动系统设计、ECS 性能工作 |
| ✨ [Unity Shader Graph Artist](game-development（游戏开发）/unity（Unity开发）/unity-shader-graph-artist（Unity%20Shader%20Graph%20艺术家）.md) | Shader Graph、HLSL、URP/HDRP、Renderer Features | 自定义 Unity 材质、VFX shader、后处理通道 |
| 🌐 [Unity Multiplayer Engineer](game-development（游戏开发）/unity（Unity开发）/unity-multiplayer-engineer（Unity%20多人游戏工程师）.md) | Netcode for GameObjects、Unity Relay/Lobby、服务器权威、预测 | 在线 Unity 游戏、客户端预测、Unity Gaming Services 集成 |
| 🛠️ [Unity Editor Tool Developer](game-development（游戏开发）/unity（Unity开发）/unity-editor-tool-developer（Unity%20编辑器工具开发者）.md) | EditorWindow、AssetPostprocessor、PropertyDrawer、构建验证 | 自定义 Unity 编辑器工具、流水线自动化、内容验证 |

#### Unreal Engine

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| ⚙️ [Unreal Systems Engineer](game-development（游戏开发）/unreal-engine（虚幻引擎开发）/unreal-systems-engineer（Unreal%20系统工程师）.md) | C++/Blueprint 混合、GAS、Nanite 约束、内存管理 | 复杂的 Unreal 游戏系统、Gameplay Ability System、引擎级 C++ |
| 🎨 [Unreal Technical Artist](game-development（游戏开发）/unreal-engine（虚幻引擎开发）/unreal-technical-artist（虚幻引擎技术美术）.md) | Material Editor、Niagara、PCG、Substrate | Unreal 材质、Niagara VFX、程序化内容生成 |
| 🌐 [Unreal Multiplayer Architect](game-development（游戏开发）/unreal-engine（虚幻引擎开发）/unreal-multiplayer-architect（Unreal%20多人游戏架构师）.md) | Actor replication、GameMode/GameState 层级、专用服务器 | Unreal 在线游戏、复制图、服务器权威的 Unreal |
| 🗺️ [Unreal World Builder](game-development（游戏开发）/unreal-engine（虚幻引擎开发）/unreal-world-builder（虚幻引擎世界构建师）.md) | World Partition、Landscape、HLOD、LWC | 大型开放世界 Unreal 关卡、流式系统、规模化地形 |

#### Godot

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 📜 [Godot Gameplay Scripter](game-development（游戏开发）/godot（Godot开发）/godot-gameplay-scripter（Godot%20游戏脚本工程师）.md) | GDScript 2.0、signals、composition、静态类型 | Godot 游戏玩法系统、场景组合、注重性能的 GDScript |
| 🌐 [Godot Multiplayer Engineer](game-development（游戏开发）/godot（Godot开发）/godot-multiplayer-engineer（Godot%20多人游戏工程师）.md) | MultiplayerAPI、ENet/WebRTC、RPC、权威模型 | 在线 Godot 游戏、场景复制、服务器权威的 Godot |
| ✨ [Godot Shader Developer](game-development（游戏开发）/godot（Godot开发）/godot-shader-developer（Godot%20着色器开发者）.md) | Godot 着色语言、VisualShader、RenderingDevice | 自定义 Godot 材质、2D/3D 效果、后处理、计算着色器 |

#### Blender

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🧩 [Blender Addon Engineer](game-development（游戏开发）/blender（Blender开发）/blender-addon-engineer（Blender%20插件工程师）.md) | Blender Python (`bpy`)、自定义操作符/面板、资源验证器、导出器、流水线自动化 | 构建 Blender 插件、资源准备工具、导出工作流和 DCC 流水线自动化 |

#### Roblox Studio

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| ⚙️ [Roblox Systems Scripter](game-development（游戏开发）/roblox-studio（Roblox%20Studio开发）/roblox-systems-scripter（Roblox%20系统脚本工程师）.md) | Luau、RemoteEvents/Functions、DataStore、服务器权威模块架构 | 构建安全的 Roblox 游戏系统、客户端-服务器通信、数据持久化 |
| 🎯 [Roblox Experience Designer](game-development（游戏开发）/roblox-studio（Roblox%20Studio开发）/roblox-experience-designer（Roblox%20体验设计师）.md) | 参与循环、变现、D1/D7 留存、引导流程 | 设计 Roblox 游戏循环、Game Pass、每日奖励、玩家留存 |
| 👗 [Roblox Avatar Creator](game-development（游戏开发）/roblox-studio（Roblox%20Studio开发）/roblox-avatar-creator（Roblox%20虚拟形象创建者）.md) | UGC 流水线、配件绑定、Creator Marketplace 提交 | Roblox UGC 物品、HumanoidDescription 定制、游戏内虚拟形象商店 |

### 📚 学术分部

为世界构建、叙事和 narrative design 提供学术严谨性。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🌍 [Anthropologist](academic（学术）/academic-anthropologist（人类学家）.md) | 文化系统、亲属关系、仪式、信仰体系 | 设计内部逻辑自洽、文化一致的社会 |
| 🌐 [Geographer](academic（学术）/academic-geographer（地理学家）.md) | 自然/人文地理、气候、制图 | 构建地理上自洽、地形与聚落真实的世界 |
| 📚 [Historian](academic（学术）/academic-historian（历史学家）.md) | 历史分析、分期、物质文化 | 验证历史一致性，用真实的时代细节丰富设定 |
| 📜 [Narratologist](academic（学术）/academic-narratologist（叙事学家）.md) | 叙事理论、故事结构、人物弧光 | 用既有理论框架分析并改进故事结构 |
| 🧠 [Psychologist](academic（学术）/academic-psychologist（心理学家）.md) | 人格理论、动机、认知模式 | 构建基于研究、心理可信的角色 |
| 📊 [Statistician](academic（学术）/academic-statistician（统计学家）.md) | 统计推断与实验设计 | 假设检验、因果推断、抽样、严谨分析 |

---

### 🌍 GIS 分部

绘制地球、分析建成环境，并从地理空间数据中提取情报。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🧠 [Technical Consultant](gis（地理信息系统）/gis-technical-consultant（技术顾问）.md) | GIS 战略、差距分析、技术路线图、数字化转型 | 理解业务需求、选择合适的地理空间技术栈、规划多阶段 GIS 项目 |
| 🔧 [Solution Engineer](gis（地理信息系统）/gis-solution-engineer（解决方案工程师）.md) | Esri + FOSS4G 原型构建、PoC 交付、技术可行性 | 构建可运行 demo、验证技术路径、售前支持 |
| 🖥️ [GIS Analyst](gis（地理信息系统）/gis-analyst（GIS%20分析师）.md) | 制图、数据 QC、符号化、版式、空间查询 | 日常 GIS 运维、制作可发布地图、维护数据完整性 |
| 📦 [Spatial Data Engineer](gis（地理信息系统）/gis-spatial-data-engineer（空间数据工程师）.md) | 地理空间 ETL、格式转换、CRS 重投影、自动化流水线 | 从任何来源摄取杂乱数据、构建可重复的数据转换流水线 |
| ⚙️ [Geoprocessing Specialist](gis（地理信息系统）/gis-geoprocessing-specialist（地理处理专家）.md) | ArcPy、Python Toolbox (.pyt)、Model Builder、批处理自动化 | 自动化重复 GIS 工作流、构建自定义地理处理工具 |
| ✅ [GIS QA Engineer](gis（地理信息系统）/gis-qa-engineer（GIS%20质量保证工程师）.md) | 拓扑验证、元数据审计、CRS 一致性、精度评估 | 数据发布前的质量门禁、合规验证、数据完整性审计 |
| 🤖 [GeoAI/ML Engineer](gis（地理信息系统）/gis-geoai-ml-engineer（GeoAI与ML%20工程师）.md) | 特征提取、目标检测、语义分割、地表覆盖分类 | 从影像中提取建筑/道路/车辆、变化检测、环境监测 |
| 🏗️ [BIM/GIS Specialist](gis（地理信息系统）/gis-bim-specialist（BIM与GIS%20专家）.md) | Revit/IFC 到 GIS、室内地图、数字孪生架构、设施管理 | 智慧校园、机场数字孪生、室内导航、楼宇运营 |
| 🏔️ [3D & Scene Developer](gis（地理信息系统）/gis-3d-scene-developer（3D%20与%20场景开发者）.md) | Cesium、ArcGIS Scene Viewer、3D Tiles、点云、地形可视化 | 3D 城市场景、地形飞越、点云 Web 查看器、OAuth 保护的场景共享 |
| 📊 [Spatial Data Scientist](gis（地理信息系统）/gis-spatial-data-scientist（空间数据科学家）.md) | 空间统计、聚类、回归、插值、点格局分析 | 热点检测、空间建模、预测分析、研究级分析 |
| 🛸 [Drone/Reality Mapping](gis（地理信息系统）/gis-drone-reality-mapping（无人机与实景建模专家）.md) | 摄影测量、正射镶嵌图、DTM/DSM、点云分类、三维网格 | 无人机测绘处理、现实采集、施工监测、环境制图 |
| 🌐 [Web GIS Developer](gis（地理信息系统）/gis-web-gis-developer（Web%20GIS%20开发者）.md) | MapLibre GL JS、ArcGIS JS API、Leaflet、实时仪表板、REST APIs | 构建交互式 Web 地图、运营仪表板、实时数据可视化 |
| 🎨 [Cartography Designer](gis（地理信息系统）/gis-cartography-designer（制图设计师）.md) | 色彩理论、排版、底图设计、视觉层级、印刷与网页美学 | 让地图美观且易读、适合色盲的配色方案、专业地图版式 |

---

### 🏥 医疗分部

为受监管的临床与主权医疗场景构建 AI agents。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🩺 [Clinical Evidence Agent](healthcare（医疗健康）/healthcare-clinical-evidence-agent（临床证据代理）.md) | 证据标准、已验证与未验证声明、诊断权威边界 | 在不越过诊断权限的前提下，可信地进行临床表述 |
| 🌍 [Sovereign Health Systems Agent](healthcare（医疗健康）/healthcare-sovereign-health-systems-agent（主权卫生系统代理）.md) | 政府卫生使命、UHC 政策、新兴市场部署 | 位于国家卫生基础设施与主权卫生政策交汇处的医疗科技团队 |
| 🧭 [Healthcare Innovation Strategist](healthcare（医疗健康）/healthcare-innovation-strategist（医疗创新战略师）.md) | 面向医疗创始人的叙事架构，覆盖投资者、监管、主权与临床受众 | 需要将临床和财务复杂性转化为能够推动资本并建立信任的语言的医疗创始人 |

---

### 🔍 研究分部

寻找、评估并综合既有证据，而不是生成新的原始数据。

| Agent | 专长 | 何时使用 |
|-------|------|----------|
| 🔍 [Research Synthesist](research（研究）/research-synthesist（研究综合分析师）.md) | 文献综述、来源评估、引文追溯、证据综合 | 把零散来源整理成结构化、权重诚实的证据地图，标明证据实际支持什么 |

---

## 🎯 真实世界使用场景

### 场景 1：构建创业 MVP

**你的团队**：
1. 🎨 **Frontend Developer** - 构建 React 应用
2. 🏗️ **Backend Architect** - 设计 API 与数据库
3. 🚀 **Growth Hacker** - 规划用户获取
4. ⚡ **Rapid Prototyper** - 快速迭代周期
5. 🔍 **Reality Checker** - 在发布前确保质量

**结果**：在每个阶段都以专业能力更快交付。

---

### 场景 2：营销活动上线

**你的团队**：
1. 📝 **Content Creator** - 开发活动内容
2. 🐦 **Twitter Engager** - Twitter 策略与执行
3. 📸 **Instagram Curator** - 视觉内容与故事
4. 🤝 **Reddit Community Builder** - 真实的社区互动
5. 📊 **Analytics Reporter** - 跟踪并优化表现

**结果**：具有平台专长的多渠道协同活动。

---

### 场景 3：企业功能开发

**你的团队**：
1. 👔 **Senior Project Manager** - 范围与任务规划
2. 💎 **Senior Developer** - 复杂实现
3. 🎨 **UI Designer** - 设计系统与组件
4. 🧪 **Experiment Tracker** - A/B 测试规划
5. 📸 **Evidence Collector** - 质量验证
6. 🔍 **Reality Checker** - 生产就绪检查

**结果**：带有质量门控与文档的企业级交付。

---

### 场景 4：付费媒体账户接手

**你的团队**：

1. 📋 **Paid Media Auditor** - 全面账户评估
2. 📡 **Tracking & Measurement Specialist** - 验证转化追踪准确性
3. 💰 **PPC Campaign Strategist** - 重构账户架构
4. 🔍 **Search Query Analyst** - 清理搜索词带来的浪费支出
5. ✍️ **Ad Creative Strategist** - 刷新所有广告文案与扩展
6. 📊 **Analytics Reporter**（Support Division）- 构建报告仪表板

**结果**：系统化账户接手，在前 30 天内完成追踪验证、浪费消除、结构优化和创意刷新。

---

### 场景 5：完整的 Agency 产品发现

**你的团队**：全部 8 个分部并行围绕同一使命协作。

请参见 **[Nexus Spatial Discovery Exercise](examples（示例）/nexus-spatial-discovery（NEXUS空间探索）.md)** —— 一个完整示例，其中 8 个 agent（Product Trend Researcher、Backend Architect、Brand Guardian、Growth Hacker、Support Responder、UX Researcher、Project Shepherd 和 XR Interface Architect）同时部署，以评估一个软件机会，并产出统一的产品计划，涵盖市场验证、技术架构、品牌战略、go-to-market、支持系统、UX 研究、项目执行和空间 UI 设计。

**结果**：在单次会话中产出全面的跨职能产品蓝图。[更多示例](examples（示例）/)。

---

### 场景 6：智慧校园数字孪生

**你的团队**：

1. 🧠 **Technical Consultant** - 定义数字孪生策略：建筑用 BIM、校园用 GIS、实时用 IoT
2. 🏗️ **BIM/GIS Specialist** - 将 Revit 建筑模型转换为 GIS 场景图层，设计室内楼层平面
3. 🛸 **Drone/Reality Mapping** - 飞越校园，生成正射镶嵌图和 3D 网格作为环境背景
4. 🌐 **Web GIS Developer** - 使用 MapLibre、建筑图层和房间查找器构建校园仪表板
5. 🏔️ **3D & Scene Developer** - 创建包含地形、建筑和飞越导览的沉浸式 3D 场景
6. 🤖 **GeoAI/ML Engineer** - 从无人机影像中提取建筑轮廓和树冠
7. ✅ **GIS QA Engineer** - 验证数据精度、检查拓扑、确认 CRS 一致性

**结果**：一个融合 BIM 细节、无人机现实采集、3D 可视化与 Web 可访问性的校园数字孪生——由协调一致的专家通过单一流水线交付。

---

## 🤝 贡献

我们欢迎贡献！以下是你可以提供帮助的方式：

### 添加新的 Agent

1. Fork 该仓库
2. 在合适的类别中创建新的 agent 文件
3. 遵循 agent 模板结构：
   - 含 name、description、color 的 Frontmatter
   - Identity & Memory 部分
   - Core Mission
   - Critical Rules（领域相关）
   - 带示例的 Technical Deliverables
   - Workflow Process
   - Success Metrics
4. 提交包含你 agent 的 PR

### 改进现有 Agents

- 添加真实世界示例
- 增强代码样例
- 更新成功指标
- 改进工作流

### 分享你的成功故事

你是否成功使用过这些 agents？在 [Discussions](https://github.com/msitarzewski/agency-agents/discussions) 中分享你的故事！

---

## 📖 Agent 设计哲学

每个 agent 都按以下原则设计：

1. **🎭 强个性**：不是通用模板——而是真实的角色与声音
2. **📋 清晰交付物**：具体输出，而不是模糊建议
3. **✅ 成功指标**：可衡量的结果与质量标准
4. **🔄 成熟工作流**：行之有效的逐步流程
5. **💡 学习记忆**：模式识别与持续改进

---

## 🎁 这有什么特别之处？

### 与通用 AI 提示词相比：
- ❌ 通用的“把自己当作开发者”提示词
- ✅ 深度专业化，带有个性与流程

### 与提示词库相比：
- ❌ 一次性的提示词集合
- ✅ 具备工作流与交付物的完整 agent 系统

### 与 AI 工具相比：
- ❌ 无法自定义的黑盒工具
- ✅ 透明、可 fork、可适配的 agent 个性

---

## 🎨 Agent 个性亮点

> "我不只是测试你的代码——我默认会找出 3-5 个问题，并且对所有内容都要求视觉证据。"
>
> -- **Evidence Collector**（Testing Division）

> "你不是在 Reddit 上做营销——你是在成为一名有价值的社区成员，而恰好代表着一个品牌。"
>
> -- **Reddit Community Builder**（Marketing Division）

> "每一个俏皮元素都必须服务于功能或情绪目的。设计愉悦感，但要增强而不是分散注意力。"
>
> -- **Whimsy Injector**（Design Division）

> "让我加一个庆祝动画，把任务完成焦虑降低 40%"
>
> -- **Whimsy Injector**（在一次 UX 评审中）

---

## 📊 统计

- 🎭 **230+ 个专业 agents**，覆盖每个分部
- 📝 **10,000+ 行** 个性、流程与代码示例
- ⏱️ **数月迭代**，来自真实世界使用
- 🌟 **经过实战检验**
- 💬 **Reddit 首 12 小时内收到 50+ 请求**

---

## 🔌 多工具集成

The Agency 与 Claude Code 原生兼容，并提供转换与安装脚本，因此你可以在所有主流 agentic coding 工具中使用同一套 agents。

### 支持的工具

- **[Claude Code](https://claude.ai/code)** — 原生 `.md` agents，无需转换 → `~/.claude/agents/`
- **[GitHub Copilot](https://github.com/copilot)** — 原生 `.md` agents，无需转换 → `~/.github/agents/` + `~/.copilot/agents/`
- **[Antigravity](https://github.com/google-gemini/antigravity)** — 每个 agent 一个 `SKILL.md` → `~/.gemini/config/skills/`
- **[Gemini CLI](https://github.com/google-gemini/gemini-cli)** -- `.md` agent 文件 -> `~/.gemini/agents/`
- **[OpenCode](https://opencode.ai)** — `.md` agent 文件 → `.opencode/agents/`
- **[Cursor](https://cursor.sh)** — `.mdc` 规则文件 → `.cursor/rules/`
- **[Aider](https://aider.chat)** — 单一 `CONVENTIONS.md` → `./CONVENTIONS.md`
- **[Windsurf](https://codeium.com/windsurf)** — 单一 `.windsurfrules` → `./.windsurfrules`
- **[OpenClaw](https://github.com/openclaw/openclaw)** — 每个 agent 一个 `SOUL.md` + `AGENTS.md` + `IDENTITY.md`
- **[Qwen Code](https://github.com/QwenLM/qwen-code)** — `.md` SubAgent 文件 → `~/.qwen/agents/`
- **[Kimi Code](https://github.com/MoonshotAI/kimi-cli)** — YAML agent 规范 → `~/.config/kimi/agents/`
- **[Codex](https://developers.openai.com/codex/overview)** — TOML 自定义 agents → `~/.codex/agents/`
- **Osaurus** -- `SKILL.md` skills -> `~/.osaurus/skills/`
- **[Hermes](integrations（集成）/hermes（Hermes集成）/README（集成说明）.md)** -- lazy-router 插件 -> `~/.hermes/plugins/`

---

### ⚡ 快速安装

**步骤 1 -- 生成集成文件：**
```bash
./scripts/convert.sh
# 更快（并行，输出顺序可能变化）：./scripts/convert.sh --parallel
```

**步骤 2 -- 安装（交互式，自动检测你的工具）：**
```bash
./scripts/install.sh
# 更快（并行，输出顺序可能变化）：./scripts/install.sh --no-interactive --parallel
```

安装器会扫描系统中已安装的工具，显示一个复选框界面，并让你精确选择要安装的内容：

```
  +------------------------------------------------+
  |   The Agency -- Tool Installer                 |
  +------------------------------------------------+

  System scan: [*] = detected on this machine

  [x]  1)  [*]  Claude Code     (claude.ai/code)
  [x]  2)  [*]  Copilot         (~/.github + ~/.copilot)
  [x]  3)  [*]  Antigravity     (~/.gemini/antigravity)
  [ ]  4)  [ ]  Gemini CLI      (~/.gemini/agents)
  [ ]  5)  [ ]  OpenCode        (opencode.ai)
  [ ]  6)  [ ]  OpenClaw        (~/.openclaw/agency-agents)
  [x]  7)  [*]  Cursor          (.cursor/rules)
  [ ]  8)  [ ]  Aider           (CONVENTIONS.md)
  [ ]  9)  [ ]  Windsurf        (.windsurfrules)
  [ ] 10)  [ ]  Qwen Code       (~/.qwen/agents)
  [ ] 11)  [ ]  Kimi Code       (~/.config/kimi/agents)
  [ ] 12)  [ ]  Codex           (~/.codex/agents)
  [ ] 13)  [ ]  Osaurus         (~/.osaurus/skills)
  [ ] 14)  [ ]  Hermes          (~/.hermes/plugins)

  [1-14] toggle   [a] all   [n] none   [d] detected
  [Enter] install   [q] quit
```

**或者直接安装某个特定工具：**
```bash
./scripts/install.sh --tool cursor
./scripts/install.sh --tool opencode
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes
```

**非交互式（CI/脚本）：**
```bash
./scripts/install.sh --no-interactive --tool all
```

**更快的运行方式（并行）** — 在多核机器上，使用 `--parallel` 让每个工具并行处理。不同工具之间的输出顺序是非确定性的。交互式与非交互式安装都适用：例如 `./scripts/install.sh --interactive --parallel`（先选择工具，再并行安装）或 `./scripts/install.sh --no-interactive --parallel`。作业数量默认使用 `nproc`（Linux）、`sysctl -n hw.ncpu`（macOS）或 4；可用 `--jobs N` 覆盖。

```bash
./scripts/convert.sh --parallel                    # 并行转换所有工具
./scripts/convert.sh --parallel --jobs 8           # 限制并行作业数
./scripts/install.sh --no-interactive --parallel   # 并行安装所有检测到的工具
./scripts/install.sh --interactive --parallel      # 选择工具后并行安装
./scripts/install.sh --no-interactive --parallel --jobs 4
```

---

### 工具特定说明

<details>
<summary><strong>Claude Code</strong></summary>

Agents 会直接从仓库复制到 `~/.claude/agents/` -- 无需转换。

```bash
./scripts/install.sh --tool claude-code
```

然后在 Claude Code 中激活：
```
Use the Frontend Developer agent to review this component.
```

详见 [integrations/claude-code/README.md](integrations（集成）/claude-code（Claude%20Code集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Agents 会直接从仓库复制到 `~/.github/agents/` 和 `~/.copilot/agents/` -- 无需转换。

```bash
./scripts/install.sh --tool copilot
```

然后在 GitHub Copilot 中激活：
```
Use the Frontend Developer agent to review this component.
```

详见 [integrations/github-copilot/README.md](integrations（集成）/github-copilot（GitHub%20Copilot集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>Antigravity (Gemini)</strong></summary>

每个 agent 都会成为 `~/.gemini/config/skills/agency-<slug>/` 中的一个 skill。

```bash
./scripts/install.sh --tool antigravity
```

在带有 Antigravity 的 Gemini 中激活：
```
@agency-frontend-developer review this React component
```

详见 [integrations/antigravity/README.md](integrations（集成）/antigravity（Antigravity集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>Gemini CLI</strong></summary>

会安装为 Gemini CLI subagents。
在全新克隆后，请先生成 Gemini agent 文件，再运行安装器。

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

详见 [integrations/gemini-cli/README.md](integrations（集成）/gemini-cli（Gemini%20CLI集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>OpenCode</strong></summary>

Agents 会放置在项目根目录下的 `.opencode/agents/` 中（项目级作用域）。

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

或者全局安装：
```bash
mkdir -p ~/.config/opencode/agents
cp integrations/opencode/agents/*.md ~/.config/opencode/agents/
```

在 OpenCode 中激活：
```
@backend-architect design this API.
```

详见 [integrations/opencode/README.md](integrations（集成）/opencode（OpenCode集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>Cursor</strong></summary>

每个 agent 都会成为项目中 `.cursor/rules/` 里的一个 `.mdc` 规则文件。

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

当 Cursor 在项目中检测到这些规则时，会自动应用。你也可以显式引用它们：
```
Use the @security-engineer rules to review this code.
```

详见 [integrations/cursor/README.md](integrations（集成）/cursor（Cursor集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>Aider</strong></summary>

所有 agents 会被编译成一个单独的 `CONVENTIONS.md` 文件，Aider 会自动读取它。

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

然后在你的 Aider 会话中引用 agents：
```
Use the Frontend Developer agent to refactor this component.
```

详见 [integrations/aider/README.md](integrations（集成）/aider（Aider集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>Windsurf</strong></summary>

所有 agents 会被编译到项目根目录下的 `.windsurfrules` 中。

```bash
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

在 Windsurf 的 Cascade 中引用 agents：
```
Use the Reality Checker agent to verify this is production ready.
```

详见 [integrations/windsurf/README.md](integrations（集成）/windsurf（Windsurf集成）/README（集成说明）.md)。
</details>

<details>
<summary><strong>OpenClaw</strong></summary>

每个 agent 都会成为 `~/.openclaw/agency-agents/` 中带有 `SOUL.md`、`AGENTS.md` 和 `IDENTITY.md` 的一个 workspace。

```bash
./scripts/convert.sh --tool openclaw
./scripts/install.sh --tool openclaw
```

如果 `openclaw` CLI 可用，安装器会自动注册每个 workspace。
安装后运行 `openclaw gateway restart`，以激活新 agents。

详见 [integrations/openclaw/README.md](integrations（集成）/openclaw（OpenClaw集成）/README（集成说明）.md)。

</details>

<details>
<summary><strong>Qwen Code</strong></summary>

SubAgents 会安装到项目根目录下的 `.qwen/agents/` 中（项目级作用域）。

```bash
# 转换并安装（在项目根目录运行）
cd /your/project
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

**在 Qwen Code 中的使用方式：**
- 按名称引用：`Use the frontend-developer agent to review this component`
- 或者让 Qwen 根据任务上下文自动委派
- 在交互模式下通过 `/agents` 命令管理

> 📚 [Qwen SubAgents 文档](https://qwenlm.github.io/qwen-code-docs/en/users/features/sub-agents/)

</details>

<details>
<summary><strong>Kimi Code</strong></summary>

Agents 会被转换为 Kimi Code CLI 格式（YAML + system prompt），并安装到 `~/.config/kimi/agents/`。

```bash
# 转换并安装
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

**在 Kimi Code 中的使用方式：**
```bash
# 使用一个 agent
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml

# 在项目中
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "Review this React component"
```

详见 [integrations/kimi/README.md](integrations（集成）/kimi（Kimi%20Code集成）/README（集成说明）.md)。

</details>

<details>
<summary><strong>Codex</strong></summary>

每个 agent 都会被转换为一个 Codex 自定义 agent TOML 文件，并安装到 `~/.codex/agents/`。

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

然后在 Codex 中按名称引用这个自定义 agent：
```
Use the Frontend Developer agent to review this component.
```

详见 [integrations/codex/README.md](integrations（集成）/codex（Codex集成）/README（集成说明）.md)。
</details>

---

### 变更后重新生成

当你添加新 agents 或编辑现有 agents 时，请重新生成所有集成文件：

```bash
./scripts/convert.sh                    # 重新生成全部（串行）
./scripts/convert.sh --parallel         # 并行重新生成全部（更快）
./scripts/convert.sh --tool codex       # 只重新生成一个工具
./scripts/convert.sh --tool cursor      # 只重新生成一个工具
```

---

## 🗺️ 路线图

- [ ] 交互式 agent 选择器 Web 工具
- [x] 多 agent 工作流示例 -- 见 [示例/](examples（示例）/)
- [x] 多工具集成脚本（Claude Code、GitHub Copilot、Antigravity、Gemini CLI、OpenCode、OpenClaw、Cursor、Aider、Windsurf、Qwen Code、Kimi Code、Codex、Osaurus、Hermes）
- [ ] 关于 agent 设计的视频教程
- [ ] 社区 agent 市场
- [ ] 用于项目匹配的 agent “性格测验”
- [ ] “本周 Agent” 展示系列

---

## 🌐 社区翻译与本地化

由社区维护的翻译与地区化改编版本。这些项目由各自独立维护——请查看各仓库以了解覆盖范围与版本兼容性。

| 语言 | 维护者 | 链接 | 说明 |
|----------|-----------|------|-------|
| 🇨🇳 简体中文 (zh-CN) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) | 141 个翻译 agent + 46 个中国市场原创 agent |
| 🇨🇳 简体中文 (zh-CN) | [@dsclca12](https://github.com/dsclca12) | [agent-teams](https://github.com/dsclca12/agent-teams) | 独立翻译，包含 Bilibili、微信、小红书本地化 |
| 🇧🇷 Português brasileiro (pt-BR) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-pt-BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | 翻译了 184 个上游 agents；欢迎巴西市场 PR |
| 🇷🇺 Русский (ru) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ru](https://github.com/jnMetaCode/agency-agents-ru) | 翻译了 184 个上游 agents；欢迎俄罗斯市场 PR |
| 🇮🇩 Bahasa Indonesia (id) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-id](https://github.com/jnMetaCode/agency-agents-id) | 翻译了 184 个上游 agents；欢迎印度尼西亚市场 PR |
| 🇸🇦 العربية (ar) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ar](https://github.com/jnMetaCode/agency-agents-ar) | 翻译了 184 个上游 agents；欢迎阿拉伯市场 PR |
| 🇰🇷 한국어 (ko) | [@jnMetaCode](https://github.com/jnMetaCode) | [agency-agents-ko](https://github.com/jnMetaCode/agency-agents-ko) | 184 个上游 agents 已完整翻译；欢迎韩国特定 PR |
| 🇯🇵 日本語 (ja-JP) | [@sscodeai](https://github.com/sscodeai) | [agency-agents-ja](https://github.com/sscodeai/agency-agents-ja) | 281 个日本本地化 agents + 97 个日本市场原创 agents + 27 个工作流 |
| 🇻🇳 Tiếng Việt (vi-VN) | [@rodonguyen](https://github.com/rodonguyen) | [agency-agents](https://github.com/rodonguyen/agency-agents) | 越南语入门本地化，重点覆盖 README、快速开始和高频文档 |

想添加一种翻译？请打开一个 issue，我们会把它链接在这里。

---

## 🔗 相关资源

- [awesome-openclaw-agents](https://github.com/mergisi/awesome-openclaw-agents) — 社区维护的 OpenClaw agent 集合（源自本仓库）

---

## 📜 许可证

MIT License - 可自由使用，商业或个人用途均可。欢迎署名，但不是必须。

---

## 🙏 致谢

最初只是 Reddit 上关于 AI agent 专业化的一个讨论串，如今已经成长为一件令人惊叹的事情——**跨越每个分部的 230+ 个 agents**，并得到了来自世界各地贡献者社区的支持。本仓库中的每一个 agent 都存在，因为有人认真地撰写、测试并分享了它。

感谢所有提交 PR、创建 issue、发起 Discussion，或只是尝试某个 agent 并告诉我们哪些有效的人——谢谢你们。你们就是 The Agency 不断变得更好的原因。

---

## 💬 社区

- **GitHub Discussions**: [分享你的成功故事](https://github.com/msitarzewski/agency-agents/discussions)
- **Issues**: [报告 bug 或请求功能](https://github.com/msitarzewski/agency-agents/issues)
- **Reddit**: 加入 r/ClaudeAI 上的讨论
- **Twitter/X**: 使用 #TheAgency 分享

---

## 🚀 开始使用

1. **浏览** 上面的 agents，为你的需求找到专家
2. **复制** 这些 agents 到 `~/.claude/agents/` 以集成 Claude Code
3. **激活** agents：在 Claude 对话中引用它们
4. **自定义** agents 的个性与工作流，以适配你的具体需求
5. **分享** 你的成果，并回馈社区

---

<div align="center">

**🎭 The Agency：你的 AI 梦之队正在等待 🎭**

[⭐ 给这个仓库点星](https://github.com/msitarzewski/agency-agents) • [🍴 Fork 它](https://github.com/msitarzewski/agency-agents/fork) • [🐛 报告问题](https://github.com/msitarzewski/agency-agents/issues) • [❤️ 赞助](https://github.com/sponsors/msitarzewski)

由社区制作，服务社区，满怀 ❤️

</div>
