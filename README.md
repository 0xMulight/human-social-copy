# ✍️ Human Social Copy

<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" alt="Status">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/badge/Hermes-skill-8A2BE2" alt="Hermes Skill">
  <img src="https://img.shields.io/badge/language-简体中文-red" alt="Language">
  <img src="https://img.shields.io/badge/Agents-All-brightgreen" alt="Agent Support">
  <img src="https://img.shields.io/badge/version-2.12.0-orange" alt="Version">
</p>

<p align="center">
  <b>让你的AI写出的中文社交文案不再像AI，也更像你本人。</b>
</p>

---

## 这是什么

一套中文社交媒体文案规则库。你可以把它交给Hermes、Claude Code、Codex、Gemini或任何AI Agent，让AI写出的内容更像真人分享。

它适合X、Threads、Instagram、TikTok，也适合AI工具、GitHub项目、crypto、空投、美股、宏观、财报、市场复盘和图文内容。

这套规则分两层：

1. 通用表达规则：去AI味、去套话、保留具体信息。
2. 个人语气系统：从用户旧内容里提取语气画像，让AI写得更像用户本人。

### 和普通写作规则的区别

| | 普通提示词 | Human Social Copy |
|---|---|---|
| 覆盖范围 | 单一Agent | 所有主流Agent通用 |
| 维护方式 | 贴在对话里 | Git版本管理，PR协作 |
| 规则粒度 | 笼统要求 | 钩子、句式、禁用词、金融规则、图文排版、个人语气 |
| 学习成本 | 每次重新解释 | clone即用，Agent自动读取 |
| 语气控制 | 只能要求“像真人” | 先提取用户语气画像，再按语气画像生成 |

## 效果对比

**改写前：**

> 这个AI工具旨在赋能创作者打造更高效的视频工作流，它的核心逻辑是通过智能剪辑算法实现视频创作范式的升级，解决了内容生产中的诸多痛点。

**改写后：**

> AI剪辑工具可以把口播视频里的沉默、口误、重复自动剪掉，导出带字幕的成片。自己剪一条10分钟视频大概40分钟，用它5分钟搞定。适合做口播、教程、复盘内容的人。免费版每天3条。

## 解决什么问题

| 问题 | 规则里的解法 |
|---|---|
| 钩子没吸引力 | 先判断内容特征，再从钩子参考里选更适合的开头 |
| 正文全是套话 | 直给句优先，对照`patterns.md`写具体信息 |
| 结尾像销售 | 轻CTA：收藏、试试、补充经验 |
| 中英文空格混乱 | 强制`AI工具``GitHub项目`格式 |
| 禁用AI八股词 | 14个禁用词清单 |
| 固定句式 | 禁止`不是...而是...`、先评价再冒号解释等 |
| 金融内容空泛 | 用`finance-writing.md`拆事件、预期、影响、观察信号和风险提示 |
| 图文排版松散 | 用`layout-playbook.md`整理标题、开头、正文骨架、结尾互动和配图 |
| AI写不像本人 | 用`voice-system.md`建立语气画像，再按用户语气生成 |
| 选题没有动作 | 用`sourcing-playbook.md`先判断读者能不能马上理解、收藏或尝试 |
| 合作内容像广告 | 用`kol-brief-workflow.md`把brief卖点改成具体场景和风险边界 |

## 快速开始

发给任何Agent一句话：

```text
按human-social-copy规则改写这段内容：
https://github.com/0xMulight/human-social-copy
```

如果要让AI写出自己的语气，先用这个Prompt采集语气：

```text
使用prompts/voice-capture-prompt.md，分析我过去写过的5到10篇内容，生成我的个人语气画像。
```

再用这句话生成内容：

```text
按我的个人语气画像和human-social-copy规则，改写下面这段内容。
```

根据Agent类型读取不同文件：

| Agent | 读取文件 |
|---|---|
| Hermes | `human-social-copy/SKILL.md` |
| Claude Code | 自动读取`CLAUDE.md` |
| Codex/OpenAI | `AGENTS.md`或`human-social-copy/agents/openai.yaml` |
| Gemini | `GEMINI.md` |
| 任意Agent | `prompts/universal-agent-prompt.md` |
| 语气采集 | `prompts/voice-capture-prompt.md` |

