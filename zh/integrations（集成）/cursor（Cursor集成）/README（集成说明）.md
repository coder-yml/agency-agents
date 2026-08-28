# Cursor 集成

将完整的 Agency 阵容转换为 Cursor `.mdc` 规则文件。规则是**项目范围**的 —— 从你的项目根目录安装它们。

## 安装

```bash
# 从你的项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

这会在你的项目中创建 `.cursor/rules/<agent-slug>.mdc` 文件。

## 激活规则

在 Cursor 中，在你的提示中引用代理：

```
@frontend-developer 审查此 React 组件的性能问题。
```

或通过编辑其 frontmatter 将规则设为始终启用：

```yaml
---
description: 专业前端开发工程师...
globs: "**/*.tsx,**/*.ts"
alwaysApply: true
---
```

## 重新生成

```bash
./scripts/convert.sh --tool cursor
```
