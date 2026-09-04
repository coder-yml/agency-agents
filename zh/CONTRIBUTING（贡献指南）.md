# 🤝 为 The Agency 贡献

首先，感谢你考虑为 The Agency 做出贡献！正是像你这样的人，让这个 AI 代理集合对每个人都更有价值。

## 📋 目录

- [行为准则](#-行为准则)
- [我该如何贡献？](#-我该如何贡献)
- [代理设计指南](#-代理设计指南)
- [拉取请求流程](#-拉取请求流程)
- [风格指南](#-风格指南)
- [致谢](#-致谢)

---

## 📜 行为准则

本项目及其中所有参与者均受我们的行为准则约束。参与本项目即表示你应当遵守以下准则：

- **保持尊重**：尊重每个人。欢迎健康的讨论，但不容忍人身攻击。
- **保持包容**：欢迎并支持来自各种背景和身份的人。
- **保持协作**：我们共同创造的成果，比各自单独创造的更好。
- **保持专业**：让讨论聚焦于改进代理和社区。

---

## 🎯 我该如何贡献？

### 1. 创建一个新的代理

你有一个专门代理的想法吗？太好了！以下是添加一个代理的方法：

1. **Fork 仓库**
2. **选择合适的分区**——或者提议一个新的分区。分区是
   顶层代理目录（例如 `engineering/`、`security/`、`gis/`、`marketing/`、
   `finance/`……）；浏览它们，找到你的代理适合放置的位置。权威列表——
   包含标签、图标和颜色——位于仓库
   根目录的 [`divisions.json`](../divisions.json)，因此它始终是最新的。

   > **分区由 `divisions.json` 定义**（仓库根目录）——它是分区集合的单一事实来源，
   > 由 `scripts/check-divisions.sh` 在 CI 中验证。
   > **提议一个新分区**意味着：创建目录，将条目添加到
   > `divisions.json`（标签/图标/颜色），并将其添加到 `AGENT_DIRS` 中，
   > 同时修改 `scripts/convert.sh` 和 `scripts/lint-agents.sh`。检查会使构建失败，
   > 除非这些内容全部一致，并且该目录至少包含一个代理文件。
   >
   > 注意：`strategy/`（NEXUS playbooks/runbooks——不含代理 frontmatter）和
   > `integrations/`（由 `convert.sh` 按工具生成的输出）**不是**
   > 分区，绝不能添加到分区列表中。

3. **按照下面的模板创建你的代理文件**
4. **在真实场景中测试你的代理**
5. **提交包含你的代理的 Pull Request**

### 2. 改进现有代理

发现了让某个代理更好的方法？欢迎贡献：

- 添加真实世界的示例和用例
- 用现代模式增强代码示例
- 根据新的最佳实践更新工作流
- 添加成功指标和基准
- 修复拼写错误、提高清晰度、增强文档

### 3. 分享成功故事

已经成功使用了这些代理？分享你的故事：

- 在 [GitHub Discussions](https://github.com/msitarzewski/agency-agents/discussions) 发帖
- 为 README 添加一个案例研究
- 写一篇博客文章并链接它
- 制作一个视频教程

### 4. 报告问题

发现了问题？请告诉我们：

- 检查问题是否已经存在
- 提供清晰的复现步骤
- 包含与你的使用场景相关的上下文
- 如果你有想法，建议潜在解决方案

---

## 🎨 代理设计指南

### 代理文件结构

每个代理都应遵循以下结构：

```markdown
---
name: Agent Name
description: One-line description of the agent's specialty and focus
color: colorname or "#hexcode"
emoji: 🎯
vibe: One-line personality hook — what makes this agent memorable
services:                              # optional — only if the agent requires external services
  - name: Service Name
    url: https://service-url.com
    tier: free                         # free, freemium, or paid
---

# Agent Name

## 🧠 你的身份与记忆
- **Role**: Clear role description
- **Personality**: Personality traits and communication style
- **Memory**: What the agent remembers and learns
- **Experience**: Domain expertise and perspective

## 🎯 你的核心使命
- Primary responsibility 1 with clear deliverables
- Primary responsibility 2 with clear deliverables
- Primary responsibility 3 with clear deliverables
- **Default requirement**: Always-on best practices

## 🚨 你必须遵守的关键规则
Domain-specific rules and constraints that define the agent's approach

## 📋 你的技术交付物
Concrete examples of what the agent produces:
- Code samples
- Templates
- Frameworks
- Documents

## 🔄 你的工作流流程
Step-by-step process the agent follows:
1. Phase 1: Discovery and research
2. Phase 2: Planning and strategy
3. Phase 3: Execution and implementation
4. Phase 4: Review and optimization

## 💭 你的沟通风格
- How the agent communicates
- Example phrases and patterns
- Tone and approach

## 🔄 学习与记忆
What the agent learns from:
- Successful patterns
- Failed approaches
- User feedback
- Domain evolution

## 🎯 你的成功指标
Measurable outcomes:
- Quantitative metrics (with numbers)
- Qualitative indicators
- Performance benchmarks

## 🚀 高级能力
Advanced techniques and approaches the agent masters
```

### 代理结构

代理文件组织为两个语义组，它们映射到
OpenClaw 的 workspace 格式，并帮助其他工具解析你的代理：

#### Persona（代理是谁）
- **身份与记忆** — 角色、个性、背景
- **沟通风格** — 语气、声音、方法
- **关键规则** — 边界与约束

#### Operations（代理做什么）
- **核心使命** — 主要职责
- **技术交付物** — 具体输出和模板
- **工作流流程** — 分步骤方法
- **成功指标** — 可衡量的结果
- **高级能力** — 专门技术

不需要特殊格式——只需保持与 persona 相关的部分
（身份、沟通、规则）与运营
部分（使命、交付物、工作流、指标）分开分组即可。`convert.sh`
脚本使用这些章节标题自动将代理拆分为
特定工具格式。

### 代理设计原则

1. **🎭 强烈的个性**
   - 赋予代理独特的声音和性格
   - 不要只是“我是一个有帮助的助手”——要具体且令人难忘
   - 示例：“我默认找出 3-5 个问题，并要求视觉证据”（Evidence Collector）

2. **📋 清晰的交付物**
   - 提供具体的代码示例
   - 包括模板和框架
   - 展示真实输出，而不是模糊描述

3. **✅ 成功指标**
   - 包含具体、可衡量的指标
   - 示例：“在 3G 网络下页面加载时间低于 3 秒”
   - 示例：“各账号合计 10,000+ karma”

4. **🔄 经验证的工作流**
   - 分步骤流程
   - 经过真实世界测试的方法
   - 不是理论上的——要经过实战检验

5. **💡 学习记忆**
   - 代理识别哪些模式
   - 它如何随着时间改进
   - 它在会话之间记住什么

### 外部服务

当外部服务（API、平台、SaaS 工具）对代理功能至关重要时，
代理可以依赖这些服务。若是如此：

1. **在 frontmatter 中使用 `services` 字段声明依赖**
2. **代理必须能够独立成立**——去掉 API 调用后，
   其下仍应保留一个有用的人设、工作流和专业能力
3. **不要重复供应商文档**——引用它们，不要复述它们。
   代理文件应当读起来像一个代理，而不是入门指南
4. **优先选择有免费层级的服务**，这样贡献者可以测试代理

测试标准：*这个代理是为用户而写，还是为供应商而写？* 一个
通过服务解决用户问题的代理可以放在这里。一个披着代理外衣的
服务快速入门指南则不可以。

### 工具特定兼容性

**Qwen Code 兼容性**：代理正文支持 `${variable}` 模板语法，用于动态上下文（例如 `${project_name}`、`${task_description}`）。Qwen SubAgents 使用最小化 frontmatter：只需要 `name` 和 `description`；`color`、`emoji` 和 `version` 字段会被省略，因为 Qwen 不使用它们。

**Codex 兼容性**：Codex 自定义代理会生成独立的 TOML 文件。Codex 集成保持最小的 1:1 映射：`name` 和 `description` 从 frontmatter 复制，Markdown 正文变为 `developer_instructions`。诸如 `color`、`emoji`、`vibe` 以及其他不受支持的 frontmatter 字段等仅源元数据会被省略。

### 添加工具集成

想让 agency-agents 安装到一个新工具中（CLI、编辑器或代理运行时）吗？首先，**[打开一个 Discussion](https://github.com/msitarzewski/agency-agents/discussions)**——新的集成平台属于“先讨论再改”的变更（见下方的 PR 流程）。一旦达成一致，一个干净的集成通常很小——通常是 **~5 个文件，绝不是转换后的输出本身。** 刚合并的 Mistral Vibe 集成就是一个很好的可复制范例。

仓库根目录的 `tools.json` 是工具集合的单一事实来源，而 `scripts/check-tools.sh`（CI）会在以下任一部分不一致时使构建失败。运行它——它会指出每一个必须匹配的位置。

**检查清单：**

1. **`tools.json`**——添加一个条目，包含 `id`、`label`、`kebab`、`format`、`installKind`、`dest`，以及 detect/version/scope 和显示字段。若你的工具所渲染的文件与其他工具的字节级输出完全相同，请**复用现有的 `format`**（例如，消费 `SKILL.md` 的工具共享 `"format": "skill-md"`——无需新的渲染器）。将 `installKind` 设置为 `per-agent`、`roster` 或 `plugin`。除非 [app](https://github.com/msitarzewski/agency-agents-app) 为其提供品牌 SVG，否则将 `icon` 设为 `null`。
2. **`scripts/convert.sh`**——添加一个 `convert_<tool>()`（或复用共享的 `format` 渲染器），并将其接入工具列表和 `--help`。
3. **`scripts/install.sh`**——添加一个 `install_<tool>()`，并将其注册到 `ALL_TOOLS` 中，以及 detection/labeling 和 `--help`。
4. **`.gitignore`**——为你的工具在 `integrations/<tool>/` 下生成的输出添加一条规则。**这一步是必需的，而且很容易遗漏。** 转换后的代理/技能文件由 `convert.sh` 在本地生成，且**绝不会提交**（见下方“我们始终会关闭的事项”）——只有 `integrations/<tool>/README.md` 会被跟踪。请匹配现有的按工具条目。
5. **`integrations/<tool>/README.md`**——为该集成编写一份简短文档（每个工具都有一份；这是该工具目录中唯一被提交的文件）。
6. **运行 `./scripts/check-tools.sh`**——它必须通过。它会交叉检查 `tools.json` 与 `install.sh` 和 `convert.sh`，并标记任何缺失项。
7. **运行 `./scripts/test-install.sh`**——它必须通过。它会安装到一次性
   沙箱中（绝不会写入你真实的 `$HOME`），并钉死安装器的可观察
   契约：文件落在何处、`--path` 优先于该工具的环境变量、
   `--division` / `--agent` / `--agents-file` 会过滤、`--dry-run` 不写入
   任何内容，以及带空格的路径可以正常工作。CI 会在 Linux 和 macOS 上运行它。
8. **运行 `./scripts/test-convert-outputs.sh`**——它必须通过。它会将
   每个工具的输出重新生成到临时目录，并检查*产物*本身，而不是
   语法：每个代理的 description 都能完整往返、每个生成的
   文件都能被真正的 YAML/TOML 解析器解析、每个工具对每个代理恰好发出一份输出，
   并且每个源文件的解析方式与桌面应用读取时一致。
   当你有意改动了转换器时，它会报告 **manifest drift**
   ——这是预期行为。查看变更内容，再用 `--update` 运行一次，并
   提交刷新后的 `scripts/convert-outputs.sha256`，以便审查者一眼看到
   影响范围。CI 会在每个 PR 上运行它。

如果你的 PR 提交了转换后的输出（生成的 `integrations/<tool>/*` 文件），CI 和审查会要求你删除它们，并改为添加 `.gitignore` 规则。

### 什么才是优秀的代理？

**优秀的代理具备**：
- ✅ 狭窄而深入的专业领域
- ✅ 独特的个性和声音
- ✅ 具体的代码/模板示例
- ✅ 可衡量的成功指标
- ✅ 分步骤工作流
- ✅ 真实世界测试和迭代

**避免**：
- ❌ 通用的“有帮助的助手”人格
- ❌ 含糊的“我会帮你……”式描述
- ❌ 没有代码示例或交付物
- ❌ 过于宽泛的范围（样样通）
- ❌ 未经测试的理论方法

---

## 🔄 拉取请求流程

### PR 中应该包含什么（以及不应该包含什么）

合并 PR 的最快路径是**一个 markdown 文件**——一个新的或改进的代理。这是最理想的范围。

对于超出这个范围的内容，我们按以下方式保持流程顺畅：

#### 始终欢迎作为 PR 的内容
- 添加一个新代理（一个 `.md` 文件）
- 改进现有代理的内容、示例或个性
- 修复拼写错误或澄清文档

#### 请先发起 Discussion
- 新的工具、构建系统或 CI 工作流
- 架构变更（新目录、新脚本、站点生成器）
- 影响仓库中许多文件的变更
- 新的集成格式或平台

我们欢迎雄心勃勃的想法——一个 [Discussion](https://github.com/msitarzewski/agency-agents/discussions) 只是为了让社区在写代码之前先就方法达成一致。它能为所有人节省时间，尤其是你自己。

#### 我们始终会关闭的事项
- **提交构建产物**：生成的文件（`_site/`、编译后的资源、转换后的代理文件）绝不应被提交。用户在本地运行 `convert.sh`；其输出会被 gitignore。添加新工具时，添加那条 `.gitignore` 规则是你的步骤——见 [添加工具集成](#添加工具集成)。
- **在没有事先讨论的情况下批量修改现有代理的 PR**——即使出于好意的重新格式化也可能为其他贡献者造成合并冲突。
- **近似重复的“换皮”**：新的代理如果只是对现有代理做查找替换式复制（例如替换国家或平台名称），而不是一个真正新的专业角色，就不行。提交前运行 `scripts/check-agent-originality.sh`——CI 会自动运行它。

### 提交之前

1. **测试你的代理**：在真实场景中使用它，根据反馈迭代
2. **遵循模板**：匹配现有代理的结构
3. **添加示例**：至少包含 2-3 个代码/模板示例
4. **定义指标**：包含具体、可衡量的成功标准
5. **校对**：检查拼写错误、格式问题、清晰度
6. **检查它是否原创**：运行 `./scripts/check-agent-originality.sh path/to/your-agent.md`。它会将你的代理与整个 roster 进行比较，并标记近似重复项（把国家/平台名称替换掉不会骗过它）。一个新代理应当真正是新的——如果你是在为某个市场做本地化，请让平台、策略和示例真正不同，而不是简单地查找替换。
7. **检查它在每个工具中都能完整保留**：运行 `./scripts/test-convert-outputs.sh`。它会重新生成每个工具的输出，并确认你的代理能通过每个转换器——description 完整往返、文件可解析、没有内容丢失——以及其 frontmatter 的解析方式与桌面应用读取时一致。添加或编辑代理会改变生成产物，因此它会报告 **manifest drift**；这是预期行为，不是你的失败。查看变更，再用 `--update` 运行一次，并将刷新后的 `scripts/convert-outputs.sha256` 与你的代理一并提交。CI 会运行同样的检查。

这些检查之所以存在，是因为人们正在这些代理之上构建真正出色的东西，每天有数千人在十几种不同工具中依赖它们。这很棒——也意味着某个转换器里的一次小疏忽，或某个文件里多出来的一个引号，会悄无声息地同时影响到所有人。在本地运行这套测试，就是我们让下游所有人都能顺畅使用的方式。大约只需一分钟，却能让你的工作以你写下的原样，出现在每一个工具、每一位使用者面前。感谢你多走这一步——这对那些你永远不会见面的人来说，是一份实实在在的善意。

### 提交你的 PR

1. **Fork** 仓库
2. **创建分支**：`git checkout -b add-agent-name`
3. **进行更改**：添加你的代理文件
4. **提交**：`git commit -m "Add [Agent Name] specialist"`
5. **推送**：`git push origin add-agent-name`
6. **打开一个 Pull Request**，其中包括：
   - 清晰的标题："Add [Agent Name] - [Category]"
   - 对该代理功能的描述
   - 为什么需要这个代理（用例）
   - 你做过的任何测试

### PR 审查流程

1. **社区审查**：其他贡献者可能会提供反馈
2. **迭代**：处理反馈并进行改进
3. **批准**：维护者准备就绪后会批准
4. **合并**：你的贡献将成为 The Agency 的一部分！

### PR 模板

```markdown
## Agent Information
**Agent Name**: [Name]
**Category**: [engineering/design/marketing/etc.]
**Specialty**: [One-line description]

## Motivation
[Why is this agent needed? What gap does it fill?]

## Testing
[How have you tested this agent? Real-world use cases?]

## Checklist
- [ ] Original — not a near-duplicate (ran `scripts/check-agent-originality.sh`)
- [ ] Follows agent template structure
- [ ] Includes personality and voice
- [ ] Has concrete code/template examples
- [ ] Defines success metrics
- [ ] Includes step-by-step workflow
- [ ] Proofread and formatted correctly
- [ ] Tested in real scenarios
```

---

## 📐 风格指南

### 写作风格

- **要具体**：用“将页面加载减少 60%”而不是“让它更快”
- **要明确**：用“使用 TypeScript 创建 React 组件”而不是“构建 UI”
- **要令人难忘**：赋予代理个性，而不是千篇一律的企业口吻
- **要实用**：包含真实代码，而不是伪代码

### 格式

- 始终一致地使用 **Markdown 格式**
- 在章节标题中加入 **emoji**（便于快速浏览）
- 所有代码示例都使用 **代码块**，并带有正确的语法高亮
- 用 **表格** 比较选项或展示指标
- 用 **加粗** 表示强调，用 `code` 表示技术术语

### 代码示例

```markdown
## Example Code Block

\`\`\`typescript
// Always include:
// 1. Language specification for syntax highlighting
// 2. Comments explaining key concepts
// 3. Real, runnable code (not pseudo-code)
// 4. Modern best practices

interface AgentExample {
  name: string;
  specialty: string;
  deliverables: string[];
}
\`\`\`
```

### 语气

- **专业但平易近人**：不要过于正式，也不要过于随意
- **自信但不傲慢**：说“这是最佳方法”，而不是“也许你可以试试……”
- **有帮助但不过度手把手**：假定对方具备能力，提供深度
- **由个性驱动**：每个代理都应有独特的声音

---

## 🌟 致谢

做出重大贡献的贡献者将会：

- 列入 README 的致谢部分
- 在发布说明中被突出提及
- 出现在“本周代理”展示中（如果适用）
- 在代理文件本身中获得署名

---

## 🤔 有问题？

- **一般问题**：[GitHub Discussions](https://github.com/msitarzewski/agency-agents/discussions)
- **Bug 报告**：[GitHub Issues](https://github.com/msitarzewski/agency-agents/issues)
- **功能请求**：[GitHub Issues](https://github.com/msitarzewski/agency-agents/issues)
- **社区聊天**：[加入我们的讨论](https://github.com/msitarzewski/agency-agents/discussions)

---

## 📚 资源

### 面向新贡献者

- [README.md](README（项目说明）.md) - 概览和代理目录
- [示例：Frontend Developer](engineering（工程）/engineering-frontend-developer（前端开发者）.md) - 结构良好的代理示例
- [示例：Reddit 社区运营](marketing（营销）/marketing-reddit-community-builder（Reddit 社区运营）.md) - 很棒的个性示例
- [示例：Whimsy Injector](design（设计）/design-whimsy-injector（趣味注入师）.md) - 富有创意的专家示例

### 面向代理设计

- 阅读现有代理以获取灵感
- 学习哪些模式效果良好
- 在真实场景中测试你的代理
- 根据反馈迭代

---

## 🎉 谢谢你！

你的贡献让 The Agency 对每个人都更好。无论你是在：

- 添加新代理
- 改进文档
- 修复 bug
- 分享成功故事
- 帮助其他贡献者

**你正在带来改变。谢谢你！**

---

<div align="center">

**有问题？有想法？有反馈？**

[提交 Issue](https://github.com/msitarzewski/agency-agents/issues) • [发起 Discussion](https://github.com/msitarzewski/agency-agents/discussions) • [提交 PR](https://github.com/msitarzewski/agency-agents/pulls)

由社区用 ❤️ 制作

</div>
