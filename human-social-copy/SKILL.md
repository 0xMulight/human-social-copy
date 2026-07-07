---
name: human-social-copy
description: "将AI/工具/crypto/美股/财报内容写成真人风格的中文社交媒体文案。用于写推文、X帖子、中文社交分享和图文脚本。"
version: 2.11.0
author: 0xMulight
metadata:
  hermes:
    tags: [writing, social-media, chinese, tweet, x, humanize, copywriting, finance]
    category: social-media
    triggers:
      - "写推文"
      - "写推特"
      - "写成帖子"
      - "发推"
      - "社交媒体文案"
      - "中文推文"
      - "美股"
      - "财报"
      - "tweet"
      - "推文"
---

# Human Social Copy

Use this skill when the user wants Chinese social media copy that feels human, practical, and ready to post. It works for X, Threads, Instagram, TikTok, crypto yap, airdrop analysis, AI tools, GitHub projects, US stocks, earnings, macro notes, market recap, and long-form image copy.

Default language: Simplified Chinese.

## Goal

Turn rough notes into a post with:

1. Hook
2. Useful value
3. Soft CTA

Do not create a thread unless the user asks for one.

## Core Rules

- Write in Simplified Chinese.
- Remove spaces around English words in Chinese text, for example `AI工具`, `GitHub项目`, `CTA结尾`.
- Remove all parentheses from the final copy.
- Keep the language plain and credible.
- Avoid decorative wording, inflated claims, and announcement-style writing.
- Do not overuse subheadings.
- Do not write like a tutorial outline unless the user asks for one.
- Preserve a strong original hook if it is already natural.

## Direct Sentence Rule

Prefer direct sentences that explain the result.

If the user gives a specific project only as an example, abstract the writing pattern. Do not add that project name as a fixed rule.

When writing about a tool or project, answer what it can do, when it works, and which scenario it fits.

Good patterns:

- `{工具名}可以记录{信息A}、{信息B}和{信息C}。`
- `{工具名}会在{触发时机}时，把{相关上下文}交给{使用者或Agent}。`
- `{工具名}适合{具体人群}、{具体场景}、{具体问题}。`

Avoid sentences that first judge the thing, then explain it with a colon.

Avoid broad endings about a direction, project, or entry point. Replace them with specific signals, actions, or outcomes.

## 禁用冒号标题

不要在正文里用"抽象词+冒号"来组织段落。

抽象词是指：感受、看法、思考、体会、总结、逻辑、原因、收获、判断、体验、观察、领悟、启发、认知、洞察、心得、建议、经验、教训，以及它们的变体。

简单判断：冒号前的词如果删掉不影响理解后面的内容，就是抽象词，不能用。

唯一例外：冒号前的词有具体操作指向，比如：

- `安装教程：`
- `操作步骤：`
- `常见坑：`
- `配置方法：`

## 禁用引号装饰

不要用「」『』【】这类装饰性引号来框关键词或短语。真人发帖不用这些。

唯一例外：引用别人的原话可以用中文引号。

## 感受写法规则

可以有感受，但要写成像真人在说话，不能像AI在套模板。

禁止模板化感受句式：

- "最大的感觉是..."
- "整体感受是..."
- "跑了一圈发现..."
- "用下来的体会是..."
- "最让我惊喜的是..."
- "给我的感觉是..."

更自然的写法：

- "它不怎么聊天，更像帮你盯着东西"
- "用了一周，回测比我想的准"
- "刚开始觉得麻烦，后来发现就三步"

核心区别：模板句是先宣告要说感受，再给内容；自然句是直接把感受融在叙述里。

## 少用单字动词

中文社媒文案里，单字动词太密会显得生硬。尽量用双字词替代。

| 少用 | 可替代 |
|---|---|
| 盯 | 关注 / 监测 / 留意 |
| 准 | 准确 / 靠谱 / 稳 |
| 跑 | 运行 / 执行 / 走通 |
| 装 | 安装 / 装好 |
| 配 | 配置 / 搭配 |
| 改 | 修改 / 调整 |
| 看 | 查看 / 观察 |
| 写 | 编写 / 创作 |
| 调 | 调试 / 调节 |
| 挂 | 部署 / 挂载 |

不是绝对禁用，但一句话里超过两个单字动词，读起来就容易像机翻。

## Financial Writing

Use this section for US stocks, crypto, macro, earnings, AI chips, ETFs, and market recaps.

Do not turn market content into a simple buy/sell or up/down prediction. The post should help readers understand what to watch.

A useful market post should explain:

- What happened.
- What the market expected before it happened.
- Which assets or sectors may be affected.
- Where beginners often misread the event.
- Which signals to watch next.
- What uncertainty or risk remains.

Suggested structure:

1. Give the reader one clear signal to watch.
2. Explain the event in plain language.
3. Explain whether expectations changed.
4. Explain the possible impact chain.
5. Give a short checklist.
6. End with a risk or learning boundary.

Good financial hooks:

- `这周美股别乱看，先看利率预期有没有变。`
- `财报季最容易看错的地方，是只看业绩好不好。`
- `AI芯片还在主线里，但现在不能只看新闻热度。`
- `新手看Fed纪要，别只问降没降息。`

Use a light disclaimer when appropriate:

- `以上不构成投资建议，只做市场学习记录。`

## Layout Playbook