## 核心规则速览

### 写作流程

**⒈ 先加载reference → ⒉ 有旧内容先提取语气画像 → ⒊ 选钩子 → ⒋ 对照句式写正文 → ⒌ 按内容类型补金融或排版规则 → ⒍ Final Check逐条扫描**

### 个人语气优先级

写作时优先级如下：

1. 事实准确
2. 用户语气
3. 内容结构
4. 平台适配
5. 传播性

如果传播性会破坏用户语气，优先保留用户语气。

### 钩子

拿到内容先对号入座。不要把所有内容都写成同一种开头。

| 内容特征 | 优先写法 |
|---|---|
| 有热点 | 热点切入，但第一句必须有具体对象 |
| 有风险或误区 | 风险提醒，先说新手容易错在哪 |
| 有工具或项目 | 直接写能做什么、适合谁 |
| 有经验复盘 | 先写真实观察或具体结果 |
| 有金融事件 | 先写该看哪个信号，不要直接预测涨跌 |
| 有长图文 | 先用标题和开头留人，再控制正文重点 |
| 有个人旧内容 | 先提取语气画像，再生成新内容 |

### 禁用词14个

旨在、赋能、打造、范式、这种、硬生生、扒、助力、路径、逻辑、痛点、说白了、护城河、东西（模糊时禁用）

### 禁用句式

`不是...而是...`对比、`当`字堆砌、`大家以为`开头、先评价再冒号解释、`这个方向`/`这个入口`结尾。

### 中文规范

简体中文、英文前后无空格、不用括号、不堆抽象小标题、少用单字动词。

## 文件结构

```
human-social-copy/
├── AGENTS.md                          # 通用Agent规则
├── CLAUDE.md                          # Claude入口
├── GEMINI.md                          # Gemini入口
├── HERMES.md                          # Hermes入口
├── README.md                          # 项目说明
├── LICENSE
├── CONTRIBUTING.md                    # 贡献指南
├── human-social-copy/
│   ├── SKILL.md                       # Hermes Skill定义
│   ├── agents/
│   │   └── openai.yaml                # OpenAI Agent配置
│   └── references/
│       ├── adaptive-hooks.md          # 钩子判断和开头参考
│       ├── patterns.md                # 句式模式和反模式
│       ├── finance-writing.md         # 美股/加密/宏观/财报内容规则
│       ├── layout-playbook.md         # 图文排版和信息图规则
│       ├── voice-system.md            # 个人语气采集和复用规则
│       ├── sourcing-playbook.md       # 素材挖掘和选题判断
│       └── kol-brief-workflow.md      # KOL Brief处理和赞助帖防翻车
├── prompts/
│   ├── universal-agent-prompt.md      # 通用Prompt
│   └── voice-capture-prompt.md        # 个人语气采集Prompt
├── examples/
│   └── before-after.md                # 改写前后对比
└── .github/
    └── workflows/
        └── validate-skill.yml         # CI校验
```

## Reference文件

| 文件 | 作用 | 何时使用 |
|---|---|---|
| `adaptive-hooks.md` | 钩子判断、开头类型、第一行自检 | 每次写作第1步 |
| `patterns.md` | 直给句、人群加动作、经验开头、轻CTA | 写正文时对照 |
| `finance-writing.md` | 金融事件、财报、AI芯片、加密内容写法 | 写美股、宏观、财报、crypto时 |
| `layout-playbook.md` | 标题、开头、正文骨架、结尾互动、配图 | 写公众号、小红书、长推或图文时 |
| `voice-system.md` | 语气画像、两阶段提示、平台提示词生成 | 要让AI写得像用户本人时 |
| `sourcing-playbook.md` | 选题、素材判断、搜索方向、信息整理 | 选题阶段 |
| `kol-brief-workflow.md` | brief拆解、卖点翻译、风险边界、披露 | 处理合作推广内容时 |

## 贡献

欢迎PR补充更自然的中文表达规则、句式模式、金融内容规则、图文排版规则、个人语气系统或新的Agent适配文件。详见`CONTRIBUTING.md`。

## 许可

MIT © 2026 [0xMulight](https://github.com/0xMulight)
