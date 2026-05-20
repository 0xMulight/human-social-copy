# ✍️ Human Social Copy

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" alt="Status">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/badge/Hermes-skill-8A2BE2" alt="Hermes Skill">
  <img src="https://img.shields.io/badge/language-简体中文-red" alt="Language">
  <img src="https://img.shields.io/badge/Agents-All-brightgreen" alt="Agent Support">
</p>

<p align="center">
  <b>让你的 AI 写出的中文社交文案不再像 AI —— 一套规则，所有 Agent 通用。</b>
</p>

---

## 这是什么

一套中文社交媒体文案规则库。你可以把它交给 Hermes、Claude Code、Codex、Gemini 或任何 AI Agent，让 AI 写出的内容更像真人分享。

### 和普通写作规则的区别

| | 普通提示词 | Human Social Copy |
|---|---|---|
| 覆盖范围 | 单一 Agent | 所有主流 Agent 通用 |
| 维护方式 | 贴在对话里 | Git 版本管理，PR 协作 |
| 规则粒度 | 笼统要求 | 禁用词清单 + 句式替换 + 钩子模板 |
| 学习成本 | 每次重新解释 | clone 即用，Agent 自动读取 |

## 效果对比

**改写前：**

> 这个AI工具旨在赋能创作者打造更高效的视频工作流，它的核心逻辑是通过智能剪辑算法实现视频创作范式的升级，解决了内容生产中的诸多痛点。

**改写后：**

> AI剪辑工具可以把口播视频里的沉默、口误、重复自动剪掉，导出带字幕的成片。自己剪一条 10 分钟视频大概 40 分钟，用它 5 分钟搞定。适合做口播、教程、复盘内容的人。免费版每天 3 条。

## 解决什么问题

| 问题 | 规则里的解法 |
|---|---|
| 开头像公告，没人停留 | 自适应钩子模板，含热点/收益/经验/人群切入 |
| 中间全是套话 | 直给句优先，先给结论 |
| 结尾像销售 | 轻 CTA：收藏、试试、补充经验 |
| 中英文空格混乱 | 强制"AI工具""GitHub项目"格式 |
| 禁用 AI 八股词 | 13 个禁用词清单 |
| 固定句式 | 禁止先评价再冒号解释等 6 种句式 |
| 空泛建议收尾 | 要求给具体信号/动作/入口 |

## 快速开始

发给任何 Agent 一句话：

```text
按 human-social-copy 规则改写这段内容：
https://github.com/0xMulight/human-social-copy
```

根据 Agent 类型读取不同文件：

| Agent | 读取文件 |
|---|---|
| Hermes | `human-social-copy/SKILL.md`（作为 skill 安装） |
| Claude Code | 自动读取 `CLAUDE.md` |
| Codex / OpenAI | `AGENTS.md` 或 `human-social-copy/agents/openai.yaml` |
| Gemini | `GEMINI.md` |
| 任意 Agent | `prompts/universal-agent-prompt.md`（复制到系统提示词） |

## 文件结构

```
human-social-copy/
├── AGENTS.md                          # 通用 Agent 规则
├── CLAUDE.md                          # Claude 入口
├── GEMINI.md                          # Gemini 入口
├── HERMES.md                          # Hermes 入口
├── README.md                          # 项目说明（本文件）
├── LICENSE
├── CONTRIBUTING.md                    # 贡献指南
├── human-social-copy/
│   ├── SKILL.md                       # Hermes Skill 定义
│   ├── agents/
│   │   └── openai.yaml               # OpenAI Agent 配置
│   └── references/
│       ├── patterns.md               # 句式模式参考
│       └── adaptive-hooks.md         # 自适应钩子
├── prompts/
│   └── universal-agent-prompt.md     # 通用 Prompt
├── examples/
│   └── before-after.md              # 🆕 改写前后对比
└── .github/
    └── workflows/
        └── validate-skill.yml        # 🆕 CI 校验
```

## 核心规则速览

**结构**：Hook → 干货 → 轻 CTA

**禁用词 13 个**：旨在、赋能、打造、范式、这种、硬生生、扒、助力、路径、逻辑、痛点、说白了、护城河

**禁用句式 6 种**：先否定再转折排比、"大家以为"开头、"当"字堆砌、先评价再冒号解释、"这个方向"加泛泛建议、空泛判断

**中文规范**：简体中文、英文前后无空格、不用括号、不堆小标题

## 贡献

欢迎 PR 补充更自然的中文表达规则、句式模式或新的 Agent 适配文件。详见 `CONTRIBUTING.md`。

## 许可

MIT © 2026 [0xMulight](https://github.com/0xMulight)
