---
name: simplify-problem
description: >
  Use this skill when a problem has become overcomplicated, blocked by too many
  prerequisites, stuck in "both/and" tradeoffs, or slowed by people/process
  friction. It reframes the real goal, decomposes dependencies, identifies the
  highest-leverage bottleneck, and proposes the cheapest independently
  verifiable next step. Chinese trigger signals include: 想复杂了、推不动、
  既要又要、人不配合、方案越做越重、纠结能不能做到、需要复杂问题简单化。
version: 2.1
load: progressive
source_note: "Unofficial learning-note skill inspired by public management ideas associated with Sun Taoran and by the user's Notion draft."
---

# Simplify Problem

## Use When

Activate this skill when the user shows one or more signals:

- The requested approach is being confused with the real goal.
- The work depends on more than 3 unresolved prerequisites.
- Two or more tasks are waiting on each other.
- The user asks for both sides of a tradeoff without separating time, scope, condition, or stakeholder.
- The team is relying on persuasion, repeated reminders, overtime, or willpower instead of a mechanism.
- The plan keeps adding process, tools, meetings, or abstractions but still cannot ship.
- The discussion is stuck on whether something is possible, instead of asking whether there is a cheaper path.

Do not activate this skill for a simple request that can be answered directly.

## Operating Principles

1. Goal first: separate the desired result from the current method.
2. Have it, then make it good, then make it cheap.
3. A usable 80-point deliverable beats a perfect plan that never starts.
4. If a task has too many prerequisites, decouple it.
5. If people do not cooperate, inspect incentives before lecturing people.
6. Pick the path that is cheapest, simplest, and independently verifiable.

## Inputs To Collect

- `problem`: What is happening, and what outcome is actually wanted?
- `current_method`: What method, process, or assumption is currently treated as mandatory?
- `constraints`: Time, budget, people, tooling, legal/compliance boundaries, irreversible risks.
- `reversibility`: Type 1 for hard-to-reverse decisions, Type 2 for reversible decisions.
- `domain`: Clear, Complicated, Complex, or Chaotic.
- `success_metric`: What observable condition proves that the problem is solved?

If critical inputs are missing, make a conservative assumption and mark it. Ask only when a wrong assumption would create material risk.

## Workflow

### 1. Define

Strip away the current method and restate the target.

Ask:

- What result do we really need?
- Is this result truly wanted, or only inherited from a process?
- What would count as solved?
- What can be ignored if it does not affect the result?

Output `redefined_goal`.

### 2. Decompose

Break the problem into MECE blocks.

Check:

- Are the subproblems independent?
- Is anything missing?
- Which parts are symptoms rather than causes?
- Which parts can be delayed, removed, or solved separately?

Output `decomposition`.

### 3. Focus

Find the 20 percent that controls most of the result.

Use:

- 80/20 to locate the highest-value lever.
- Theory of Constraints to locate the bottleneck.

Output `key_bottleneck` and explain why it is the current limiting factor.

### 4. Decouple

Remove unnecessary dependencies.

Rules:

- More than 3 prerequisites usually means the work must be split.
- Mutual prerequisites usually mean the work must be resequenced.
- Prefer parallel, reversible steps over one large coupled launch.

Output `decoupled_plan`.

### 5. Re-incentivize

For people/process problems, change the mechanism before adding reminders.

Ask:

- Who can actually change the outcome?
- Who currently feels the cost of inaction?
- Can ownership, visibility, feedback, or risk be reassigned?
- What behavior should become the easiest path?

Output `mechanism_change`.

### 6. Validate

Pick the cheapest test that can independently prove progress.

The validation plan must include:

- Minimum test scope.
- Owner.
- Time box.
- Success metric.
- Stop or rollback condition.
- What decision the test unlocks.

Output `validation_plan`.

## Framework Router

Use at most 3 frameworks by default.

| Signal | Prefer |
| --- | --- |
| Stuck in convention | First principles |
| Too many threads | Cynefin, then MECE |
| Limited resources | 80/20 and Theory of Constraints |
| Work cannot move | Decoupling / systems thinking |
| Both/and conflict | TRIZ separation principles |
| People do not cooperate | Incentive redesign |
| Plan keeps getting heavier | Occam's razor and Via Negativa |
| High-risk decision | Pre-mortem, red team, reversibility check |

## Output Format

Return a concise structured answer:

```markdown
## Redefined Goal
...

## Bottleneck
...

## Decoupled Plan
1. ...
2. ...
3. ...

## Minimum Validation
- Owner:
- Test:
- Time box:
- Success metric:
- Stop condition:

## Frameworks Used
- ...
```

## Hard Rules

- Do not confuse the current process with the goal.
- Do not add a framework when plain common sense is enough.
- Do not use more than 3 frameworks unless the risk justifies it.
- Do not move to the next step without an independently checkable intermediate output.
- For Type 1 irreversible decisions, include pre-mortem and red-team checks before recommending commitment.
- For regulated or high-stakes domains such as medical, legal, financial, compliance, or safety, treat this skill as a thinking aid only; require domain evidence and qualified review.

## Anti-Patterns

- Turning a simple problem into a large methodology project.
- Waiting because the ideal solution is unavailable.
- Adding meetings, tools, or rules while the bottleneck remains untouched.
- Relying on repeated persuasion when incentives are misaligned.
- Optimizing cost before proving the result exists.
- Averaging effort across all work instead of attacking the bottleneck.
- Treating this skill as official teaching, legal advice, or professional advice.

## Rights And Attribution Boundary

This is an unofficial, educational, operationalized skill. It is not endorsed by Sun Taoran, Lakala, Anthropic, or any referenced open-source project. Names are used only for attribution and descriptive reference. Do not copy proprietary books, paid-course materials, speeches, slides, or articles into this skill unless you have permission or a clear license.

中文边界：本 Skill 是非官方学习笔记和工作流重写，不代表孙陶然本人、拉卡拉或任何相关机构；不要把书籍、课程、演讲、文章等受版权保护内容原文复制进来，除非已经取得授权或确认许可。
