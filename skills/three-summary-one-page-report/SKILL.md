---
name: three-point-one-page-report
description: >
  Use this skill when the user needs to summarize, present, propose, plan, or
  explain a complex issue in a concise, memorable, action-oriented way. It
  forces a complete three-point summary and a one-page report with problem,
  conclusion, evidence, action recommendation, and appendix. Chinese trigger
  signals include: 三条总结, 一页报告, 汇报太长, 总结不清, 提案, 战略规划,
  想不清楚, 说不明白, 需要让别人记住并执行.
metadata:
  version: "1.1"
  source-note: "Unofficial bilingual learning-note skill rewritten from the user's Notion draft on three-point summaries and one-page reports."
---

# Three-Point One-Page Report / 三条总结 + 一页报告

## Use When / 何时启用

Activate this skill when the user needs to:

当用户需要以下结果时启用本 skill：

- Summarize a complex topic so another person can remember it.  
  把复杂主题总结到别人能记住。
- Prepare a report, proposal, strategy note, briefing, or decision memo.  
  准备报告、提案、战略说明、汇报或决策备忘录。
- Explain a messy issue to a busy reader who needs a clear action.  
  向忙碌读者解释复杂问题，并给出明确行动。
- Turn scattered material into a compact structure.  
  把零散材料压缩成紧凑结构。
- Force clearer thinking because the current explanation feels vague, long, or unfocused.  
  当前解释太模糊、太长或没有重点，需要倒逼想清楚。

Do not activate this skill for a simple factual answer, a long-form creative draft, or a case where the user explicitly wants exhaustive detail instead of compression.

如果只是简单事实回答、长篇创作，或用户明确要求穷尽细节而不是压缩，不要启用本 skill。

## Core Principles / 核心原则

1. Three points must explain the whole issue, not merely list the three most interesting points.  
   三条必须解释整件事，不只是列出最有意思的三点。
2. A one-page report is a thinking constraint: problem, conclusion, evidence, action, then appendix.  
   一页报告是思考约束：问题、结论、论据、行动，再放附件。
3. If something is still too complex to explain, the structure is probably not high-level enough yet.  
   如果仍然复杂到说不清，通常是结构还不够高。
4. Plain language wins. If the reader cannot repeat it, the work is not done.  
   人话优先；读者复述不出来，就还没完成。
5. Numbers beat vague scale words. Replace "many", "roughly", "a lot", and "almost" with observable quantities whenever possible.  
   数字胜过模糊词；尽量把“大概、差不多、很多、海量”等换成可观察数量。

## Inputs To Collect / 需要收集的输入

- `topic`: What is being summarized or reported?  
  要总结或汇报的主题是什么？
- `audience`: Who must understand, decide, or act?  
  谁需要理解、决策或行动？
- `decision_or_action`: What should the reader do after reading?  
  读者读完后应采取什么行动？
- `evidence`: Facts, numbers, examples, constraints, links, and source material.  
  事实、数字、案例、约束、链接和来源材料。
- `scope`: What must be included, and what can move to appendix?  
  哪些必须进入正文，哪些可以移到附件？
- `length_limit`: Default to one A4 page or about 1000 Chinese characters for the main report.  
  默认主报告控制在一页 A4 或约 1000 中文字以内。

If facts are missing, make conservative assumptions and label them. Ask only when a wrong assumption would materially mislead the report or create risk.

如果事实缺失，先做保守假设并标注；只有错误假设会实质误导报告或造成风险时才追问。

## Workflow / 工作流

### 1. Step Back / 先退一步

Pull out of the details before writing.

动笔前先从细节里拔出来。

Ask / 追问：

- What is the actual question?  
  真正的问题是什么？
- What does the reader need to remember?  
  读者真正需要记住什么？
- What decision or action should this unlock?  
  这份总结要解锁什么决策或行动？
- Which details are evidence, and which details are only background?  
  哪些是论据，哪些只是背景？

Output a one-sentence `working_topic`.

输出一句话 `working_topic`。

### 2. Group And Prioritize / 分组并排序

Cluster the material into logical groups before choosing the final three points.

先把材料归为逻辑组，再选择最终三条。

Check / 检查：

- Which facts are about the same cause, risk, customer, cost, timing, or action?  
  哪些事实属于同一个原因、风险、客户、成本、时间或行动？
- Which details are symptoms rather than root points?  
  哪些只是症状，不是根点？
- Which items are supporting evidence rather than headline points?  
  哪些只是支撑论据，不应成为标题点？
- Which parts can move to appendix without weakening the main answer?  
  哪些移到附件也不会削弱主答案？

Output `candidate_groups`.

输出 `candidate_groups`。

### 3. Force The Three / 压成三条

Compress the candidate groups until exactly three points can cover the whole topic.

持续压缩候选组，直到正好三条能覆盖整个主题。

Rules / 规则：

- If there are more than three, combine upward.  
  超过三条，就向上合并。
- If there are fewer than three, check whether the topic is too narrow or the evidence is incomplete.  
  少于三条，检查主题是否过窄或证据是否不足。
- Each point should be a plain sentence, not a label.  
  每条应是人话句子，不只是标签。
- The three points should be mutually distinct and collectively cover the issue.  
  三条之间要彼此区分，并共同覆盖问题。

Output `three_point_summary`.

输出 `three_point_summary`。

