# Aider 集成

`CONVENTIONS.md` 是花名册索引：每个 agent 的名称、用途、所属分类，以及完整指令的路径。

## 为什么用索引而不是全文

Aider 会在整个会话中把约定文件保持在上下文里——这正是该文件的用途。279 份 agent 正文合计约 380 万字符，大约一百万 tokens，因此一份装下全部正文的约定文件塞不进任何模型，尝试这样做也会代价高昂。

索引大约 97,000 字符（约 24k tokens）。以只读方式加载，以便 aider 将其标记为可缓存，并在真正需要时再读入单个 agent 的完整指令。

## 安装

```bash
# 从你的项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

## 使用代理

通常点名即可——描述已经在上下文中：

```
使用 Frontend Developer 代理重构此组件。
```

若需要该代理的完整指令，把它的文件读入会话。索引会给出路径：

```
/read-only /path/to/agency-agents/engineering/engineering-frontend-developer.md
```

## 手动使用

```bash
aider --read CONVENTIONS.md
```

`--read` 会把文件标记为只读，并在启用 prompt caching 时让 aider 缓存它，因此索引不会在每一轮都重新发送。

## 重新生成

```bash
./scripts/convert.sh --tool aider
```
