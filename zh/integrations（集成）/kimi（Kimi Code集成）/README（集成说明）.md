# Kimi Code CLI 集成

将所有 Agency 代理转换为 Kimi Code CLI 代理规格。每个代理成为一个包含 `agent.yaml`（代理规格）和 `system.md`（系统提示）的目录。

## 安装

### 前置条件

- 已安装 [Kimi Code CLI](https://github.com/MoonshotAI/kimi-cli)

### 安装

```bash
# 生成集成文件（新克隆时需要）
./scripts/convert.sh --tool kimi

# 安装代理
./scripts/install.sh --tool kimi
```

这会将代理复制到 `~/.config/kimi/agents/`。

## 使用

### 激活代理

使用 `--agent-file` 标志加载特定代理：

```bash
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml
```

### 在项目中

```bash
cd /your/project
kimi --agent-file ~/.config/kimi/agents/frontend-developer/agent.yaml \
     --work-dir /your/project \
     "审查此 React 组件的性能问题"
```

### 列出已安装的代理

```bash
ls ~/.config/kimi/agents/
```

## 代理结构

每个代理目录包含：

```
~/.config/kimi/agents/frontend-developer/
├── agent.yaml    # 代理规格（工具、subagent）
└── system.md     # 包含人格和指令的系统提示
```

### agent.yaml 格式

```yaml
version: 1
agent:
  name: frontend-developer
  extend: default  # 继承自 Kimi 内置的默认代理
  system_prompt_path: ./system.md
  tools:
    - "kimi_cli.tools.shell:Shell"
    - "kimi_cli.tools.file:ReadFile"
    # ... 所有默认工具
```

## 重新生成

修改源代理后：

```bash
./scripts/convert.sh --tool kimi
./scripts/install.sh --tool kimi
```

## 故障排除

### 找不到代理文件

确保在 `install.sh` 之前运行了 `convert.sh`：

```bash
./scripts/convert.sh --tool kimi
```

### 未检测到 Kimi CLI

确保 `kimi` 在你的 PATH 中：

```bash
which kimi
kimi --version
```

### 无效的 YAML

验证生成的文件：

```bash
python3 -c "import yaml; yaml.safe_load(open('integrations/kimi/frontend-developer/agent.yaml'))"
```
