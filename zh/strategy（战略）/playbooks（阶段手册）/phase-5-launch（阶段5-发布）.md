# 🚀 第 5 阶段 Playbook — 发布与增长

> **持续时间**：2-4 周（T-7 至 T+14） | **代理**：12 | **关卡守门人**：Studio Producer + Analytics Reporter

---

## 目标

协调所有渠道同时进行上市执行。在发布时产生最大影响。每个营销代理协同发力，同时工程团队确保稳定性。

## 前置条件

- [ ] 第 4 阶段质量关卡已通过（Reality Checker 就绪判定）
- [ ] 第 4 阶段交接包已接收
- [ ] 生产部署计划已批准
- [ ] 营销内容管道已就绪（来自第 3 阶段轨道 B）

## 发布时间线

### T-7：发布前一周

#### 内容与活动准备（并行）

```
激活 Content Creator：
- 最终定稿所有发布内容（博客文章、落地页、邮件序列）
- 在发布平台中排队内容
- 为预期问题准备回复模板
- 创建发布日实时内容计划

激活 Social Media Strategist：
- 最终定稿跨平台活动素材
- 安排发布前的预告内容
- 协调 KOL 合作
- 准备平台特定内容变体

激活 Growth Hacker：
- 激活病毒传播机制（推荐码、分享激励）
- 配置增长实验跟踪
- 设置漏斗分析
- 准备获客渠道预算

激活 App Store Optimizer（如为移动端）：
- 最终定稿应用商店列表（标题、描述、关键词、截图）
- 提交应用审核（如适用）
- 准备发布日 ASO 调整
- 配置应用内评价提示
```

#### 技术准备（并行）

```
激活 DevOps Automator：
- 准备蓝绿部署
- 验证回滚程序
- 配置功能标志以支持渐进发布
- 端到端测试部署管道

激活 Infrastructure Maintainer：
- 配置自动扩缩以应对 10 倍预期流量
- 验证监控和告警阈值
- 测试灾难恢复程序
- 准备事件响应 runbook

激活 Project Shepherd：
- 向所有代理分发发布检查清单
- 确认所有依赖关系已解决
- 设置发布日沟通渠道
- 向利益相关方简报发布计划
```

### T-1：发布前夕

```
最终检查清单（Project Shepherd 协调）：

技术：
☐ 蓝绿部署已测试
☐ 回滚程序已验证
☐ 自动扩缩已配置
☐ 监控仪表盘已上线
☐ 事件响应团队待命
☐ 功能标志已配置

内容：
☐ 所有内容已排队并安排
☐ 邮件序列已激活
☐ 社交媒体帖子已安排
☐ 博客文章准备发布
☐ 新闻材料已分发

营销：
☐ 病毒传播机制已测试
☐ 推荐系统可操作
☐ 分析跟踪已验证
☐ 广告活动准备激活
☐ 社区互动计划就绪

支持：
☐ 支持团队已简报
☐ FAQ 和帮助文档已发布
☐ 升级程序已确认
☐ 反馈收集已激活
```

### T-0：发布日

#### 第 0 小时：部署

```
激活 DevOps Automator：
1. 执行到生产的蓝绿部署
2. 对所有服务运行健康检查
3. 验证数据库迁移已完成
4. 确认所有端点响应
5. 将流量切换到新部署
6. 监控错误率 15 分钟
7. 确认：部署成功 或 回滚

激活 Infrastructure Maintainer：
1. 实时监控所有系统指标
2. 关注流量峰值和扩缩事件
3. 跟踪错误率和响应时间
4. 任何阈值突破时告警
5. 确认：系统稳定
```

#### 第 1-2 小时：营销激活

```
激活 Twitter Engager：
- 发布发布主题帖
- 与早期回应互动
- 监控品牌提及
- 放大积极反应
- 实时参与对话

激活 Reddit Community Builder：
- 在相关 subreddits 发布真实的发布公告
- 与评论互动（价值优先，而非推广）
- 监控社区情绪
- 回复技术问题

激活 Instagram Curator：
- 发布发布视觉内容
- 产品演示 Stories
- 与早期关注者互动
- 与其他渠道交叉推广

激活 TikTok Strategist：
- 发布发布视频
- 监控病毒传播潜力
- 与评论互动
- 根据早期表现调整内容
```

