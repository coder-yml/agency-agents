# ZCode 集成

[ZCode](https://z.ai) 是 Z.ai 基于 GLM 的编码代理运行时。每个 agency
agent 都会作为一个独立的 Markdown agent 文件呈现，带有 `name` 和
`description` frontmatter，ZCode 会从其 agents 目录中发现它们。

生成的文件来自 `scripts/convert.sh --tool zcode`，该脚本会将每个 agency agent
写入 `integrations/zcode/agents/` 中的一个 Markdown 文件。这些生成文件不会被提交（见
`.gitignore`）；请在本地重新生成。

## 生成

从仓库根目录执行：

```bash
./scripts/convert.sh --tool zcode
```

## 安装

从你的目标目录运行安装程序：

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool zcode
```

agents 会安装到 `~/.zcode/agents/<slug>.md`（用户作用域）——也就是
ZCode 读取子 agent 的目录。使用 `--division` / `--agent` 安装子集，
或者设置 `ZCODE_AGENTS_DIR` 来覆盖目标位置。
