# 真人感社媒文案Agent规则包

这是一个通用的中文社媒文案规则包，Codex、Claude、Gemini、Hermes和其他支持自定义提示词的Agent都可以用。

它适合把草稿、笔记、截图内容、项目资料、AI工具体验、crypto内容、空投内容、教程或粗略想法，改成更像真人写的中文社媒内容。

重点很简单：第一行抓住注意力，中间给有用信息，结尾引导一个动作。语言要朴素、克制、可信。改写时优先保留原稿里已经成立的强钩子；原稿开头偏弱时，再按内容选择更合适的开头。

## 这个仓库能做什么

它可以帮助Agent在写中文社媒内容时稳定做到：

- 按钩子加干货加CTA输出
- 第一行抓住读者注意力，但不夸张
- 根据文章类型、目标读者、核心收益和可信证据选择开头
- 保留原稿里有结果感、场景感、读者收益的强钩子
- 第一行优先写读者能得到的变化，少写泛泛提醒
- 中间给真实经验、步骤、清单、判断标准、限制或注意事项
- 结尾只引导一个动作，比如评论、收藏、关注、分享、尝试、提问
- 去掉明显AI腔、空话、套话和过度修饰
- 用户没有要求时，不写线程
- 清理括号和括号里的补充说明
- 减少分类小标题，让内容更像自然分享
- 避免“大家以为”这类老套开头
- 避免先否定再转折强调的排比句式
- 少用“当”字开头的句子
- 删除“旨在、赋能、打造、范式、这种、硬生生、扒、助力、路径、逻辑、痛点、说白了、护城河”等常见AI词
- 去除英文单词或缩写前后的空格，比如把“AI 腔”改成“AI腔”，把“加 CTA”改成“加CTA”

## 适合哪些内容

- X帖子
- Threads帖子
- Instagram文案
- TikTok口播稿
- 小红书笔记草稿
- cryptoYap内容
- 空投解析
- 项目观察
- 工具教程
- AI工具体验
- AI模型更新解读
- AI工作流分享
- 个人经验复盘
- 社群公告改写
- 把AI草稿改得更像真人表达

## 选题规则

写社媒内容时，优先看两点：

1. 内容要对读者有用

教程、工具、清单、避坑、案例、数据整理、真实体验，通常比泛泛观点更容易被读者看完。

2. 选题要贴近当下热度

可以结合市场正在讨论的话题、项目更新、空投规则变化、任务变化、代币消息、AI模型更新、AI工具发布、AI新玩法，或者社区里反复出现的问题。

写AI内容时，不要编模型能力、发布时间、价格、上下文长度、产品功能或官方承诺。需要最新事实时先核实；核实不了就提醒用户哪些信息需要确认。

## 如何使用

不同Agent没有统一安装格式，所以这个仓库同时提供了通用提示词和常见Agent入口文件。

### 直接给AI仓库链接

如果你的AI可以访问GitHub，可以直接把仓库链接发给它：

```text
请读取这个仓库里的规则，并按它来改写我的中文社媒文案：
https://github.com/0xMulight/human-social-copy
```

更稳一点可以这样说：

```text
请优先读取这个仓库的AGENTS.md和prompts/universal-agent-prompt.md，然后按human-social-copy规则帮我写中文社媒文案。
https://github.com/0xMulight/human-social-copy
```

如果AI打不开GitHub链接，就复制`prompts/universal-agent-prompt.md`里的内容给它。

### 通用方式

打开`prompts/universal-agent-prompt.md`，把全文复制到你的Agent系统提示词、自定义指令、Project知识、Gem或Agent说明里。

调用时可以这样说：

```text
按human-social-copy规则，把下面草稿改成中文社媒文案。要求保留原稿里已经成立的强钩子；如果原稿没有好开头，就根据文章内容自适应选择开头钩子；钩子加干货加CTA，贴近当下热度，加入AI相关角度，去掉AI腔和英文前后空格。
```

### 仓库读取方式

把这个仓库加入Agent工作区，让Agent读取这些文件：

- `AGENTS.md`：通用Agent规则
- `CLAUDE.md`：ClaudeCode入口
- `GEMINI.md`：GeminiCLI入口
- `HERMES.md`：Hermes或其他自定义Agent入口
- `human-social-copy/references/patterns.md`：模板和示例
- `human-social-copy/references/adaptive-hooks.md`：自适应开头钩子模型

### CodexSkill方式

把`human-social-copy`文件夹放到Codexskills目录后，可以这样调用：

```text
使用$human-social-copy，把这段草稿改成保留强钩子、能根据文章内容自适应选择开头、钩子加干货加CTA的中文社媒文案。
```

## 仓库结构

```text
AGENTS.md
CLAUDE.md
GEMINI.md
HERMES.md
prompts/universal-agent-prompt.md
human-social-copy/
  SKILL.md
  agents/openai.yaml
  references/adaptive-hooks.md
  references/patterns.md
```

## 文件说明

`AGENTS.md`是通用Agent入口，适合Codex、Claude、Gemini、Hermes和其他能读取仓库文件的Agent。

`prompts/universal-agent-prompt.md`是可复制的完整提示词，适合放进任何支持自定义提示词的Agent。

`CLAUDE.md`、`GEMINI.md`、`HERMES.md`分别给对应Agent提供快速入口。

`human-social-copy/SKILL.md`是CodexSkill核心规则，决定Codex什么时候使用这个Skill，以及写作时必须遵守哪些要求。

`human-social-copy/agents/openai.yaml`是技能展示信息，包含名称、简介和默认调用提示。

`human-social-copy/references/adaptive-hooks.md`是自适应开头钩子参考，放了好奇、问题、反差、圈定受众、风险提醒、高价值、借势、数字清单等模型。

`human-social-copy/references/patterns.md`是参考模板，放了常用开头、第一行选择、基础公式、cryptoYap文案结构、AI内容文案结构和改写检查清单。

`CONTRIBUTING.md`是贡献说明，方便别人知道怎么改这个规则包。

`LICENSE`是MIT开源协议。

## License

MIT
