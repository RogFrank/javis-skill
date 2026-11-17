# 贾维斯 · 个人助理 Skill

【AI个人助理方案】grokbot+reminder版

用苹果「提醒事项」和 Grok Bot（也支持其他支持 Skills 的 Agent），给你自己配一个会按时汇报的助理。技能正文是仓库里的 `skills/javis/SKILL.md`。能不能写入提醒事项、能不能按时汇报，取决于正在使用的 Agent 自身能力，以及你在苹果系统里授予的日历和提醒事项权限。

作者：天天开单 弗兰克

- 仓库：https://github.com/RogFrank/javis-skill
- 技能全文：https://github.com/RogFrank/javis-skill/blob/main/skills/javis/SKILL.md
- 纯文本：https://raw.githubusercontent.com/RogFrank/javis-skill/main/skills/javis/SKILL.md

## 能帮你做什么

- 你说「这个客户王总，放到[大客户]跟一跟」，它会立刻写进苹果提醒事项，并同步到 iPhone。
- 你说「最近两周要吸引100客户，这个事儿，要规划规划，到大蓝图」，它会把目标写入【大蓝图】，并把具体下一步放到【进行中】。
- 你说「Javis工作日早 8 点做计划、晚 10 点自动更新汇报」，它会按北京时间为工作日建好早 8 点和晚 10 点的定时汇报；「很重要」由你亲自填写，助手不代填。

七个清单：大蓝图、很重要、进行中、忽略的、好生活、大客户、小客户。每条标题统一写成「要什么结果｜下一步是什么」。

上面三句是技能里必须原样识别的说法，七个清单的名称也与 `skills/javis/SKILL.md` 一致。这些动作发生在 Agent 按技能正文执行、并且苹果权限已经允许之后。

## 怎么用

### 兼容 skills CLI 的 Agent

下面这条命令适用于兼容 skills CLI 的 Agent。它把本仓库里名为 `javis` 的 skill 安装到该 Agent 的用户级 skills 目录。

```bash
npx -y skills add RogFrank/javis-skill -g --skill javis
```

这条命令未被证实可以自动导入 Grok Bot。它只安装技能文件：不授予苹果日历或提醒事项访问，也不创建定时例程。安装之后，请该 Agent 按技能全文执行。系统若弹出权限请求，由你决定是否允许。

### Grok Bot

Grok Bot 请打开技能全文，把 `SKILL.md` 的完整文字复制进你自己的 Bot，再请它执行。能否落地，以该 Bot 自身能力和你授予的苹果权限为准。

https://github.com/RogFrank/javis-skill/blob/main/skills/javis/SKILL.md

纯文本（便于整段复制）：

https://raw.githubusercontent.com/RogFrank/javis-skill/main/skills/javis/SKILL.md

### 自己克隆

```bash
git clone https://github.com/RogFrank/javis-skill.git
```

仓库：https://github.com/RogFrank/javis-skill

兼容 skills CLI 的 Agent 使用其中的 `skills/javis`（目录名与 frontmatter 的 `name: javis` 一致）。Grok Bot 请复制 `skills/javis/SKILL.md` 的全文。

## 授权

欢迎个人学习和使用，请保留「天天开单 · 贾维斯」来源说明。商业分发请先联系作者。

试一次看看效果，好用再说。

好好聊天 · 天天开单
用好AI，开心赚钱
