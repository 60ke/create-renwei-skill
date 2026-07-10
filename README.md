# Create Renwei Skill

用 Agent 基于你自己的文章、口述和长期对话，生成一份真正属于你的“人味写作” Skill。

这个仓库不是一份固定文风，也不提供某个作者的成品 Skill。它的定位很简单：

> 参考现有的人味写作方法，再让 Agent 从你的真实表达材料里，提取属于你自己的写作手迹。

参考项目：

- [orange2ai/renwei-writing](https://github.com/orange2ai/renwei-writing)

原项目最重要的启发是：改稿不是把文字磨得更漂亮，而是保住文字背后那个人的存在感。本仓库在此基础上，提供一套“如何让 Agent 为你生成专属 Skill”的教程和提示词。

## 为什么要做自己的 Skill

直接套用别人的“人味”，最后往往只是从一种 AI 味，换成另一个作者的味道。

真正属于你的 Skill，应该来自：

- 你自己写过的文章；
- 你没有整理过的口述；
- 你和 AI 的长期对话；
- 你觉得“这句很像我”的表达；
- 你明确否掉过的 AI 改稿；
- 你常用的技术词、类比、语气和判断方式。

所谓“人味”，不是几个形容词，而是一组稳定、可执行的表达规则。

## 仓库内容

```text
.
├── README.md
├── PROMPT.md
├── GUIDE.md
└── templates/
    ├── STYLE_PROFILE.md
    └── SKILL_TEMPLATE.md
```

- `PROMPT.md`：可直接交给 Agent 的完整提示词
- `GUIDE.md`：从准备材料到回归测试的实操流程
- `templates/STYLE_PROFILE.md`：个人表达特征整理模板
- `templates/SKILL_TEMPLATE.md`：最终 Skill 的结构模板

## 最快使用方法

### 1. 准备材料

至少准备：

- 3 到 10 篇你自己写过、并且满意的文章；
- 一些未经润色的真实口述或聊天记录；
- 2 到 5 组“AI 改坏了 / 你重新改好”的对照；
- 你明确喜欢和讨厌的句式。

材料越真实，生成的 Skill 越像你。

### 2. 把本仓库和材料交给 Agent

可以使用 ChatGPT、Codex、Claude Code 或其他支持文件读取的 Agent。

把这些内容一起提供给它：

- 本仓库中的 `PROMPT.md`
- 参考项目 `orange2ai/renwei-writing`
- 你的文章、口述、聊天记录和改稿反馈

然后要求 Agent：

```text
请严格按照 PROMPT.md 执行。
先阅读参考项目，再分析我提供的全部材料。
不要模仿参考项目作者，只提取我本人稳定的表达手迹。
最终生成一份可以直接使用的专属写作 Skill。
```

### 3. 让 Agent 生成结果

建议最终至少生成：

```text
my-renwei-skill/
├── SKILL.md
├── references/
│   ├── post-edit-checklist.md
│   └── before-after.md
└── README.md
```

### 4. 用旧文章做回归测试

不要马上相信第一版。

拿同一篇旧文章测试：

1. 原文；
2. Agent 按 Skill 改写后的版本；
3. 你逐句指出“不像我”的地方；
4. Agent 把失败原因补回 Skill；
5. 再跑一轮。

一个专属 Skill 通常不是一次生成出来的，而是通过几次真实改稿慢慢收敛。

## 在 ChatGPT 中使用

### 方式一：上传文件

把最终生成的 `SKILL.md` 和检查清单上传到 ChatGPT 项目或当前对话，再上传要修改的文章。

提示词：

```text
请先完整阅读 SKILL.md 和检查清单。
按这个 Skill 修改我上传的文章。
保留我的原始观点、技术判断、口语毛边和个人表达习惯。
只处理不通顺、重复、指代不清和结构断裂。
不要把文章改成行业报告，不要擅自补平衡观点，不要强行写金句。
```

### 方式二：放进 Agent 的 Skills 目录

不同 Agent 的目录规范不同。核心做法都是把整个专属 Skill 目录放到它能自动读取的位置。

例如：

```bash
cp -r my-renwei-skill ~/.codex/skills/
```

或者把 `SKILL.md` 放进项目根目录，并在 `AGENTS.md` 中要求 Agent 在改稿前先读取它。

## 核心原则

1. 不要复制别人的文风。
2. 不要只用“口语化、直接、专业”这类空洞标签。
3. 规则必须来自真实文章和真实修改反馈。
4. 先判断该不该改，再检查有没有改出 AI 味。
5. 只检查 Agent 修改过的句子，不要拿清单误伤作者原文。
6. 最好的结果不是“写得更漂亮”，而是读者觉得：这就是你自己想明白以后写出来的。

## 许可与参考

本仓库只提供教程、模板和生成提示词。

参考项目的许可要求请以其原仓库说明为准：

- [orange2ai/renwei-writing](https://github.com/orange2ai/renwei-writing)