#### 第 2-8 小时：监控与响应

```
激活 Support Responder：
- 处理传入的用户询问
- 记录常见问题
- 将技术问题升级给工程团队
- 收集早期用户反馈

激活 Analytics Reporter：
- 实时指标仪表盘
- 每小时流量和转化报告
- 渠道归因跟踪
- 用户行为流程分析

激活 Feedback Synthesizer：
- 监控所有反馈渠道
- 分类传入的反馈
- 识别关键问题
- 优先排序用户报告的问题
```

### T+1 至 T+7：发布后一周

```
每日节奏：

上午：
├── Analytics Reporter → 每日指标报告
├── Feedback Synthesizer → 反馈摘要
├── Infrastructure Maintainer → 系统健康报告
└── Growth Hacker → 渠道表现分析

下午：
├── Content Creator → 基于反响的响应内容
├── Social Media Strategist → 互动优化
├── Experiment Tracker → 发布 A/B 测试结果
└── Support Responder → 问题解决摘要

晚上：
├── Executive Summary Generator → 每日利益相关方简报
├── Project Shepherd → 跨团队协调
└── DevOps Automator → 热修复部署（如需）
```

### T+7 至 T+14：优化周

```
激活 Growth Hacker：
- 分析首周获客数据
- 基于数据优化转化漏斗
- 扩大赢利渠道，削减亏损渠道
- 基于 K 因子数据优化病毒传播机制

激活 Analytics Reporter：
- 第 1 周综合分析
- 发布用户的群组分析
- 留存曲线分析
- 收入/互动指标

激活 Experiment Tracker：
- 启动系统性 A/B 测试
- 测试入门引导变体
- 测试定价/套餐（如适用）
- 测试功能发现流程

激活 Executive Summary Generator：
- 第 1 周执行摘要（SCQA 格式）
- 关键指标 vs 目标
- 第 2 周及之后的建议
- 资源重新分配建议
```

## 质量关卡检查清单

| # | 标准 | 证据来源 | 状态 |
|---|-----------|----------------|--------|
| 1 | 部署成功（零停机） | DevOps Automator 部署日志 | ☐ |
| 2 | 系统稳定（48 小时内无 P0/P1） | Infrastructure Maintainer 监控 | ☐ |
| 3 | 用户获客渠道活跃 | Analytics Reporter 仪表盘 | ☐ |
| 4 | 反馈循环可操作 | Feedback Synthesizer 报告 | ☐ |
| 5 | 利益相关方已知情 | Executive Summary Generator 输出 | ☐ |
| 6 | 支持运营正常 | Support Responder 指标 | ☐ |
| 7 | 增长指标跟踪中 | Growth Hacker 渠道报告 | ☐ |

## 关卡决策

**双重签署**：Studio Producer（战略） + Analytics Reporter（数据）

- **稳定**：产品已发布，系统稳定，增长活跃 → 激活第 6 阶段
- **严重**：需要立即工程响应的重大问题 → 热修复周期
- **回滚**：根本性问题 → 回滚部署，返回到第 4 阶段

## 交接给第 6 阶段

```markdown
## 第 5 阶段 → 第 6 阶段交接包

### 给持续运营：
- 发布指标基线（Analytics Reporter）
- 用户反馈主题（Feedback Synthesizer）
- 系统性能基线（Infrastructure Maintainer）
- 增长渠道表现（Growth Hacker）
- 支持问题模式（Support Responder）

### 给持续改进：
- A/B 测试结果和学习（Experiment Tracker）
- 流程改进建议（Workflow Optimizer）
- 财务表现 vs 预测（Finance Tracker）
- 合规监控状态（Legal Compliance Checker）

### 已建立的运营节奏：
- 每日：系统监控、支持、分析
- 每周：分析报告、反馈综合、冲刺规划
- 每月：执行摘要、财务审查、合规检查
- 每季度：战略审查、流程优化、市场情报
```

---

*当产品已部署、系统稳定超过 48 小时、增长渠道活跃、且反馈循环可操作时，第 5 阶段即告完成。*
