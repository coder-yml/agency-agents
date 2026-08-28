# Windsurf 集成

完整的 Agency 阵容合并到一个 `.windsurfrules` 文件中。规则是**项目范围**的 —— 从你的项目根目录安装它们。

## 安装

```bash
# 从你的项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

## 激活代理

在 Windsurf 中，在你的提示中按名称引用代理：

```
使用 Frontend Developer 代理构建此组件。
```

## 重新生成

```bash
./scripts/convert.sh --tool windsurf
```
