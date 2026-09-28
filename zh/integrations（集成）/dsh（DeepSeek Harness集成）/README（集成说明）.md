# DeepSeek Harness 集成

将完整的 Agency 角色库安装为 DeepSeek Harness（DSH）skills。每个 agent 都会添加 `agency-` 前缀，以避免与内置 skills 冲突。

## 安装

```bash
./scripts/install.sh --tool dsh
```

这会将 `integrations/dsh/` 中的文件复制到 `${DSH_HOME:-$HOME/.dsh}/skills/`（用户级）。如果 Harness 配置位于其他位置，请设置 `DSH_HOME`。对于项目范围内的 skills，在项目根目录使用 `DSH_SKILLS_DIR=.dsh/skills` 运行安装器——该覆盖优先于 `DSH_HOME`，且 DSH 会自动读取 `<project>/.dsh/skills/`。

> DSH 会实时发现 skills（监视这些根目录）：新增、重命名或删除的 skills 会在下一次技能目录中生效，无需重启。没有需要编辑的配置文件。

## 激活 Skill

在 DSH 中，skills 默认可由用户和模型调用。通过斜杠命令，或在对话中按名称激活一个 agent：

```
/agency-frontend-developer review this React component
```

或者：

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
./scripts/convert.sh --tool dsh
```

## 文件格式

每个 skill 都是一个 `SKILL.md` 文件，带有标准 Agent-Skills frontmatter（必填 `name` 和 `description`，`name` 必须是严格的 kebab-case），正文为 agent 人格：

```markdown
---
name: 'agency-frontend-developer'
description: 'Expert frontend developer specializing in modern web technologies, React/Vue/Angular frameworks, UI implementation, and performance optimization'
---
...agent body...
```

这与 Antigravity 和 Osaurus 的 skill 输出逐字节相同（`skill-md` 格式），因此 Agency Agents 应用可以原生渲染它。

## DSH 扫描的 Skill 根目录

| 优先级 | 来源 | 路径 |
|---|---|---|
| 100 | 项目 | `<project>/.dsh/skills` |
| 200 | 项目 | `<project>/.agents/skills` |
| 300 | 自定义 | `customSkillDirs` 配置 |
| 400 | 用户 | `${DSH_HOME:-$HOME/.dsh}/skills`（默认安装位置） |
| 500 | 用户 | `~/.agents/skills` |

项目级 skills（优先级 100/200）会遮蔽同名的用户级 skills（优先级 400/500），因此项目安装会在该项目中覆盖用户级安装。
