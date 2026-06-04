---
name: simplify-problem
description: >
  Use this skill when a problem has become overcomplicated, blocked by too many
  prerequisites, stuck in "both/and" tradeoffs, or slowed by people/process
  friction. It reframes the real goal, decomposes dependencies, identifies the
  highest-leverage bottleneck, and proposes the cheapest independently
  verifiable next step. Chinese trigger signals include: 想复杂了、推不动、
  既要又要、人不配合、方案越做越重、纠结能不能做到、需要复杂问题简单化。
metadata:
  version: "2.2"
  source-note: "Unofficial bilingual learning-note skill inspired by public management ideas associated with Sun Taoran and by the user's Notion draft."
---

# Simplify Problem / 简化问题

## Use When / 何时启用

Activate this skill when the user shows one or more signals:

当用户出现以下信号时启用本 skill：

- The requested approach is being confused with the real goal.  
  把当前做法误当成真实目标。
- The work depends on more than 3 unresolved prerequisites.  
  一件事依赖超过 3 个未解决前提。
- Two or more tasks are waiting on each other.  
  多个任务互相等待，形成耦合。
- The user asks for both sides of a tradeoff without separating time, scope, condition, or stakeholder.  
  用户陷入“既要又要”，但没有拆分时间、范围、条件或相关方。
- The team is relying on persuasion, reminders, overtime, or willpower instead of a mechanism.  
  团队靠说服、提醒、加班或意志力推进，而不是靠机制。
- The plan keeps adding process, tools, meetings, or abstractions but still cannot ship.  
  方案不断加流程、工具、会议或抽象层，却仍然无法交付。
- The discussion is stuck on whether something is possible, instead of asking whether there is a cheaper path.  
  讨论卡在“能不能做到”，而不是追问“有没有更省力的路径”。

Do not activate this skill for a simple request that can be answered directly.

如果请求可以直接回答，不要启用本 skill。

## Operating Principles / 操作原则

1. Goal first: separate the desired result from the current method.  
   目标优先：先把想要的结果和当前做法拆开。
2. Have it, then make it good, then make it cheap.  
   先有，再好，再省。
3. A usable 80-point deliverable beats a perfect plan that never starts.  
   可用的 80 分交付，胜过永远不开始的完美方案。
4. If a task has too many prerequisites, decouple it.  
   前提太多，就先解耦。
5. If people do not cooperate, inspect incentives before lecturing people.  
   人不配合，先看激励机制，再谈教育说服。
6. Pick the path that is cheapest, simplest, and independently verifiable.  
   选择最低成本、最简单、可独立验证的路径。

## Inputs To Collect / 需要收集的输入

- `problem`: What is happening, and what outcome is actually wanted?  
  发生了什么，真正想要的结果是什么？
- `current_method`: What method, process, or assumption is currently treated as mandatory?  
  现在被当作必选项的方法、流程或假设是什么？
- `constraints`: Time, budget, people, tooling, legal/compliance boundaries, irreversible risks.  
  时间、预算、人力、工具、法律/合规边界、不可逆风险。
- `reversibility`: Type 1 for hard-to-reverse decisions, Type 2 for reversible decisions.  
  决策可逆性：Type 1 表示难以逆转，Type 2 表示可逆。
- `domain`: Clear, Complicated, Complex, or Chaotic.  
  领域状态：清晰、繁杂、复杂或混乱。
- `success_metric`: What observable condition proves that the problem is solved?  
  什么可观察条件能证明问题已解决？

If critical inputs are missing, make a conservative assumption and mark it. Ask only when a wrong assumption would create material risk.

如果关键信息缺失，先做保守假设并标注；只有错误假设会造成实质风险时才追问。

## Workflow / 工作流

### 1. Define / 重新定义

Strip away the current method and restate the target.

剥离当前做法，重新表述真实目标。

Ask / 追问：

- What result do we really need?  
  我们真正需要什么结果？
- Is this result truly wanted, or only inherited from a process?  
  这个结果是真需求，还是流程继承下来的假需求？
- What would count as solved?  
  什么状态算解决？
- What can be ignored if it does not affect the result?  
  哪些不影响结果的东西可以忽略？

Output `redefined_goal`.

输出 `redefined_goal`。

### 2. Decompose / 拆解

Break the problem into MECE blocks.

把问题拆成 MECE 子模块。

Check / 检查：

- Are the subproblems independent?  
  子问题是否相互独立？
- Is anything missing?  
  是否有遗漏？
- Which parts are symptoms rather than causes?  
  哪些只是症状，不是原因？
- Which parts can be delayed, removed, or solved separately?  
  哪些可以推迟、删除或独立解决？

Output `decomposition`.

输出 `decomposition`。

### 3. Focus / 聚焦

Find the 20 percent that controls most of the result.

找到控制大部分结果的关键 20%。

Use / 可用方法：

- 80/20 to locate the highest-value lever.  
  用 80/20 找最高价值杠杆。
- Theory of Constraints to locate the bottleneck.  
  用约束理论找当前瓶颈。

Output `key_bottleneck` and explain why it is the current limiting factor.

输出 `key_bottleneck`，并说明为什么它是当前限制因素。

### 4. Decouple / 解耦

Remove unnecessary dependencies.

移除不必要依赖。

Rules / 规则：

- More than 3 prerequisites usually means the work must be split.  
  超过 3 个前提，通常说明需要拆分。
