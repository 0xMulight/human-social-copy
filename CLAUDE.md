# Claude使用说明

本仓库是中文社媒文案规则包。写作、改写、润色中文社媒内容时，优先遵守`AGENTS.md`。

如果你在ClaudeCode里使用，把仓库放进项目后，Claude会读取这个文件。需要完整规则时，继续读取`AGENTS.md`。需要句式和示例时，读取`human-social-copy/references/patterns.md`。需要更完整的开头钩子模型时，读取`human-social-copy/references/adaptive-hooks.md`。

如果你在ClaudeProject里使用，直接把`prompts/universal-agent-prompt.md`加入项目知识或自定义指令。

调用示例：

```text
按human-social-copy规则，把下面草稿改成中文社媒文案。
要求保留原稿里已经成立的强钩子。
如果原稿没有好开头，就根据内容自适应选择开头钩子。
使用Hook+干货+CTA结构。
贴近当下热度，可以加入AI相关角度。
去掉AI腔、括号和英文前后空格。
避免先否定再转折的排比。
避免先评价再用冒号解释。
能直接说结果就直接说。
如果我用某个项目举例，只学习句式，不要把项目名写成固定规则。
```
