# Hiring Kit Generator Skill / 招聘作战包生成器

一个通用的 Agent Skill：先采访用户，再为任意岗位生成完整招聘作战包，包括可投放 JD、招聘官参考资料、面试测人题、评判 Checkpoint 与 Rubric、试岗任务、内部隐藏挖坑、候选人准备指引和招聘节奏。

A general-purpose Agent Skill that interviews the user first, then generates a complete hiring kit for any role: publishable JD, recruiter notes, interview questions, evaluation checkpoints, scoring rubric, trial task, internal hidden traps, candidate preparation guide, and hiring timeline.

## To Humans / 给人看的说明

### What This Is / 这是什么

This is a reusable hiring workflow for Codex, Claude Code, OpenClaw, and similar agents. It is designed for founders, operators, recruiters, and hiring managers who need something more useful than a generic JD.

这是给 Codex、Claude Code、OpenClaw 等 Agent 使用的招聘工作流，适合创始人、运营负责人、招聘负责人和用人经理。它的目标不是写一份普通 JD，而是把岗位定义、筛选逻辑、面试问题、试岗任务和评判标准一起做出来。

### Quick Start / 快速开始

1. Copy this folder into your agent's skills directory.
2. Copy `references/company-config.example.md` to `references/company-config.md`.
3. Fill `company-config.md` with your private company defaults.
4. Ask the agent: `我要招 <岗位>。`

```text
我要招 运营负责人。先采访我，确认后生成完整招聘作战包。
```

### Privacy / 隐私

Do not commit `references/company-config.md`. It is ignored by `.gitignore` because it may contain private company names, salary bands, channels, contacts, values, strategy, or market context.

不要提交 `references/company-config.md`。它已经被 `.gitignore` 忽略，因为里面可能包含公司名、薪资、渠道、联系人、价值观、战略和市场背景。

Before publishing a generated hiring kit, remove:

公开投放前请删除：

- internal checkpoints and scoring rubric / 内部评判点和打分规则；
- hidden-trap answers / 试岗挖坑答案；
- private company config / 私有公司配置；
- candidate/person-specific data / 候选人或个人数据；
- anything that needs legal or compliance review / 需要法务或合规审查的内容。

### Files / 文件说明

- `SKILL.md`: agent-facing workflow and trigger instructions.
- `references/01-interview-playbook.md`: six-part intake script.
- `references/02-kit-template.md`: seven-part hiring-kit template.
- `references/03-checkpoint-rubric.md`: checkpoint and scoring method.
- `references/04-trial-task-traps.md`: trial-task and hidden-trap design method.
- `references/company-config.example.md`: private company configuration template.
- `examples/operations-lead.md`: sanitized example.
- `NOTICE.md`: source and rights notes.
- `LICENSE`: MIT license for this skill directory.

## To Agents / 给 Agent 的说明

When this skill is activated:

本 Skill 被触发时：

1. Read `SKILL.md` first and follow its hard-stop rule.
2. Read `references/company-config.md` if present; otherwise use `company-config.example.md` as the schema.
3. Interview the user before generating. Do not skip the three required inputs: role scope, business problem, and talent profile.
4. Confirm facts and assumptions before producing the kit.
5. Classify the role type before writing checkpoints, rubric, or hidden traps.
6. Generate both polished and plain-text versions unless the user opts out.
7. Separate public-facing and internal-only content.
8. End with a pre-publication deletion checklist.

Trigger examples:

```text
我要招销售负责人。
帮我写一个 CTO 的 JD 和面试题。
给我设计一个运营岗试岗任务。
I need to hire a customer success lead. Interview me first.
```

## License / 许可

MIT. See [`LICENSE`](./LICENSE).
