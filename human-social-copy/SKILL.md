---
name: human-social-copy
description: "将 AI/工具/crypto 内容写成真人风格的中文社交媒体文案。用于写推文、X帖子、中文社交分享。"
version: 2.7.0
author: 0xMulight
metadata:
  hermes:
    tags: [writing, social-media, chinese, tweet, x, humanize, copywriting]
    category: social-media
    triggers:
      - "写推文"
      - "写推特"
      - "写成帖子"
      - "发推"
      - "社交媒体文案"
      - "中文推文"
      - "tweet"
      - "推文"
---

# Human Social Copy

Use this skill when the user wants Chinese social media copy that feels human, practical, and ready to post. It works for X, Threads, Instagram, TikTok, crypto yap, airdrop analysis, AI tools, GitHub projects, product notes, and personal experience posts.

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

不要在正文里用 **"抽象词 + 冒号"** 来组织段落。

抽象词是指：感受、看法、思考、体会、总结、逻辑、原因、收获、判断、体验、观察、领悟、启发、认知、洞察、心得、建议、经验、教训……以及它们的变体（"一个感受""两点思考""三个原因""最大收获"）。

简单判断：**冒号前的词如果删掉不影响理解后面的内容，就是抽象词，不能用。**

唯一例外：冒号前的词有**具体操作指向**，比如：
- `安装教程：` `操作步骤：` `常见坑：` `配置方法：`
- 这类词删掉后读者无法判断后面是什么内容，允许使用。

---

## 禁用引号装饰

不要用「」『』【】这类装饰性引号来框关键词或短语。真人发帖不用这些。

❌ `「帮我看BTC和ETH的预测面板」`
✅ `帮我看BTC和ETH的预测面板`

唯一例外：引用别人的原话可以用引号，但用中文引号" "而非装饰引号。

---

## 感受写法规则

可以有感受，但要写成像真人在说话，不能像 AI 在套模板。

❌ 模板化感受句式（禁止）：
- "最大的感觉是..."
- "整体感受是..."
- "跑了一圈发现..."
- "用下来的体会是..."
- "最让我惊喜的是..."
- "给我的感觉是..."

✅ 自然的感受写法：
- "它不怎么聊天，更像帮你盯着东西"
- "用了一周，回测比我想的准"
- "刚开始觉得麻烦，后来发现就三步"

核心区别：模板句是先宣告"我要说感受了"再给内容，自然句是直接把感受融在叙述里。

---

## 少用单字动词

中文社媒文案里，单字动词显得生硬、像机器翻译。尽量用双字词替代。

| ❌ 单字 | ✅ 双字 |
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

不是绝对禁用，但如果一句话里超过两个单字动词，读起来就像机翻。

---

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
- GitHub open-source projects
- wallets, DeFi, L2, Restaking, SocialFi

A topic should answer at least one of these:

- Who should care?
- What can it do?
- What changed?
- What can the reader try next?
- What risk should the reader avoid?

### Engagement-first selection

The goal is likes, retweets, comments, and bookmarks. Select content that is inherently shareable:

1. **Tools > Opinions.** A GitHub repo with a concrete stat (e.g. "98% fewer tokens") outperforms a philosophical essay every time. Pick tools, extensions, libraries, CLI apps — things people can try immediately.
2. **Numbers hook harder than narratives.** "比grep省98% token" gets retweeted. "AI is a technology not a product" gets scrolled past. Pull the strongest quantifiable claim from the source and lead with it.
3. **Open source + self-hostable = bookmarks.** Tools people can clone and run themselves get saved for later.
4. **Show HN / Launch HN projects** are gold — they are fresh, unposted, and the author is hungry for attention (they will engage with your tweet).

### Accessibility filter (CRITICAL)

Every selected topic must pass the **grandma test**: can a non-technical person understand what this tool does and why they'd want it, in under 10 seconds?

Pass: VoiceBox (clone any voice for free), GPT Image tools (generate images from text), AI writing tools, video generators, photo editors.
Fail: multi-agent orchestration engines, LLM inference frameworks, architecture visualizers, code search tools, anything with "framework" or "orchestration" or "pipeline" in the pitch.

The user explicitly rejected architecture/developer content: "什么什么架构 我看了都不懂". If the best item in the scout results is a developer framework, keep scrolling.

### What to skip (anti-patterns)

Do NOT write tweets about:

- Opinion essays, think-pieces, "AI is X not Y" hot takes
- Philosophy-of-AI articles (e.g. "I don't think AI will make your processes go faster")
- News about partnerships, funding rounds, or corporate announcements (unless the user explicitly asks)
- **Architecture, frameworks, orchestration engines** — anything where the pitch is "build/deploy/orchestrate" rather than "use/enjoy/create"
- **Developer-only tools** — code search, CI plugins, LSP servers, build tools. If only an engineer would bookmark it, skip it.
- Anything that cannot answer "what can the reader try next?"
- Content where the only shareable angle is "this is interesting to think about"

