# 工作流示例：书籍章节开发

> 一个聚焦的单 Agent 工作流，将粗糙的源材料转化为具有明确修订循环的战略性第一人称章节草稿。

## 何时使用此工作流

当作者有语音笔记、片段或策略笔记，但尚未形成干净的章节草稿时使用此工作流。目标不是通用的代笔写作。目标是产出一个强化品类定位、保留作者声音、并清晰暴露开放性编辑决策的章节。

## 使用的 Agent

| Agent | 角色 |
|-------|------|
| Book Co-Author | 将源材料转化为带编辑注释和后续步骤问题的版本化章节草稿 |

## 激活示例

```text
Activate Book Co-Author.

Book goal: Build authority around practical AI adoption for Mittelstand companies.
Target audience: Owners and operational leaders of 20-200 person businesses.
Chapter topic: Why most AI projects fail before implementation starts.
Desired draft maturity: First substantial draft.

Raw material:
- Voice memo: "The real failure happens in expectation setting, not tooling."
- Notes: Leaders buy software before defining the operational bottleneck.
- Story fragment: We nearly rolled out the wrong automation in a cabinetmaking workflow because the actual problem was quoting delays, not production throughput.
- Positioning angle: Practical realism over hype.

Produce:
1. Chapter objective and strategic role in the book
2. Any clarification questions you need
3. Chapter 2 - Version 1 - ready for review
4. Editorial notes on assumptions and proof gaps
5. Specific next-step revision requests
```

## 预期输出形态

Book Co-Author 应以五个部分回复：

1. `Target Outcome`
2. `Chapter Draft`
3. `Editorial Notes`
4. `Feedback Loop`
5. `Next Step`

## 质量标准

- 草稿保持第一人称语气
- 章节有一个清晰的承诺和内部逻辑
- 论断与源材料关联或标记为假设
- 移除通用的激励性语言
- 输出以明确的修订问题结束，而非模糊的交接