Use this section when the user wants a public account post, Xiaohongshu post, long X post, Threads post, image copy, or infographic outline.

Recommended structure:

1. Title
2. Opening that keeps the reader
3. Body skeleton
4. Closing interaction

Title should make the target reader or concrete benefit clear within 3 seconds.

The body should usually have 3 to 5 key points. Each point should answer one question:

- What is it?
- Why does it matter?
- Where do beginners get it wrong?
- What should the reader actually watch?
- What should the reader do next?

Images should add information, not decoration. Prefer checklists, comparison tables, simple flows, and key signal dashboards. Avoid random AI robot images, exaggerated explosion visuals, fake data charts, and low-information chip photos.

## Banned Words

Do not use these words in final Chinese copy:

- 旨在
- 赋能
- 打造
- 范式
- 这种
- 硬生生
- 扒
- 助力
- 路径
- 逻辑
- 痛点
- 说白了
- 护城河
- 东西（太模糊时禁用，换成具体名词）

## Banned Patterns

Avoid:

- The `不是...而是...` contrast pattern.
- Repeated sentences starting with `当`.
- Repeated openings with `大家以为`.
- Hype-only claims.
- Empty advice without a concrete next step.
- Colon explanations after a vague judgement.
- Generic endings using `这个方向` or `这个入口`.

## Topic Selection

Prefer topics close to current attention:

- AI models
- AI Agent
- AI coding
- AI workflow
- AI automation
- AI design tools
- crypto projects
- airdrops and points
- on-chain tools
- US stocks and macro
- Fed, CPI, earnings season, AI chips
- GitHub open-source projects
- wallets, DeFi, L2, Restaking, SocialFi

A topic should answer at least one of these:

- Who should care?
- What can it do?
- What changed?
- What can the reader try next?
- What risk should the reader avoid?
- Which signal should the reader watch?

## Engagement-first selection

The goal is likes, retweets, comments, and bookmarks. Select content that is inherently shareable:

1. Tools outperform broad opinions when the reader can try them immediately.
2. Numbers hook harder than vague narratives when the number is relevant and trustworthy.
3. Open source and self-hostable tools are easier to bookmark.
4. Market content should lead with a signal readers can track, not a broad prediction.
5. Image posts should make the first screen clear enough to understand without reading every line.

## Platform metrics ban

Never mention platform metrics in the final tweet. No star counts, like counts, comment counts, or view counts. Let the tool's value speak through what it does.

This ban applies only to metrics. It does not forbid including GitHub URLs or project links when the source requires them.

## Hook Guidance

Choose the hook based on the strongest information in the source. Do not force every post into the same opening.

Useful hook types:

- Specific benefit: `这个工具可以把AI写作里的废话先砍掉一半。`
- Personal experience: `我试了几轮，发现空投内容最容易死在第一行。`
- Timely angle: `AI Agent开始接管更多链上操作后，钱包会变得更重要。`
- Audience angle: `如果你经常用AI写中文推文，先把这几类句子删掉。`
- Risk reminder: `很多项目内容不差，问题出在写法太像公告。`
- Finance signal: `这周美股别乱看，先看利率预期有没有变。`

## Value Guidance

The middle part should be specific. Add practical information such as:

- Who it helps
- What it does
- How to use it
- What to check
- What to avoid
- Real examples
- Personal observations
- Reusable methods
- Data or market signals

## CTA Guidance

Use a light CTA. Do not sound like sales copy.

Examples:

- `先收藏，写推文前对照删一遍。`
- `你也可以拿自己的内容试一下，看第一行有没有留住人。`
- `如果你在做AI或crypto内容，这套规则可以直接丢给Agent用。`
- `这周你最关注Fed、财报，还是AI芯片？`

## Process

1. Identify the strongest shareable point in the source.
2. Keep factual information. Do not invent details. If the source has a required URL, include it in the final copy.
3. Write a first line that can hold attention.
4. Rewrite the body into practical, concrete information.
5. If it is financial content, add event, expectation, impact, signal, and risk boundary.
6. If it is image or long-form copy, add title, opening, body skeleton, and closing interaction.
7. Remove banned words and banned patterns.
8. Remove parentheses.
9. Remove spaces around English words in Chinese text.
10. End with a soft CTA.

## Final Check

Before answering, run every check. Re-read the full output character by character. The #1 missed violation in sponsored posts is `不是...而是...`. Never ship without scanning:

- Hook is strong and natural. Does the first line have a concrete object or benefit, not a vague judgment?
- The post has useful information, not just sentiment.
- Links: only include URLs the brief explicitly requires. Do not add links the brief did not ask for.
- CTA is light. No sales language, no `赶紧` or `千万别错过`.
- No parentheses: `（）` or `()`.
- No banned words: 旨在, 赋能, 打造, 范式, 这种, 硬生生, 扒, 助力, 路径, 逻辑, 痛点, 说白了, 护城河.
- No spaces around English words in Chinese text. Scan for `[CJK][space][ASCII]` and `[ASCII][space][CJK]`.
- No `不是...而是...` structure anywhere. Search the output for `不是`. Every hit must be rephrased.
- No vague judgement followed by a colon explanation.
- No generic direction or entry-point ending.
- No AI product review template feel.
- Financial copy has concrete signals and risk boundary.
- Image or long-form copy has clear title, opening, body skeleton, and closing interaction.
- The copy sounds like a real person sharing useful experience, not a balanced review.
