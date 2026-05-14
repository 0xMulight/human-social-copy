# Human Social Copy

Use this skill when the user wants Chinese social media copy, thread writing, tweet/post optimization, Xiaohongshu-style hooks, or rewrites that should sound human, specific, and engaging.

## Core Principle

The first line decides whether people keep reading. It must show who this is for, what problem it helps with, and why the reader should care now.

Good social copy should be attractive and credible at the same time. The attraction should come from specific facts: a concrete person, scene, result, risk, bug, tool, community, or decision point.

## Default Workflow

1. Extract the factual payload: project, tool, audience, scene, problem, result, evidence.
2. Choose the strongest hook angle from `references/adaptive-hooks.md`.
3. Draft three opening options: steady, catchy, strong.
4. Use the catchy-but-credible version unless the user asks for a conservative tone.
5. Build the post with short paragraphs, numbered points when useful, and concrete nouns.
6. Check against the banned-template list before final output.

## Hook Rules

A hook may use conflict, result, contrast, risk, or curiosity, but it cannot rely on vague hype.

Prefer hooks like:

- `{project/tool} 里真正值钱的，是 {specific signal/result}`.
- `关注 {field/project} 的人，{entry/tool} 值得先盯。`
- `{scenario} 卡住时，先看 {method/entry}，能少踩 {specific pitfall}。`
- `{tool/project} 的早期问题，往往会先在 {community/issue/meeting} 里露出来。`

Avoid opening with:

- 很多人 / 大家都 / 大多数人
- 别只当成 / 别只把 / 别再以为
- 不是……而是……
- 不是普通 X，更像 Y
- X 不在……而在……
- 简单讲 / 简单理解 / 简单说
- 千万不要 / 99% 的人 / 全网最（unless the source proves it）

## Strength Control

If the copy feels too flat, strengthen it by adding one of these:

- A sharper audience: `正在装 Agent Wallet 的开发者` beats `对 Arc 感兴趣的人`.
- A clearer result: `更早看到 bug 和修复节奏` beats `了解社区动态`.
- A real conflict: `只看公告会漏掉社区里的早期反馈` beats `社区信息很多`.
- A concrete scene: `Office Hour / Windows npm module bug / community.arc.network` beats `生态活动`.

Do not strengthen by adding empty adjectives. Strengthen by making the reader see the practical stake.

## Rewrite Boundaries

When using reference posts:

- Borrow structure, not sentences.
- Borrow hook type, not phrasing.
- Borrow rhythm, not the author’s口头禅.
- Avoid copying the same opening, transition, or conclusion pattern.

## Output Standards

Before replying, verify:

- The first line is not a generic intro.
- The hook is attractive enough for social media.
- The wording does not trigger banned templates.
- Strong claims are tied to concrete facts.
- The result could plausibly be posted without sounding like AI.

When the user asks to optimize repository rules, update `AGENTS.md`, `prompts/universal-agent-prompt.md`, and relevant files in `human-social-copy/references/` so the behavior is consistent across entry points.
