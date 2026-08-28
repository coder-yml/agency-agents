# Codex 集成

将所有 Agency 代理转换为 Codex 自定义代理 TOML 文件。每个源代理成为一个独立的 `.toml` 文件，包含 Codex 所需的最小字段：`name`、`description` 和 `developer_instructions`。

## 安装

### 前置条件

- 已安装 [Codex](https://developers.openai.com/codex/overview)

### 转换并安装

```bash
# 生成集成文件（新克隆时需要）
./scripts/convert.sh --tool codex

# 安装代理
./scripts/install.sh --tool codex
```

这会将生成的代理文件复制到 `~/.codex/agents/`。

## 生成格式

每个生成的文件位于：

```text
integrations/codex/agents/<slug>.toml
```

映射是有意最小化的：

- `name` 从源 frontmatter 原样复制
- `description` 从源 frontmatter 原样复制
- `developer_instructions` 包含完整的 Markdown 正文，不做更改

仅源信息的元数据如 `color`、`emoji`、`vibe` 以及其他不受支持的 frontmatter 字段将被省略。

## 使用

安装后，在 Codex 中按名称引用自定义代理：

```text
使用 Frontend Developer 代理审查此组件。
```

Codex 使用 TOML 文件中的 `name` 字段作为真实来源，因此生成的文件名标识符仅用于文件系统安全。

## 重新生成

修改源代理后：

```bash
./scripts/convert.sh --tool codex
./scripts/install.sh --tool codex
```

## 故障排除

### 未找到 Codex 集成

在安装前生成 Codex 产物：

```bash
./scripts/convert.sh --tool codex
```

### 未检测到 Codex

确保 `codex` 在你的 PATH 中，或 `~/.codex/` 已存在：

```bash
which codex
codex --help
```
