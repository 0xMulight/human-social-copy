# Claude使用说明

本仓库是中文社媒文案规则包。写作、改写、润色中文社媒内容时，优先遵守`AGENTS.md`。

如果你在ClaudeCode里使用，把仓库放进项目后，Claude会读取这个文件。需要完整规则时，继续读取`AGENTS.md`。需要模板和示例时，读取`human-social-copy/references/patterns.md`。

如果你在ClaudeProject里使用，直接把`prompts/universal-agent-prompt.md`加入项目知识或自定义指令。

调用示例：

```text
按human-social-copy规则，把下面草稿改成中文社媒文案。要求保留原稿里已经成立的强钩子，钩子加干货加CTA，贴近当下热度，加入AI相关角度，去掉AI腔和英文前后空格。
```