# 🔌 集成

此目录包含 The Agency 的集成以及为受支持的 agentic 编码工具转换后的格式。

## 支持的工具

- **[Claude Code](#claude-code)** — `.md` agents，直接使用仓库
- **[GitHub Copilot](#github-copilot)** — `.md` agents，直接使用仓库
- **[Antigravity](#antigravity)** — `antigravity/` 中每个 agent 一个 `SKILL.md`
- **[Gemini CLI](#gemini-cli)** — `gemini-cli/agents/` 中的 `.md` agent 文件
- **[OpenCode](#opencode)** — `opencode/` 中的 `.md` agent 文件
- **[OpenClaw](#openclaw)** — `SOUL.md` + `AGENTS.md` + `IDENTITY.md` 工作区
- **[Cursor](#cursor)** — `cursor/` 中的 `.mdc` 规则文件
- **[Aider](#aider)** — `aider/` 中的 `CONVENTIONS.md`
- **[Windsurf](#windsurf)** — `windsurf/` 中的 `.windsurfrules`
- **[Kimi Code](#kimi-code)** — `kimi/` 中的 YAML agent 规范
- **[Qwen Code](#qwen-code)** — `.qwen/agents/` 中项目范围的 `.md` SubAgents
- **[Codex](#codex)** — `codex/` 中的 `.toml` 自定义 agents
- **[Mistral Vibe](vibe（Mistral%20Vibe集成）/README（集成说明）.md)** — 在 `vibe/` 中生成的 `.toml` agents + 提示文件
- **Osaurus** -- 在 `osaurus/` 中生成的 `SKILL.md` skills
- **[Hermes](hermes（Hermes集成）/README（集成说明）.md)** -- 生成的 lazy-router 插件

## 快速安装

```bash
# 自动为所有检测到的工具安装
./scripts/install.sh

# 安装一个特定的 home 范围工具
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code
./scripts/install.sh --tool codex
./scripts/install.sh --tool osaurus
./scripts/install.sh --tool hermes

# Gemini CLI 在全新克隆的仓库中需要生成的集成文件
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli

# Qwen Code 在全新克隆的仓库中也需要生成的 SubAgent 文件
./scripts/convert.sh --tool qwen
./scripts/install.sh --tool qwen
```

如果你安装了 OpenClaw 且 gateway 已在运行，请在安装后重启它：

```bash
openclaw gateway restart
```

对于 OpenCode、Cursor、Aider、Windsurf 和 Qwen Code 等项目范围工具，请像下面各工具专用章节所示那样，从你的目标项目根目录运行安装程序。

## 重新生成集成文件

如果你添加或修改了 agents，请重新生成所有集成文件：

```bash
./scripts/convert.sh
```

---

## Claude Code

The Agency 最初就是为 Claude Code 设计的。agents 可原生工作，无需转换。

```bash
cp -r <category>/*.md ~/.claude/agents/
# 或一次性安装全部：
./scripts/install.sh --tool claude-code
```

详情请参见 [claude-code/README.md](claude-code（Claude%20Code集成）/README（集成说明）.md)。

---

## GitHub Copilot

The Agency 也可与 GitHub Copilot 原生协作。agents 可以直接复制到 `~/.github/agents/` 和 `~/.copilot/agents/`，无需转换。

```bash
./scripts/install.sh --tool copilot
```

详情请参见 [github-copilot/README.md](github-copilot（GitHub%20Copilot集成）/README（集成说明）.md)。

---

## Antigravity

Skills 安装到 `~/.gemini/config/skills/`。每个 agent 都会变成一个单独的 skill，并以前缀 `agency-` 命名，以避免命名冲突。

```bash
./scripts/install.sh --tool antigravity
```

详情请参见 [antigravity/README.md](antigravity（Antigravity集成）/README（集成说明）.md)。

---

## Gemini CLI

agents 会被打包为 Gemini CLI subagents。  
Subagents 安装到 `~/.gemini/agents/`。  
由于 agent 文件是生成的产物，请在全新克隆后先运行  
`./scripts/convert.sh --tool gemini-cli` 再安装。

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

详情请参见 [gemini-cli/README.md](gemini-cli（Gemini%20CLI集成）/README（集成说明）.md)。

---

## OpenCode

每个 agent 都会变成 `.opencode/agents/` 中一个项目范围的 `.md` 文件。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool opencode
```

详情请参见 [opencode/README.md](opencode（OpenCode集成）/README（集成说明）.md)。

---

## OpenClaw

每个 agent 都会变成一个 OpenClaw 工作区，其中包含 `SOUL.md`、`AGENTS.md` 和 `IDENTITY.md`。

在安装之前，先生成 OpenClaw 工作区：

```bash
./scripts/convert.sh --tool openclaw
```

然后安装它们：

```bash
./scripts/install.sh --tool openclaw
```

详情请参见 [openclaw/README.md](openclaw（OpenClaw集成）/README（集成说明）.md)。

---

## Cursor

每个 agent 都会变成一个 `.mdc` 规则文件。规则是项目范围的——请从你的项目根目录运行安装程序。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool cursor
```

详情请参见 [cursor/README.md](cursor（Cursor集成）/README（集成说明）.md)。

---

## Aider

所有 agents 会被整合到一个单独的 `CONVENTIONS.md` 文件中，Aider 会在你的项目根目录中存在该文件时自动读取它。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool aider
```

详情请参见 [aider/README.md](aider（Aider集成）/README（集成说明）.md)。

---

## Windsurf

所有 agents 会被整合到一个单独的 `.windsurfrules` 文件中，放在你的项目根目录。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool windsurf
```

详情请参见 [windsurf/README.md](windsurf（Windsurf集成）/README（集成说明）.md)。

---

## Kimi Code

每个 agent 都会被转换为一个 Kimi Code CLI agent 规范（YAML 格式，配有单独的 system prompt 文件）。agents 会安装到 `~/.config/kimi/agents/`。

由于 Kimi agent 文件是从源 Markdown 生成的，请在全新克隆后先运行  
`./scripts/convert.sh --tool kimi` 再安装。

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

### 用法

安装后，使用 `--agent-file` 标志来使用某个 agent：

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

或者在特定项目中使用：

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project
```

详情请参见 [kimi/README.md](kimi（Kimi%20Code集成）/README（集成说明）.md)。

---

## Qwen Code

每个 agent 都会变成 `.qwen/agents/` 中一个项目范围的 `.md` SubAgent 文件。

从全新克隆开始时，请先生成 Qwen 文件：

```bash
./scripts/convert.sh --tool qwen
```

然后从你的项目根目录安装它们：

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool qwen
```

详情请参见 [qwen/README.md](qwen（Qwen%20Code集成）/README（集成说明）.md)。

---

## Codex

每个 agent 都会被转换为一个独立的 Codex 自定义 agent TOML 文件，并安装到 `~/.codex/agents/`。

由于 Codex 使用的是生成的 TOML 文件，而不是直接使用源 Markdown，所以请在全新克隆后先运行转换器再安装：

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

详情请参见 [codex/README.md](codex（Codex集成）/README（集成说明）.md)。
