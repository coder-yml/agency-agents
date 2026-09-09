# Hermes Agency Agents Router 插件

由 `scripts/convert.sh --tool hermes` 生成。

此集成安装一个名为 `agency-agents-router` 的 Hermes 插件，而非将数百个生成的技能添加到 `skills.external_dirs`。Hermes 在启动时看到一个小型固定的工具界面，而完整的 Agency 阵容存储在磁盘上的 `data/agents.json` 中，并按需搜索/延迟加载。

生成的代理数量：279

## 暴露给 Hermes 的工具

- `agency_agents_search` — 按查询/部门查找匹配的专家。
- `agency_agents_inspect` — 检查一个专家的元数据或完整正文。
- `agency_agents_load` — 为当前任务组合一个专家提示。
- `agency_agents_delegate` — 通过 Hermes 的公开子代理生命周期进行委托。

每个工具都使用 Hermes 完整的 function-tool schema 注册，包括其名称、描述和 JSON `parameters`。可用参数如下：

| 工具 | 参数 |
| --- | --- |
| `agency_agents_search` | `query`（必填），可选 `division` 和 `limit` |
| `agency_agents_inspect` | `agent` 或 `slug`，可选 `include_body` |
| `agency_agents_load` | `agent` 或 `slug`，可选 `task` |
| `agency_agents_delegate` | `agent` 或 `slug`，`task`（必填） |

常见流程是：按能力搜索，取回返回的 `slug`，然后检查、加载或委托给该专家。你可以用自然语言让 Hermes 完成这些步骤；不需要直接调用工具。

## Hermes 的专家使用说明

当 Hermes 项目需要 Agency 专家时，明确要求 Hermes 使用 `agency-agents-router` 插件/路由器，并仅为当前阶段加载所需的专家。不要要求 Hermes 安装或预加载完整的 Agency 阵容作为技能。

推荐的项目指令：

```text
使用 agency-agents-router 插件。搜索 Agency 阵容找到合适的专家，然后仅为项目的每个部分加载或委托所需的特定代理。对于多学科项目，在项目中使用多个选定的专家，但保持路由延迟加载：不要预加载完整的 Agency 阵容，也不要将 agency-agents 添加到 skills.external_dirs。
```

示例：

```text
对于此 Data Swami 构建，使用 agency-agents-router 插件选择相关的 Agency 专家。先搜索，然后根据需要委托给选定的代理，如前端、后端、UX、QA、数据工程和产品策略。按需加载/委托每个专家，而非在启动时加载所有 Agency 代理。
```

## 安装

```bash
./scripts/convert.sh --tool hermes
./scripts/install.sh --tool hermes
```

安装程序将生成的插件复制到：

```text
${HERMES_HOME:-~/.hermes}/plugins/agency-agents-router
```

然后在 Hermes 配置中的 `plugins.enabled` 下启用 `agency-agents-router`。它**不会**写入 `skills.external_dirs`。

安装后请重启 Hermes 或开启新会话，以便加载插件及其工具 schema。如果 Hermes 显示这些工具但没有文档中的参数，请从最新的 Agency Agents 检出重新生成并重新安装插件，然后重启 Hermes。
