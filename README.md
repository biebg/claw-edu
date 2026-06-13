# 🦐 养虾指南 · 手把手教你用 AI 助手把活干得又快又好

一个**单文件、零依赖**的交互式入门网页，写给**第一次接触 AI、不懂技术的普通人**。把「怎么用好公司里的 AI 助手（OpenClaw / Hermes 类工具）」讲成一个轻松的「养虾」养成过程。设计风格参考 [coze.cn](https://www.coze.cn)。

> 这里的「虾」= 你工作里能用的那个 AI 助手。本页围绕三件最常见的活展开：**写周报、看数据、写材料**。

## 怎么打开

双击 `index.html` 用浏览器打开即可。或起个本地服务器：

```bash
python3 -m http.server 4173   # 然后访问 http://localhost:4173
```

## 内容结构（六关 + 一个小测）

| 关卡 | 主题 | 给普通人讲清楚的事 | 交互 |
|------|------|------|------|
| 1 | **认识它** | 它是个会动手的助理、用大白话说就行、能看你给的资料、记性有限、**会一本正经说错（要复核）**、放心用但守规矩 | 翻面卡片 |
| 2 | **能帮你做什么** | 写周报 / 看数据 / 做材料 / 打杂，各列 4 个能直接用的本事 | 标签切换 |
| 3 | **🌟 实战案例** | 三段完整对话演示（写周报 / 看懂数据表 / 做汇报材料），「你这样说 → 虾这样做」+ 每步诀窍 | 聊天气泡 + 案例切换 |
| 4 | **喂料升级** | 喂材料、喂样板、喂新信息——让它更懂你的活，每条带「这样说」示例 | 手风琴 |
| 5 | **用好它的诀窍** | 6 条好习惯（说清楚、给例子、先提纲、不满意就改、自己复核、一件事一对话），do/don't 对照 | do/don't 卡片 |
| 6 | **你的专属虾** | 回答 3 个小问题 → 生成**一段能直接复制粘贴去对虾说的话术** + 贴心提醒 | 话术生成器 |
| – | **毕业小测** | 4 道日常情景题，答完给评价 | 答题计分 |

页面细节：滚动进度条、随滚动「长大」的虾缸成长环、浮现动画、随页滚动高亮的导航、**🌙 深色 / ☀️ 浅色一键切换**（记住上次选择，首次跟随系统）。

## 🖨️ 一页打印小抄（cheatsheet.html）

导航栏点「打印小抄」会打开 `cheatsheet.html`——一张可直接打印或存 PDF 的单页速查表，建议贴在工位上：

- 用好它的 6 条诀窍（说清楚 / 给例子 / 先提纲 / 让它改 / 自己核 / 一事一对话）
- 三样「喂料」+ 记住它的脾气
- **三句「开口话术」模板**：把高亮处换成自己的内容，复制即用
- 顶部最显眼处：「重要数字自己核一遍」的醒目提醒

针对打印做了 `@media print` 优化（隐藏按钮、铺满 A4）。

## 设计取舍（为什么这么写）

- **零黑话**：不出现 MCP / token / 上下文工程 / Subagent 等术语，全部翻译成生活化说法（如「它记性有限」「给它喂样板」）。
- **案例驱动**：核心是第 3 关的聊天气泡演示——普通人看一遍真实对话，比读十条原理更容易上手。
- **反复强调复核**：AI 会编造/算错，页面在基础卡、数据案例、诀窍三处反复提醒「重要数字自己核一遍」。
- **话术生成器**给的是「能直接用的一段话」，而不是技术配置——对非技术用户才真正有用。

## 诀窍出处

第 5 关的好习惯整理自公开资料并已通俗化：

- [Anthropic · Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)
- [Anthropic · Effective Context Engineering for AI Agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Anthropic · Writing Tools for AI Agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- [Claude Code Best Practices](https://code.claude.com/docs/en/best-practices)

> ⚠️ 用法、权限与数据规范请以你们公司对 OpenClaw / Hermes 的内部说明为准。

## 文件结构

```
claw-edu/
├── index.html          # 主教程（HTML + CSS + JS 内联，无外部依赖，含深色模式）
├── cheatsheet.html     # 一页可打印的速查小抄
├── README.md
└── .claude/launch.json # 本地预览用的静态服务器配置
```
