# Three-Point One-Page Report Skill

非官方学习笔记型 Agent Skill：把「三条总结 + 一页报告」整理成可被 Codex、Claude Code、OpenClaw 等智能体调用的 `SKILL.md` 工作流。

An unofficial learning-note Agent Skill that turns "three-point summaries + one-page reports" into a `SKILL.md` workflow usable by Codex, Claude Code, OpenClaw, and other agents.

> 免责声明：本目录内容不是孙陶然本人、拉卡拉、OpenAI、Anthropic 或任何相关机构的官方项目，也未获得授权、背书或合作确认。相关人名和机构名仅用于说明学习笔记的思想来源、主题方向和归属边界。
>
> Disclaimer: This directory is not an official project of Sun Taoran, Lakala, OpenAI, Anthropic, or any related organization. It has not been authorized, endorsed, sponsored, or confirmed as a collaboration. Names are used only to describe the learning source, theme, and attribution boundary.

## 内容概览 / Content Overview

这个 Skill 解决两件事：

This skill solves two related problems:

- `三条总结`：不是挑三个亮点，而是用三条把整件事说清楚，让读者能记住并复述。  
  `Three-point summary`: not picking three highlights, but using three points to explain the whole issue so the reader can remember and repeat it.
- `一页报告`：用「问题 -> 结论 -> 论据 -> 行动建议 -> 附件」的倒序结构，让忙碌读者先看到结论和要做什么。  
  `One-page report`: using the order "problem -> conclusion -> evidence -> action recommendation -> appendix" so a busy reader sees the answer and next action first.

它适合总结、汇报、提案、战略规划、复杂问题解释、会议材料整理，以及任何「想不清楚 / 说不明白 / 对方记不住」的场景。

It is useful for summaries, briefings, proposals, strategy notes, complex explanations, meeting-material cleanup, and any case where the thinking is unclear, the explanation is hard to follow, or the reader will not remember the message.

## 什么时候调用 / When To Use

- 汇报材料太长，读者抓不到重点。  
  The briefing is too long and the reader cannot find the point.
- 总结写成了很多条，但没有主线。  
  The summary has many bullets but no main line.
- 需要把复杂问题讲给非专业读者听。  
  A complex issue must be explained to a non-specialist reader.
- 提案或战略规划需要压成高层可决策的一页纸。  
  A proposal or strategy plan must be compressed into a decision-ready one-pager.
- 已经有素材，但缺少结论、论据和行动建议。  
  Source material exists, but the conclusion, evidence, and action recommendation are missing.

## 快速使用 / Quick Start

把 [`SKILL.md`](./SKILL.md) 放入你的 Agent 技能目录，或复制到项目级指令文件中。

Place [`SKILL.md`](./SKILL.md) into your agent's skill directory, or copy it into a project-level instruction file.

常见位置 / Common locations:

- Codex / Codex CLI：项目 `AGENTS.md` 或用户全局 skill 目录。  
  Codex / Codex CLI: project `AGENTS.md` or user-global skill directory.
- Claude Code：`.claude/skills/three-point-one-page-report/SKILL.md`。  
  Claude Code: `.claude/skills/three-point-one-page-report/SKILL.md`.
- 其他 Agent：按其技能系统要求放置 `SKILL.md`。  
  Other agents: follow their skill-system placement rules.

示例提示词 / Example prompt:

```text
请使用 three-point-one-page-report skill，把下面材料整理成三条总结和一页报告。
读者是：____
希望读者采取的行动是：____
材料如下：____

Use the three-point-one-page-report skill to turn the material below into a three-point summary and one-page report.
Audience: ____
Desired reader action: ____
Material: ____
```

## 输出契约 / Output Contract

该 Skill 激活后应输出：

When activated, this skill should output:

- `Three-Point Summary`：严格三条，每条都用人话表达。  
  Exactly three plain-language points.
- `One-Page Report`：问题、结论、论据、行动建议、附件。  
  Problem, conclusion, evidence, action recommendation, and appendix.
- `Self-Check`：确认三条是否覆盖全部、一页是否达标、模糊词是否替换、行动建议是否明确。  
  A self-check for full coverage, page limit, vague wording, and explicit action.

## 版权与来源说明 / Rights And Sources

本目录内容来自用户自有 Notion 整理稿的重写和结构化，不直接发布完整原文，不使用第三方 logo、肖像、付费课程材料、书籍长摘录或演讲/文章原文。

This directory contains rewritten and structured workflow material based on the user's own Notion draft. It does not publish the full original text, third-party logos, portraits, paid-course materials, long book excerpts, or verbatim speeches/articles.

主要来源、非官方边界和权利处理方式见 [`NOTICE.md`](./NOTICE.md)。

See [`NOTICE.md`](./NOTICE.md) for source notes, non-official status, and rights-handling rules.

如果你是相关权利人，认为本仓库中的表述、名称或引用不合适，请通过 GitHub Issue 提出具体位置和原因；维护者会优先处理修改、署名补充或删除请求。

If you are a rights holder and believe any wording, naming, or reference is inappropriate, please open a GitHub Issue with the exact location and reason. The maintainer will prioritize correction, attribution, or removal requests.
