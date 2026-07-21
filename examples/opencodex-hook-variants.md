# opencodex 六种钩子变体

同一个工具 opencodex，用六种不同钩子角度去写。展示平级感钩子模板库的实际应用。

工具简介：opencodex 是一个本地代理，让 Codex CLI/App 和 Claude Code 可以使用任何 LLM（DeepSeek、Claude、Gemini、Grok 等），不再锁定 OpenAI。

---

## A. 丢人坦白型

说实话我之前一直以为Codex只能用OpenAI的模型，还特意充了ChatGPT Plus，结果公司给的是DeepSeek的API额度，每个月看着那个额度在那躺着用不了。

前两天同事说opencodex可以让Codex跑任何模型。我一装，还真是。npm全局装完、ocx init选DeepSeek、ocx start，Codex就自动走DeepSeek了。我之前充的ChatGPT Plus直接可以停了。

Claude Code也能用，Gemini、Grok、Ollama随便切。Web面板点两下换模型，不用改任何Codex配置。

有公司API额度的、想省OpenAI订阅费的，这个可能比等官方支持快多了。

**钩子分析**：A 类——说实话我之前一直不知道/搞错了XX → 才发现 → 验证后真香。适合反常识技巧和隐藏功能。

---

## B. 偶然发现型

本来是在GitHub上搜Codex的prompt技巧，结果看到有人用opencodex让Codex跑了Claude模型。我当时就想，Codex不是OpenAI家的吗怎么可能。

点进去发现它是个本地代理，把Codex的请求转成你选的模型能懂的格式。装完之后Codex完全不知道自己在跟DeepSeek还是Gemini说话，照常用。

最夸张的是Claude Code也能接，在它那个dashboard里点两下，Claude Code就直接调用DeepSeek了。40多个模型来回切，不用等任何官方适配。

用惯了DeepSeek又想用Codex工作流的，拿opencodex搭个桥就行了。

**钩子分析**：D 类——本来在找XX → 无意间看到 → 试了一下发现比XX好用多了。适合替代工具和新发现。

---

## C. 朋友安利型

群里一个做独立开发的朋友截图说他Codex在用DeepSeek跑，一个月token费才几十块。我以为他吹牛，Codex不是只能接OpenAI吗。

结果他甩了个GitHub链接过来，说装个opencodex就行。我试了一下，真的就是npm全局装、ocx init、ocx start三步，Codex就开始走DeepSeek了。代码能力跟用OpenAI没差，费用差了快十倍。

他说之前Codex + ChatGPT Plus一个月两百多，现在DeepSeek API几十块搞定，Claude Code也能接进去。

https://github.com/lidge-jun/opencodex

公司有DeepSeek API额度的、不想续ChatGPT Plus的，试试这个。

**钩子分析**：E 类——群里/朋友/同事发给我的 → 一开始不信 → 试了发现真有用。适合冷门好工具、有真实数字对比。

---

## D. 对比打脸型

用了半年的ChatGPT Plus配合Codex，一个月固定20刀，加上API超量偶尔飙到四五十。上个月发现opencodex之后，同一个Codex、一样的代码质量，走DeepSeek API一个月才花了几十块人民币。

打开账单对比差点没吐血。

没啥技术门槛，npm装完、ocx init选模型、ocx start，Codex就自动走了。Claude Code同理，Gemini、Grok都能接。

现在Plus续费提醒弹出来直接划掉。

**钩子分析**：F 类——用了X年的XX → 最近才知道有免费的YY能替代 → 省了几千块。适合免费替代和省钱方案。

---

## E. 反常识型

不是吧，Codex还能用DeepSeek跑？

之前一直以为Codex是OpenAI亲儿子只能接自家模型，结果opencodex就是个本地翻译层，Codex发出的请求它转成DeepSeek/Gemini/Claude能懂的格式，模型回的内容它再转回来。Codex完全不知道自己在对谁说话。

装完三步走，之后就跟原生支持一样。Claude Code也能这样玩——在opencodex面板里点一下，Claude Code就跑去调用DeepSeek了。

40多个模型随便接，Ollama本地模型也行。Codex从此不是OpenAI专属了。

**钩子分析**：G 类——"不是吧，XX还能这样？" 直接挑战一个普遍假设，然后用事实推翻。跟丢人坦白型的区别：丢人坦白是"我不知道"，反常识是"我以为所有人都这么想，结果发现有例外"。

---

## F. 被逼无奈型

上周Codex Plus限流，一天只能用50次，下午三点额度就没了，任务做一半卡在那。

死马当活马医搜到opencodex，说是能让Codex走别的模型。装完切到DeepSeek，后半段任务正常跑完。第二天发现token费还不到Plus一天的订阅钱。

现在日常用DeepSeek，需要强推理的时候才临时切回Claude或OpenAI。Claude Code也接进去了，一个ocx start全搞定。

Plus还在续的可以先装这个试一天，看看账单差多少。

**钩子分析**：C 类——XX客户/老板/紧急情况突然要我做什么 → 只剩X小时 → 死马当活马医试了这个 → 居然成了。适合紧急场景和省时工具。

---

## 六种钩子对照

| 变体 | flat-hooks类型 | 核心情绪 | 适用场景 |
|---|---|---|---|
| A | 丢人坦白型 | 羞愧→解脱 | 反常识技巧、隐藏功能 |
| B | 偶然发现型 | 意外→惊喜 | 替代工具、新发现 |
| C | 朋友安利型 | 怀疑→信服 | 冷门好工具、有真实数字对比 |
| D | 对比打脸型 | 后悔→行动 | 免费替代、省钱方案 |
| E | 反常识型 | 震惊→兴奋 | 打破认知、重新定义品类 |
| F | 被逼无奈型 | 紧迫→获救 | 紧急场景、效率工具 |

同一个工具，换一个钩子角度，完全不同的阅读体验。写之前先想清楚这条内容最强的情绪引擎是什么，然后对号入座选钩子。
