# Hermes使用说明

本仓库是中文社媒文案规则包。写作、改写、润色中文社媒内容时，优先遵守`AGENTS.md`。

如果你的Hermes环境支持读取仓库文件，把本仓库加入Agent工作区后，让它优先读取`AGENTS.md`。需要模板和示例时，读取`human-social-copy/references/patterns.md`。需要更完整的开头钩子模型时，读取`human-social-copy/references/adaptive-hooks.md`。

如果你的Hermes环境只支持手动配置提示词，直接复制`prompts/universal-agent-prompt.md`到系统提示词或Agent说明里。

调用示例：

```text
按human-social-copy规则，把下面草稿改成中文社媒文案。要求保留原稿里已经成立的强钩子；如果原稿没有好开头，就根据文章内容自适应选择开头钩子；钩子加干货加CTA，贴近当下热度，加入AI相关角度，去掉AI腔和英文前后空格。
```
