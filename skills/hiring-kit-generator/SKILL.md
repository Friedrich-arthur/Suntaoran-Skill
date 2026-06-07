---
name: hiring-kit-generator
description: >
  Use this skill when the user wants to hire for a role and needs a complete,
  role-specific hiring kit after an intake interview: publishable job
  description, recruiter notes, interview questions, evaluation checkpoints,
  scoring rubric, trial task, hidden internal traps, candidate preparation
  guide, and hiring timeline. Chinese trigger signals include: 我要招人, 招某个岗位,
  写 JD, 招聘方案, 面试题, 试岗题, 候选人指引, 招聘流程.
---

# Hiring Kit Generator / 招聘作战包生成器

## Mission / 目标

Turn a vague hiring request such as "I need to hire a head of operations" into a company-aware, role-specific hiring kit. Interview first, confirm assumptions, then generate practical hiring assets. Do not output generic HR language.

把用户一句模糊的「我要招 X」变成贴合公司、岗位、人才市场的完整招聘作战包。先采访，后确认，再生成；不要直接输出通用套话。

## Required Source Files / 必读资源

Read these files when the corresponding step starts:

按步骤读取对应资源：

- `references/company-config.example.md`: configuration schema. If `company-config.md` exists beside it, read that file for company-specific defaults. Never ask the user to publish `company-config.md`.
- `references/01-interview-playbook.md`: intake questions and hard-stop rules.
- `references/02-kit-template.md`: the seven-part hiring kit structure.
- `references/03-checkpoint-rubric.md`: role-specific checkpoint and scoring methodology.
- `references/04-trial-task-traps.md`: trial-task and hidden-trap design.

## Workflow / 工作流

### 1. Load Context / 读取背景

Check whether `references/company-config.md` exists. If it exists, use it only as private working context. If it does not exist, use `references/company-config.example.md` as the schema and ask the user for missing company defaults only when they materially affect the hiring kit.

先检查是否有 `references/company-config.md`。如果有，只作为私有工作上下文使用；如果没有，用 `company-config.example.md` 的字段结构追问必要公司信息。

### 2. Interview / 采访

Use `references/01-interview-playbook.md`.

Hard stop: do not generate the hiring kit until these three inputs are known:

硬停止：拿到以下三项之前，不要进入生成：

1. Role name and responsibility scope / 岗位名与职责范围。
2. The business problem this hire must solve / 为什么现在招、招来解决什么问题。
3. Talent profile / 资历、必备特质、硬门槛。

For salary, location, work mode, tone, deliverable format, and channels, use company defaults if available and label them as assumptions.

薪资、地点、办公方式、语气、产出形态和投放渠道可以用公司默认值补齐，但必须标注为假设。

### 3. Confirm / 确认

Summarize:

汇总确认：

- known facts / 已确认事实；
- assumptions from company defaults / 来自公司配置的默认假设；
- open questions that materially change the output / 会明显影响结果的未决问题。

Wait for the user to confirm before producing the full kit. If the user explicitly asks to proceed without confirmation, mark all assumptions clearly.

等用户确认后再生成完整作战包。若用户明确要求直接继续，必须清楚标注所有假设。

### 4. Classify Role Type / 岗位分流

Before designing checkpoints or traps, classify the role:

设计 Checkpoint 和挖坑前，先判断岗位类型：

- Innovation or technical roles: test problem definition and prototype execution.
- Operations, project, or assistant roles: test reliability, prioritization, discretion, and execution.
- Sales or BD roles: test discovery, persuasion, resilience, and pipeline judgment.
- Professional functions such as finance, legal, or HR: test rigor, compliance, judgment, and communication.
- Support or administrative roles: test reliability, attention to detail, and communication.

Do not force one role framework onto another role type.

不要把一种岗位的框架硬套到另一种岗位上。

### 5. Generate The Hiring Kit / 生成作战包

Use `references/02-kit-template.md` and produce both versions unless the user asks otherwise:

默认生成两版，除非用户另有要求：

1. Polished version for internal collaboration and archiving / 美化版，适合内部协作和归档。
2. Plain-text copyable version for job boards and chats / 纯文本可复制版，适合投放和聊天转发。

The kit must include seven parts:

必须包含七块：

1. Publishable external JD / 对外 JD。
2. Recruiter reference notes / 招聘官参考资料。
3. Hooks and embedded screening cues / 钩子与伏笔。
4. Internal evaluation checkpoints and rubric / 内部评判 Checkpoint + Rubric。
5. Trial task and internal hidden traps / 试岗 Case + 内部挖坑。
6. Candidate preparation guide / 候选人准备指引。
7. Hiring process and timeline / 招聘流程与节奏。

Mark internal-only material with `Internal only` / `内部`. Include a final pre-publication deletion checklist that tells the user to remove internal checkpoints, rubric details, hidden-trap answers, private company config, and any candidate/person-specific data before posting publicly.

内部内容必须标注 `Internal only` / `内部`。最后附公开投放前删除清单：删除内部 Checkpoint、Rubric 细节、挖坑答案、私有公司配置、候选人或个人数据。

## Style Rules / 风格规则

- Write in plain language, not HR jargon.
- Be specific to this company, role, and market.
- Make values and "who we want / who we do not want" visible as screening signals, not slogans.
- Avoid discriminatory, illegal, sexualized, humiliating, or invasive requirements.
- Do not encourage unpaid production work disguised as a trial task. Trial tasks should be small, bounded, relevant, and scoreable.
- For high-stakes legal or compliance claims, tell the user to obtain qualified review.

## Output Format / 输出格式

Return a concise structured answer:

```markdown
## Intake Confirmation / 采访确认
...

## Role Type / 岗位类型
...

## Polished Hiring Kit / 美化版招聘作战包
...

## Plain-Text Version / 纯文本可复制版
...

## Pre-Publication Deletion Checklist / 公开投放前删除清单
- [ ] Remove internal checkpoints and scoring rubric.
- [ ] Remove hidden-trap answers.
- [ ] Remove private company configuration.
- [ ] Remove candidate/person-specific data.
- [ ] Run legal/compliance review when required.
```

## Self-Check / 完成前自检

- Did you collect the three hard-stop inputs?
- Did the user confirm assumptions, or did you label them clearly?
- Did you classify the role before designing checkpoints and traps?
- Does the output fit the company, role, and market instead of sounding generic?
- Are internal and external materials separated?
- Are both polished and plain-text versions included unless the user opted out?
- Is there a pre-publication deletion checklist?
