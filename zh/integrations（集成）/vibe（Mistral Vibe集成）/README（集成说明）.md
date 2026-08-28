# Mistral Vibe 集成

Mistral Vibe 每个 agent 使用两个文件：
- 一个 TOML 配置文件（`~/.vibe/agents/<slug>.toml`）
- 一个 Markdown 提示文件（`~/.vibe/prompts/<slug>.md`）

生成的文件来自 `scripts/convert.sh --tool vibe`，该脚本会为每个 agency agent
分别写入一个 TOML agent 配置和一个 Markdown 提示文件到
`integrations/vibe/agents/` 和 `integrations/vibe/prompts/`。

## 生成

从仓库根目录执行：

```bash
./scripts/convert.sh --tool vibe
```

## 安装

从你的目标目录运行安装器：

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool vibe
```

这会把生成的文件复制到：

```text
~/.vibe/agents/<slug>.toml
~/.vibe/prompts/<slug>.md
```

你可以使用 `VIBE_HOME` 环境变量覆盖目标位置：

```bash
VIBE_HOME=~/.config/vibe ./scripts/install.sh --tool vibe
```

## 生成格式

每个生成的 agent 对位于：

```text
integrations/vibe/agents/<slug>.toml
integrations/vibe/prompts/<slug>.md
```

### Agent TOML 文件

最小化的 Vibe agent 配置：

```toml
agent_type = "agent"
system_prompt_id = "<slug>"
```

用户可以在他们的 agent TOML 文件中指定 `active_model`，或者依赖其
Vibe 配置默认模型。

### 提示 Markdown 文件

提示文件包含：
- 带有 agent 名称的标题头
- agent 描述
- 来自源 agent 的完整 Markdown 正文

## 使用方法

安装后，在 Mistral Vibe 中通过 system prompt ID 引用 agent
（该 ID 与文件名 slug 一致）。

示例：
```text
Use the Code Reviewer agent to analyze this pull request.
```

## 过滤

只安装特定 division 或 agent：

```bash
# 仅安装 Division 1 的 agents
./scripts/install.sh --tool vibe --division 1

# 仅安装 code-reviewer agent
./scripts/install.sh --tool vibe --agent code-reviewer
```

## 重新生成

修改源 agents 之后：

```bash
./scripts/convert.sh --tool vibe
./scripts/install.sh --tool vibe
```

## 故障排查

### 未检测到 Mistral Vibe

确保 `vibe` 在你的 PATH 中，或者 `~/.vibe/` 已经存在：

```bash
which vibe
vibe --version
```

### 未生成集成文件

在安装前先生成 Vibe 产物：

```bash
./scripts/convert.sh --tool vibe
```
