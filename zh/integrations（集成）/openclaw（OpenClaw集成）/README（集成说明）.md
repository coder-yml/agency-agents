# OpenClaw 集成

OpenClaw 代理安装为工作区，包含 `SOUL.md`、`AGENTS.md` 和 `IDENTITY.md` 文件。安装程序将每个工作区复制到 `~/.openclaw/agency-agents/` 中，并在 `openclaw` CLI 可用时注册它。

安装前，生成 OpenClaw 工作区：

```bash
./scripts/convert.sh --tool openclaw
```

## 安装

```bash
./scripts/install.sh --tool openclaw
```

## 激活代理

安装后，代理在 OpenClaw 会话中通过 `agentId` 可用。

如果 OpenClaw 网关已在运行，安装后重启它：

```bash
openclaw gateway restart
```

## 重新生成

```bash
./scripts/convert.sh --tool openclaw
```
