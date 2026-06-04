# Suntaoran-Skill

非官方学习笔记型 Agent Skill 集合：把孙陶然相关公开管理思想和用户 Notion 整理稿，重写成可被 Codex、Claude Code、OpenClaw 等智能体调用的 `SKILL.md` 工作流。

> 免责声明：本仓库不是孙陶然本人、拉卡拉、OpenAI、Anthropic 或任何相关机构的官方项目，也未获得授权、背书或合作确认。仓库名、相关人名和机构名仅用于说明学习笔记的思想来源、主题方向和归属边界。

## Skill 索引

| Skill | 路径 | 解决什么 | 适合场景 |
| --- | --- | --- | --- |
| Simplify Problem | [`SKILL.md`](./SKILL.md) | 把复杂、耦合、卡住的问题重新定义目标，拆解瓶颈，并找最低成本验证路径。 | 想复杂了、推不动、既要又要、人不配合、方案越做越重。 |
| Three-Point One-Page Report | [`skills/three-summary-one-page-report/SKILL.md`](./skills/three-summary-one-page-report/SKILL.md) | 用三条说清楚整件事，用一页报告给出问题、结论、论据和行动建议。 | 总结、汇报、提案、战略规划、复杂问题解释、材料压缩。 |

## 如何使用

只需要某一个 skill 时，复制对应路径下的 `SKILL.md` 到你的 Agent 技能目录。

常见位置：

- Codex / Codex CLI：项目 `AGENTS.md` 或用户全局 skill 目录
- Claude Code：`.claude/skills/<skill-name>/SKILL.md`
- 其他 Agent：按其技能系统要求放置 `SKILL.md`

示例：

```text
请使用 three-point-one-page-report skill，把下面材料整理成三条总结和一页报告。
读者是：____
希望读者采取的行动是：____
材料如下：____
```

## 内容概览

### Simplify Problem

一句话工作法：

> 先问目的 -> 先有再好再省 -> 倒推解耦 -> 小步快跑 -> 改机制不靠意志 -> 选最省力那条路。

该 skill 激活后应输出：

- `redefined_goal`：剥离现有做法后的真实目标。
- `decomposition`：MECE 子问题、依赖链、关键瓶颈。
- `least_effort_solution`：最低成本、可独立验证的解法。
- `validation_plan`：最小试点、验收标准、停止条件。

### Three-Point One-Page Report

一句话工作法：

> 三条覆盖全部，一页先给结论，行动建议必须明确。

该 skill 激活后应输出：

- `Three-Point Summary`：严格三条，每条都用人话表达。
- `One-Page Report`：问题、结论、论据、行动建议、附件。
- `Self-Check`：确认三条是否覆盖全部、一页是否达标、模糊词是否替换、行动建议是否明确。

## 版权与来源说明

本仓库内容来自用户自有 Notion 整理稿的重写和结构化，不直接发布完整原文，不使用第三方 logo、肖像、付费课程材料、书籍长摘录或演讲/文章原文。

主要来源、非官方边界和权利处理方式见 [`NOTICE.md`](./NOTICE.md)。

如果你是相关权利人，认为本仓库中的表述、名称或引用不合适，请通过 GitHub Issue 提出具体位置和原因；维护者会优先处理修改、署名补充或删除请求。
