# Qwen Code 集成

Qwen Code 使用 `.qwen/agents/` 中的项目范围 `.md` SubAgent 文件。

生成的文件来自 `scripts/convert.sh --tool qwen`，它为每个 agency 代理写入一个 SubAgent Markdown 文件到 `integrations/qwen/agents/`。

## 生成

从仓库根目录：

```bash
./scripts/convert.sh --tool qwen
```

## 安装

从你的目标项目根目录运行安装程序：

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool qwen
```

这会将生成的 SubAgent 文件复制到：

```text
.qwen/agents/
```

## 在 Qwen Code 中刷新

安装后：

- 在 Qwen Code 中运行 `/agents manage` 刷新代理列表，或
- 重启当前的 Qwen Code 会话

## 注意事项

- Qwen Code 是项目范围的，非 home 范围的
- 生成的 Qwen 文件使用最小化的 frontmatter：`name`、`description` 和可选的 `tools`
- 如果你更新此仓库中的代理，在重新安装前重新生成 Qwen 输出