- Mutual prerequisites usually mean the work must be resequenced.  
  互为前提，通常说明顺序需要重排。
- Prefer parallel, reversible steps over one large coupled launch.  
  优先采用可并行、可逆的小步骤，而不是一次性大耦合发布。

Output `decoupled_plan`.

输出 `decoupled_plan`。

### 5. Re-incentivize / 重设机制

For people/process problems, change the mechanism before adding reminders.

遇到人和流程问题，先改机制，再加提醒。

Ask / 追问：

- Who can actually change the outcome?  
  谁真正能改变结果？
- Who currently feels the cost of inaction?  
  现在谁在承担不行动的成本？
- Can ownership, visibility, feedback, or risk be reassigned?  
  是否能重新分配责任、可见性、反馈或风险？
- What behavior should become the easiest path?  
  哪种行为应该变成最容易走的路？

Output `mechanism_change`.

输出 `mechanism_change`。

### 6. Validate / 验证

Pick the cheapest test that can independently prove progress.

选择能独立证明进展的最低成本测试。

The validation plan must include / 验证计划必须包括：

- Minimum test scope / 最小测试范围。
- Owner / 负责人。
- Time box / 时间盒。
- Success metric / 成功指标。
- Stop or rollback condition / 停止或回滚条件。
- What decision the test unlocks / 测试能解锁什么决策。

Output `validation_plan`.

输出 `validation_plan`。

## Framework Router / 框架路由

Use at most 3 frameworks by default.

默认最多使用 3 个框架。

| Signal / 信号 | Prefer / 优先使用 |
| --- | --- |
| Stuck in convention / 被惯例困住 | First principles / 第一性原理 |
| Too many threads / 头绪太多 | Cynefin, then MECE / Cynefin 后接 MECE |
| Limited resources / 资源有限 | 80/20 and Theory of Constraints / 80/20 与约束理论 |
| Work cannot move / 工作推不动 | Decoupling / systems thinking / 解耦与系统思维 |
| Both/and conflict / 既要又要冲突 | TRIZ separation principles / TRIZ 分离原则 |
| People do not cooperate / 人不配合 | Incentive redesign / 激励重设 |
| Plan keeps getting heavier / 方案越来越重 | Occam's razor and Via Negativa / 奥卡姆剃刀与反向删减 |
| High-risk decision / 高风险决策 | Pre-mortem, red team, reversibility check / 预演失败、红队、可逆性检查 |

## Output Format / 输出格式

Return a concise structured answer:

返回简洁结构化答案：

```markdown
## Redefined Goal / 重新定义目标
...

## Bottleneck / 瓶颈
...

## Decoupled Plan / 解耦计划
1. ...
2. ...
3. ...

## Minimum Validation / 最小验证
- Owner / 负责人:
- Test / 测试:
- Time box / 时间盒:
- Success metric / 成功指标:
- Stop condition / 停止条件:

## Frameworks Used / 使用框架
- ...
```

## Hard Rules / 硬规则

- Do not confuse the current process with the goal.  
  不要把当前流程误当成目标。
- Do not add a framework when plain common sense is enough.  
  常识足够时不要硬加框架。
- Do not use more than 3 frameworks unless the risk justifies it.  
  除非风险需要，否则不要使用超过 3 个框架。
- Do not move to the next step without an independently checkable intermediate output.  
  没有可独立检查的中间产物，不要进入下一步。
- For Type 1 irreversible decisions, include pre-mortem and red-team checks before recommending commitment.  
  Type 1 不可逆决策必须先做失败预演和红队检查。
- For regulated or high-stakes domains such as medical, legal, financial, compliance, or safety, treat this skill as a thinking aid only; require domain evidence and qualified review.  
  医疗、法律、财务、合规、安全等高风险领域中，本 skill 只能作为思考辅助，必须要求领域证据和专业审查。

## Anti-Patterns / 反模式

- Turning a simple problem into a large methodology project.  
  把简单问题做成大型方法论项目。
- Waiting because the ideal solution is unavailable.  
  因为理想方案不可得而一直等待。
- Adding meetings, tools, or rules while the bottleneck remains untouched.  
  瓶颈没动，却不断加会议、工具或规则。
- Relying on repeated persuasion when incentives are misaligned.  
  激励错位时仍反复说服。
- Optimizing cost before proving the result exists.  
  尚未证明结果存在，就先优化成本。
- Averaging effort across all work instead of attacking the bottleneck.  
  平均用力，而不是攻击瓶颈。
- Treating this skill as official teaching, legal advice, or professional advice.  
  把本 skill 当作官方教学、法律意见或专业建议。

## Rights And Attribution Boundary / 权利与署名边界

This is an unofficial, educational, operationalized skill. It is not endorsed by Sun Taoran, Lakala, OpenAI, Anthropic, or any referenced open-source project. Names are used only for attribution and descriptive reference. Do not copy proprietary books, paid-course materials, speeches, slides, or articles into this skill unless you have permission or a clear license.

本 Skill 是非官方学习笔记和工作流重写，不代表孙陶然本人、拉卡拉、OpenAI、Anthropic 或任何相关开源项目；相关名称仅用于署名和描述性引用。不要把书籍、课程、演讲、幻灯片、文章等受版权保护内容原文复制进来，除非已经取得授权或确认许可。
