# GitHub Copilot 集成

The Agency 开箱即用地支持 GitHub Copilot。无需转换 —— 代理使用现有的 `.md` + YAML frontmatter 格式。

## 安装

```bash
# 将所有代理复制到你的 GitHub Copilot 代理目录
./scripts/install.sh --tool copilot

# 或手动复制一个类别
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

## 激活代理

在任何 GitHub Copilot 会话中，按名称引用代理：

```
激活 Frontend Developer，帮我构建一个 React 组件。
```

```
使用 Reality Checker 代理验证此功能是否可投产。
```

## 代理目录

代理按部门组织。请参阅 [主 README](../../README（项目说明）.md) 了解完整的当前阵容。