If the best item in the scout results is an opinion piece or developer tool, keep scrolling until you find a tool a regular person would want to try.

### Sourcing strategy

See `references/sourcing-playbook.md` for concrete queries, thresholds, and the VoiceBox case study.

GitHub API and HN are biased toward developer tools. For consumer-facing AI tools, Twitter/Surf social with natural-language queries consistently outperforms:

Good queries: "AI image generator free", "AI video tool free", "AI voice clone app", "best free AI tools"
Bad queries: "topic:ai+stars:>50" (returns frameworks), "AI tool open source" (returns dev tools)

The winning pattern from this session: a Surf social hit for an "open-source alternative to paid tool X" (VoiceBox replacing ElevenLabs) had 26k+ GitHub stars and 400+ Twitter likes — consumer-friendly, free, replaces a known paid product. This is the ideal content shape.

### Platform metrics ban

Never mention platform metrics (star counts, like counts, comment counts) in the final tweet. No "HN上277赞93评论", no "GitHub 26k stars", no "Twitter 400 likes". The tool's value must speak for itself through what it does, not through social proof numbers. Let the reader discover the popularity on their own.

⚠️ **This ban applies ONLY to numbers/metrics. It does NOT forbid including GitHub/URL links.** The link itself (e.g. `github.com/author/repo`) must always be present in tool tweets — the reader needs to know where to find the tool. Just don't mention how many stars it has.

⚠️ **This ban applies ONLY to numeric metrics (star counts, like counts, comment counts, view counts). It does NOT forbid including the GitHub URL or project link itself. If the source is a GitHub project, always include the GitHub URL in the final copy — just don't say how many stars it has.** This rule has been misinterpreted by agents as "don't link to GitHub" in past sessions, causing links to be omitted from delivered tweets. Link = required. Metrics = banned.

## Hook Guidance

Choose the hook based on the strongest information in the source. Do not force every post into the same opening.

Useful hook types:

- Specific benefit: `这个工具可以把AI写作里的废话先砍掉一半。`
- Personal experience: `我试了几轮，发现空投内容最容易死在第一行。`
- Timely angle: `AI Agent开始接管更多链上操作后，钱包会变得更重要。`
- Audience angle: `如果你经常用AI写中文推文，先把这几类句子删掉。`
- Risk reminder: `很多项目内容不差，问题出在写法太像公告。`

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

## CTA Guidance

Use a light CTA. Do not sound like sales copy.

Examples:

- `先收藏，写推文前对照删一遍。`
- `你也可以拿自己的内容试一下，看第一行有没有留住人。`
- `如果你在做AI或crypto内容，这套规则可以直接丢给Agent用。`
- `有更像真人的写法，也可以直接提PR补进去。`

## Process

1. Identify the strongest shareable point in the source.
2. Keep factual information. Do not invent details. If the source has a URL (GitHub, official site, etc.), include it in the final copy.
3. Write a first line that can hold attention.
4. Rewrite the body into practical, concrete information.
5. Remove banned words and banned patterns.
6. Remove parentheses.
7. Remove spaces around English words in Chinese text.
8. Include the source URL (GitHub/project link) on its own line before the CTA.
9. End with a soft CTA.

## Final Check

Before answering, run every check. **Re-read the full output character by character.** The #1 missed violation in sponsored posts is `不是...而是...` — agents skip it because the contrast "feels natural" in Chinese, but it's banned. Never ship without scanning:

- Hook is strong and natural. Does the first line have a concrete object or benefit, not a vague judgment?
- The post has useful information, not just sentiment.
- **Links: only include URLs the brief explicitly requires.** Do not add links the brief didn't ask for.
- CTA is light — no sales language, no "赶紧" / "千万别错过".
- No parentheses — `（）` or `()`.
- No banned words: 旨在, 赋能, 打造, 范式, 这种, 硬生生, 扒, 助力, 路径, 逻辑, 痛点, 说白了, 护城河.
- No spaces around English words in Chinese text. Scan for `[CJK][space][ASCII]` and `[ASCII][space][CJK]`.
- **No `不是...而是...` structure anywhere.** Search the output for the substring `不是`. Every hit must be rephrased.
- No vague judgement followed by a colon explanation.
- No generic direction or entry-point ending.
- No "AI product review template" feel: no paired pros/cons paragraphs, no numbered takeaways, no "几个让我留下来的点" / "当然也有还在磨合的地方" structure.
- The copy sounds like a real person sharing useful experience, not a balanced review.
