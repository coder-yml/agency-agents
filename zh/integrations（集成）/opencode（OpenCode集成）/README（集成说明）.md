# OpenCode 集成

OpenCode 代理是存储在 `.opencode/agents/` 中的带有 YAML frontmatter 的 `.md` 文件。转换器将命名颜色映射为十六进制代码，并添加 `mode: subagent`，以便代理通过 `@agent-name` 按需调用，而非在主代理选择器中杂乱显示。

## 安装

```bash
# 从你的项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

这会在你的项目目录中创建 `.opencode/agents/<slug>.md` 文件。

## 激活代理

在 OpenCode 中，使用 `@` 前缀调用 subagent：

```
@frontend-developer 帮助构建此组件。
```

```
@reality-checker 审查此 PR。
```

你也可以从 OpenCode UI 的代理选择器中选择代理。

## 代理格式

每个生成的代理文件包含：

```yaml
---
name: Frontend Developer
description: 专注于现代 Web 技术的专业前端开发工程师...
mode: subagent
color: "#00FFFF"
---
```

- **mode: subagent** — 代理按需可用，不显示在主 Tab 循环列表中
- **color** — 十六进制代码（源文件中的命名颜色会自动转换）

## 项目 vs 全局

`.opencode/agents/` 中的代理是**项目范围**的。要使其在所有项目中全局可用，先生成代理文件，然后使用 `--path` 安装：

```bash
./scripts/convert.sh --tool opencode
./scripts/install.sh --tool opencode --path ~/.config/opencode/agents
```

## 重新生成

```bash
./scripts/convert.sh --tool opencode
```