### 4. Write In Human Language / 说人话

Rewrite the three points so a non-specialist can repeat them.

把三条改写到非专业读者也能复述。

Prefer / 优先：

- Short sentences / 短句。
- Concrete nouns and verbs / 具体名词和动词。
- Numbers where useful / 有用时用数字。
- Direct action words / 直接行动词。

Avoid / 避免：

- Jargon used to hide weak thinking / 用术语掩盖思考薄弱。
- Decorative frameworks / 装饰性框架。
- Vague quantifiers without evidence / 没有证据的模糊定量词。
- Long preambles before the answer / 答案前的长铺垫。

### 5. Build The One-Page Report / 生成一页报告

Use this order:

按以下顺序写：

1. Problem: state the issue directly.  
   问题：直接说明问题。
2. Conclusion: give the answer before the full argument.  
   结论：先给答案，再展开论证。
3. Evidence: list only the strongest support for the conclusion.  
   论据：只列最能支撑结论的证据。
4. Action recommendation: specify who should do what, by when, and how.  
   行动建议：明确谁、何时、做什么、怎么做。
5. Appendix: put detailed reasoning, source links, tables, and long context after the one-page body.  
   附件：把详细论证、来源链接、表格和长背景后置。

The action recommendation is mandatory. A report without a recommendation is only reference material.

行动建议是必选项。没有行动建议的报告，只是参考资料。

### 6. Self-Check / 完成前自检

Before finalizing, check:

定稿前检查：

- Are there exactly three summary points?  
  是否正好三条？
- Do the three points explain the whole issue?  
  三条是否解释了整件事？
- Can the intended reader repeat the points after one reading?  
  目标读者读一遍后能否复述？
- Does the report start with problem and conclusion?  
  报告是否先写问题和结论？
- Does every fuzzy quantity have a number, source, or explicit unknown?  
  每个模糊定量词是否都有数字、来源或明确标记未知？
- Is there a concrete action recommendation?  
  是否有具体行动建议？
- Is the main body within the requested page or word limit?  
  正文是否符合页数或字数限制？

## Output Format / 输出格式

Return a concise structured answer:

返回简洁结构化答案：

```markdown
## Three-Point Summary / 三条总结
1. ...
2. ...
3. ...

## One-Page Report / 一页报告
Problem / 问题: ...
Conclusion / 结论: ...
Evidence / 论据:
1. ...
2. ...
3. ...
Action Recommendation / 行动建议: ...
Appendix / 附件: ...

## Self-Check / 自检
- Three points cover the whole issue / 三条覆盖全部: yes/no
- Main report within limit / 主报告在限制内: yes/no
- Fuzzy quantities replaced by numbers or marked unknown / 模糊词已替换或标未知: yes/no
- Action recommendation included / 已包含行动建议: yes/no
```

## Hard Rules / 硬规则

- Do not output four or more headline points unless the user explicitly rejects the three-point constraint.  
  除非用户明确拒绝三条约束，否则不要输出四条或更多标题点。
- Do not treat "top three" as the same thing as "three points that explain the whole issue."  
  不要把“前三个重点”等同于“能解释全部事情的三条”。
- Do not bury the conclusion after a long background section.  
  不要把结论埋在长背景之后。
- Do not use vague scale words when a number, range, source, or "unknown" is available.  
  能给数字、范围、来源或“未知”时，不要用模糊规模词。
- Do not call a document a report if it has no action recommendation.  
  没有行动建议的文档不要称为报告。
- For legal, medical, financial, compliance, safety, or other high-stakes domains, treat this skill as a thinking aid only and require domain evidence plus qualified review.  
  法律、医疗、财务、合规、安全等高风险领域中，本 skill 只能作为思考辅助，必须要求领域证据和专业审查。

## Anti-Patterns / 反模式

- Turning a report into a long background essay.  
  把报告写成长篇背景文章。
- Listing many points because choosing is uncomfortable.  
  因为不愿取舍而列很多点。
- Starting from chronology instead of the reader's decision.  
  从时间流水账开始，而不是从读者决策开始。
- Writing in slogans that sound polished but do not explain the issue.  
  写听起来漂亮但解释不了问题的口号。
- Hiding weak evidence behind jargon.  
  用术语掩盖证据薄弱。
- Dumping all source material into the main body instead of an appendix.  
  把所有材料堆进正文，而不是放到附件。

## Rights And Attribution Boundary / 权利与署名边界

This is an unofficial, educational, operationalized skill rewritten from the user's Notion draft. It is not endorsed by Sun Taoran, Lakala, OpenAI, Anthropic, or any referenced person or organization. Names and references are used only for attribution and descriptive context.

本 Skill 是基于用户 Notion 草稿重写的非官方学习笔记和工作流，不代表孙陶然本人、拉卡拉、OpenAI、Anthropic 或任何被提及个人/机构；相关名称和引用仅用于署名和描述性上下文。

Do not copy proprietary books, paid-course materials, speeches, slides, articles, or third-party notes into this skill unless you have permission or a clear license. When adapting source material, publish the workflow in original wording, keep source links, and avoid long verbatim excerpts.

不要把专有书籍、付费课程材料、演讲、幻灯片、文章或第三方笔记原文复制进本 skill，除非已经取得授权或明确许可。改写来源材料时，应使用原创表达、保留来源链接，并避免长段逐字摘录。
