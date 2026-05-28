# ✍️ Human Social Copy

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" alt="Status">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/badge/Hermes-skill-8A2BE2" alt="Hermes Skill">
  <img src="https://img.shields.io/badge/language-简体中文-red" alt="Language">
  <img src="https://img.shields.io/badge/Agents-All-brightgreen" alt="Agent Support">
  <img src="https://img.shields.io/badge/version-2.10.2-orange" alt="Version">
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
| 规则粒度 | 笼统要求 | 8大钩子模型 + 8类句式模板 + 禁用词清单 |
| 学习成本 | 每次重新解释 | clone 即用，Agent 自动读取 |

## 效果对比

**改写前：**

> 这个AI工具旨在赋能创作者打造更高效的视频工作流，它的核心逻辑是通过智能剪辑算法实现视频创作范式的升级，解决了内容生产中的诸多痛点。

**改写后：**

> AI剪辑工具可以把口播视频里的沉默、口误、重复自动剪掉，导出带字幕的成片。自己剪一条 10 分钟视频大概 40 分钟，用它 5 分钟搞定。适合做口播、教程、复盘内容的人。免费版每天 3 条。

## 解决什么问题

| 问题 | 规则里的解法 |
|---|---|
| 钩子没吸引力 | 8大钩子模型（好奇/痛点/反差/圈定/焦虑/恐惧/高价值/借势）+ 8类50+句式模板库 |
| 正文全是套话 | 直给句优先 + 7类句式模式（patterns.md） |
| 结尾像销售 | 轻 CTA：收藏、试试、补充经验 |
| 中英文空格混乱 | 强制`AI工具``GitHub项目`格式 |
| 禁用 AI 八股词 | 14 个禁用词清单 |
| 固定句式 | 禁止`不是...而是...`、先评价再冒号解释等 |
| 钩子是原创的、没验证 | 必须先走决策表选模型→模板库匹配句式，禁止原创钩子结构 |
| 忘了用参考文件 | 强制先加载4个reference文件再动笔 |
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

## 核心规则速览

### 写作流程

**⒈ 先加载全部 reference → ⒉ 先选钩子（8大模型）→ ⒊ 对照 patterns.md 写正文 → ⒋ Final Check 逐条扫描**

### 钩子：8大核心模型

拿到内容先对号入座，再从模板库匹配句式。**禁止原创钩子结构。**

| 内容特征 | 选这个模型 |
|---|---|
| 有反直觉发现/秘密/内幕 | 好奇模型：只说一半 + 关键留白 |
| 解决一个让人烦的问题 | 痛点模型：精准扎心 + 立刻给方案 |
| 有before/after对比 | 反差模型：过去糟糕 → 现在翻身 |
| 只对特定人群有用 | 圈定受众模型："所有XX的人" |
| 涉及落后/被淘汰焦虑 | 焦虑模型：危机信号 + 来得及 |
| 涉及风险/损失/踩坑 | 恐惧模型：放大坏结果 + 给预防 |
| 有独家数据/方法/干货 | 高价值模型：别处没有的独家 |
| 蹭名人/热点/趋势 | 借势模型：权威背书 |

模板库含8类：情绪冲击、工具实用、反常识、人群点名、结果承诺、亲测实证、稀缺独家、平替省钱。

### 禁用词 14 个

旨在、赋能、打造、范式、这种、硬生生、扒、助力、路径、逻辑、痛点、说白了、护城河、东西（模糊时禁用）

### 禁用句式

`不是...而是...` 对比、`当`字堆砌、`大家以为`开头、先评价再冒号解释、`这个方向`/`这个入口`结尾

### 中文规范

简体中文、英文前后无空格、不用括号、不堆小标题、少量单字动词

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
│   ├── SKILL.md                       # Hermes Skill 定义（v2.10.2）
│   ├── agents/
│   │   └── openai.yaml               # OpenAI Agent 配置
│   └── references/
│       ├── adaptive-hooks.md         # 8大钩子模型 + 8类模板库 + 爆款案例
│       ├── patterns.md               # 7类句式模式 + 反模式
│       ├── sourcing-playbook.md      # 素材挖掘策略 + Surf 查询模板
│       └── kol-brief-workflow.md     # KOL Brief 处理流程 + 赞助帖防翻车
├── prompts/
│   └── universal-agent-prompt.md     # 通用 Prompt
├── examples/
│   └── before-after.md              # 改写前后对比
└── .github/
    └── workflows/
        └── validate-skill.yml        # CI 校验
```

### 4个 Reference 文件

| 文件 | 作用 | 何时使用 |
|---|---|---|
| `adaptive-hooks.md` | 钩子决策表 + 8大模型 + 50+句式模板 + 爆款案例 | 每次写作第1步，钩子不定好不动笔 |
| `patterns.md` | 7类句式模式 + 反模式 | 写正文时对照，不要自由发挥句式 |
| `sourcing-playbook.md` | 素材挖掘策略、查询模板、阈值 | 选题阶段，找工具/项目素材时 |
| `kol-brief-workflow.md` | KOL Brief 处理流程、赞助帖防翻车 | 处理合作推广内容时 |

## 贡献

欢迎 PR 补充更自然的中文表达规则、句式模式或新的 Agent 适配文件。详见 `CONTRIBUTING.md`。

## 许可

MIT © 2026 [0xMulight](https://github.com/0xMulight)
