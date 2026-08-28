# Aider 集成

完整的 Agency 阵容合并到一个 `CONVENTIONS.md` 文件中。Aider 在项目根目录中检测到此文件时会自动读取。

## 安装

```bash
# 从你的项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

## 激活代理

在你的 Aider 会话中，按名称引用代理：

```
使用 Frontend Developer 代理重构此组件。
```

```
应用 Reality Checker 代理验证此功能是否可投产。
```

## 手动使用

你也可以直接传递约定文件：

```bash
aider --read CONVENTIONS.md
```

## 重新生成

```bash
./scripts/convert.sh --tool aider
```
