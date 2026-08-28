# Gemini CLI 集成

将所有 Agency 代理打包为 Gemini CLI subagent。这些代理安装到 `~/.gemini/agents/`。

## 安装

```bash
# 先生成 Gemini CLI 代理文件
./scripts/convert.sh --tool gemini-cli

# 然后安装到 ~/.gemini/agents/
./scripts/install.sh --tool gemini-cli
```

## 使用代理

在 Gemini CLI 中，在你的提示中按名称引用代理：

```
使用 frontend-developer 代理帮我构建这个 UI。
```

或者如果你的 Gemini CLI 版本支持，直接调用代理：

```bash
gemini --agent frontend-developer "我应该如何构建这个 React 组件？"
```

## 结构

```
~/.gemini/agents/
  frontend-developer.md
  backend-architect.md
  reality-checker.md
  ...
```

## 重新生成

```bash
./scripts/convert.sh --tool gemini-cli
```
