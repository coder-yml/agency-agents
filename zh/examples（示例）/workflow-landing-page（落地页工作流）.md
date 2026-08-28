# 多 Agent 工作流：落地页冲刺

> 使用 4 个 Agent 在一天内交付一个转化优化的落地页。

## 场景

你需要为一个新产品发布制作落地页。它需要看起来很棒、能转化访客，并在当天结束前上线。

## Agent 团队

| Agent | 在此工作流中的角色 |
|-------|---------------------|
| Content Creator | 撰写文案 |
| UI Designer | 设计布局和组件规范 |
| Frontend Developer | 构建它 |
| Growth Hacker | 优化转化 |

## 工作流

### 上午：文案 + 设计（并行）

**步骤 1a — 激活 Content Creator**

```
Activate Content Creator.

Write landing page copy for "FlowSync" — an API integration platform
that connects any two SaaS tools in under 5 minutes.

Target audience: developers and technical PMs at mid-size companies.
Tone: confident, concise, slightly playful.

Sections needed:
1. Hero (headline + subheadline + CTA)
2. Problem statement (3 pain points)
3. How it works (3 steps)
4. Social proof (placeholder testimonial format)
5. Pricing (3 tiers: Free, Pro, Enterprise)
6. Final CTA

Keep it scannable. No fluff.
```

**步骤 1b — 激活 UI Designer（并行）**

```
Activate UI Designer.

Design specs for a SaaS landing page. Product: FlowSync (API integration platform).
Style: clean, modern, dark mode option. Think Linear or Vercel aesthetic.

Deliver:
1. Layout wireframe (section order + spacing)
2. Color palette (primary, secondary, accent, background)
3. Typography (font pairing, heading sizes, body size)
4. Component specs: hero section, feature cards, pricing table, CTA buttons
5. Responsive breakpoints (mobile, tablet, desktop)
```

### 中午：构建

**步骤 2 — 激活 Frontend Developer**

```
Activate Frontend Developer.

Build a landing page from these specs:

Copy: [粘贴 Content Creator 输出]
Design: [粘贴 UI Designer 输出]

Stack: HTML, Tailwind CSS, minimal vanilla JS (no framework needed).
Requirements:
- Responsive (mobile-first)
- Fast (no heavy assets, system fonts OK)
- Accessible (proper headings, alt text, focus states)
- Include a working email signup form (action URL: /api/subscribe)

Deliver a single index.html file ready to deploy.
```

### 下午：优化

**步骤 3 — 激活 Growth Hacker**

```
Activate Growth Hacker.

Review this landing page for conversion optimization:

[粘贴 HTML 或描述当前页面]

Evaluate:
1. Is the CTA above the fold?
2. Is the value proposition clear in under 5 seconds?
3. Any friction in the signup flow?
4. What A/B tests would you run first?
5. SEO basics: meta tags, OG tags, structured data

Give me specific changes, not general advice.
```

## 时间线

| 时间 | 活动 | Agent |
|------|------|-------|
| 9:00 | 文案 + 设计启动（并行） | Content Creator + UI Designer |
| 11:00 | 构建开始 | Frontend Developer |
| 14:00 | 第一版本就绪 | — |
| 14:30 | 转化审查 | Growth Hacker |
| 15:30 | 应用反馈 | Frontend Developer |
| 16:30 | 发布 | 部署到 Vercel/Netlify |

## 关键模式

1. **并行启动**：文案和设计同时进行，因为它们是独立的
2. **合并点**：Frontend Developer 在开始之前需要两个输出
3. **反馈循环**：Growth Hacker 审查，然后 Frontend Developer 应用更改
4. **时间盒约束**：每个步骤有明确的时间盒以防止范围蔓延
