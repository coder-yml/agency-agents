# Claude Code 集成

The Agency 是为 Claude Code 构建的。无需转换 —— 代理原生使用现有的 `.md` + YAML frontmatter 格式。

## 安装

```bash
# 将所有代理复制到你的 Claude Code 代理目录
./scripts/install.sh --tool claude-code

# 或手动复制一个类别
cp engineering/*.md ~/.claude/agents/
```

## 激活代理

在任何 Claude Code 会话中，按名称引用代理：

```
激活 Frontend Developer，帮我构建一个 React 组件。
```

```
使用 Reality Checker 代理验证此功能是否可投产。
```

## 代理目录

代理按部门组织。请参阅 [主 README](../../README（项目说明）.md) 了解完整的 Agency 阵容。
