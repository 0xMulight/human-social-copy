# 贡献说明

欢迎改进这个中文社媒文案Agent规则包。

这个仓库维护一套中文社交媒体文案写作规则，主要让内容更像真人写的经验分享，少一点模板感和AI腔。

## 可以贡献什么

- 补充更自然的中文表达规则
- 增加更实用的社媒文案模板
- 优化开头钩子、标题选择和第一句自检规则
- 优化crypto、空投、AI工具、AI模型更新、AI工作流、AI coding内容的写法
- 删除容易显得空泛、夸张、套路化的表达
- 修正文案里的错别字、表述不清或重复内容
- 补充Claude、Gemini、Hermes等Agent的使用说明

## 修改原则

- 保持简体中文。
- 语言要朴素，不要堆漂亮词。
- 钩子可以有冲突感、结果感和反差感，但不能靠空泛夸张撑场面。
- 第一句要让读者知道：这篇内容和我有什么关系，能解决什么问题，为什么要继续看。
- 中文和英文单词或缩写之间不要留空格。
- 优先使用直给句，直接说明主语能做什么。
- 用户拿某个项目举例时，只学习句式和判断方法，不要把项目名写成固定规则。
- 避免先评价项目，再用冒号解释功能。
- 避免用空泛建议收尾，要给具体信号、动作或结果。
- 不要加入“互推、助推、找人转发”这类分发规则。
- 不要加入夸张、绝对化、制造焦虑的表达。
- 修改后尽量检查一遍禁用词、括号和英文单词前后空格。
- 如果改了核心规则，尽量同步更新`AGENTS.md`、`prompts/universal-agent-prompt.md`和`human-social-copy/SKILL.md`。
- 如果改了开头钩子、标题模型或图片里的钩子方法，优先更新`human-social-copy/references/adaptive-hooks.md`。

## 文件说明

- `AGENTS.md`是通用Agent规则。
- `CLAUDE.md`是Claude入口。
- `GEMINI.md`是Gemini入口。
- `HERMES.md`是Hermes入口。
- `prompts/universal-agent-prompt.md`是可复制的完整提示词。
- `human-social-copy/SKILL.md`是CodexSkill核心规则。
- `human-social-copy/agents/openai.yaml`是技能展示信息。
- `human-social-copy/references/adaptive-hooks.md`是自适应开头钩子规则。
- `human-social-copy/references/patterns.md`是句式和示例。

## 提交建议

提交信息可以用中文，比如：

```text
优化中文写作规则
补充空投文案模板
补充Claude使用入口
修正README说明
```
