# Antigravity 集成

将完整的 Agency 角色库安装为 Antigravity skills。每个 agent 都会添加 `agency-` 前缀，以避免与现有 skills 冲突。

## 安装

```bash
./scripts/install.sh --tool antigravity
```

这会将 `integrations/antigravity/` 中的文件复制到 `~/.gemini/config/skills/`（全局）。对于项目范围内的 skills，Antigravity 也会读取 `<project>/.agents/skills/`。

## 激活 Skill

在 Antigravity 中，通过 slug 激活一个 agent：

```
Use the agency-frontend-developer skill to review this component.
```

可用的 slug 遵循 `agency-<agent-name>` 模式，例如：
- `agency-frontend-developer`
- `agency-backend-architect`
- `agency-reality-checker`
- `agency-growth-hacker`

## 重新生成

在修改 agents 之后，重新生成 skill 文件：

```bash
./scripts/convert.sh --tool antigravity
```

## 文件格式

每个 skill 都是一个带有与 Antigravity 兼容 frontmatter 的 `SKILL.md` 文件：

```yaml
---
name: agency-frontend-developer
description: Expert frontend developer specializing in...
risk: low
source: community
date_added: '2026-03-08'
---
```
