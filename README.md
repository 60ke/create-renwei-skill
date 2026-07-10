# Create Renwei Skill

用 ChatGPT 或其他 Agent，基于你的长期聊天记录、已保存记忆和真实表达，生成一份真正属于你的“人味写作” Skill。

这个仓库不是一份固定文风，也不提供某个作者的成品 Skill。它的定位很简单：

> 参考现有的人味写作方法，再让 Agent 从它已经掌握的你，提取属于你自己的写作手迹。

参考项目：

- [orange2ai/renwei-writing](https://github.com/orange2ai/renwei-writing)

原项目最重要的启发是：改稿不是把文字磨得更漂亮，而是保住文字背后那个人的存在感。本仓库进一步解决另一个问题：如何让 ChatGPT 利用长期聊天、历史反馈和记忆，自动生成属于你的专属 Skill。

## 最简单的用法

如果你长期使用 ChatGPT，它通常已经保存了不少关于你的记忆，也了解你的表达习惯、技术背景、常用类比、喜欢和讨厌的句式。

这时不需要先整理一堆材料，直接把 `PROMPT.md` 丢给 ChatGPT，然后说：

```text
请参考这个仓库的 PROMPT.md，以及：
https://github.com/orange2ai/renwei-writing

优先使用你已经保存的关于我的记忆、我们的长期聊天记录、我过去的表达和我对改稿结果的反馈，生成一份属于我的人味写作 Skill。

不要模仿参考项目作者。参考项目只提供方法，我本人长期留下的表达记录才是风格来源。
```

如果 ChatGPT 已经足够了解你，这一步就能直接生成初版。

## 什么时候需要补材料

只有在以下情况下，才需要额外上传文章或聊天记录：

- 这是一个新账号，几乎没有历史对话；
- 记忆功能没有开启；
- 你想为某个特定身份单独建 Skill，例如技术评论、小说、商业写作；
- 第一版 Skill 明显不像你；
- 你想让 Agent 分析某些它看不到的旧文章或私有记录。

这时再补充：

- 你写过并且满意的文章；
- 原始口述或聊天记录；
- AI 改坏后被你否掉的版本；
- 你对改稿结果的真实反馈。

## 为什么要做自己的 Skill

直接套用别人的“人味”，最后往往只是从一种 AI 味，换成另一个作者的味道。

真正属于你的 Skill，应该来自：

- ChatGPT 已经保存的你的长期记忆；
- 你和 AI 的历史聊天；
- 你平时提出问题和表达判断的方式；
- 你反复修改、否定 AI 的记录；
- 你自己写过的文章和口述；
- 你常用的术语、类比、语气和判断方式。

所谓“人味”，不是几个形容词，而是一组长期反复出现、可以执行的表达规则。

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

- `PROMPT.md`：直接交给 ChatGPT / Agent 的完整提示词
- `GUIDE.md`：从记忆优先到补充材料、测试迭代的实操流程
- `templates/STYLE_PROFILE.md`：个人表达特征整理模板
- `templates/SKILL_TEMPLATE.md`：最终 Skill 的结构模板

## 推荐生成结果

```text
my-renwei-skill/
├── SKILL.md
├── README.md
└── references/
    ├── post-edit-checklist.md
    └── before-after.md
```

## 在 ChatGPT 中使用生成后的 Skill

把最终生成的 `SKILL.md` 和检查清单上传到 ChatGPT 项目或当前对话，再上传要修改的文章：

```text
请先完整阅读 SKILL.md 和检查清单。
按这个 Skill 修改我上传的文章。
保留我的原始观点、技术判断、口语毛边和个人表达习惯。
只处理不通顺、重复、指代不清和结构断裂。
不要把文章改成行业报告，不要擅自补平衡观点，不要强行写金句。
```

也可以把整个 Skill 放进支持 Skills 的 Agent 目录：

```bash
cp -r my-renwei-skill ~/.codex/skills/
```

## 核心原则

1. 优先使用 ChatGPT 已有的记忆和长期聊天，不要先让用户重复整理它已经知道的信息。
2. 不要复制参考项目作者的文风。
3. 不要只用“口语化、直接、专业”这类空洞标签。
4. 规则必须能在历史表达中找到依据。
5. 第一版可以直接生成，之后再用真实改稿反馈迭代。
6. 最好的结果不是“写得更漂亮”，而是读者觉得：这就是你自己想明白以后写出来的。

## 许可与参考

本仓库只提供教程、模板和生成提示词。

参考项目的许可要求请以其原仓库说明为准：

- [orange2ai/renwei-writing](https://github.com/orange2ai/renwei-writing)
