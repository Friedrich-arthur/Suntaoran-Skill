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
  version: "1.0"
  source-note: "Unofficial learning-note skill rewritten from the user's Notion draft on three-point summaries and one-page reports."
---

# Three-Point One-Page Report

## Use When

Activate this skill when the user needs to:

- Summarize a complex topic so another person can remember it.
- Prepare a report, proposal, strategy note, briefing, or decision memo.
- Explain a messy issue to a busy reader who needs a clear action.
- Turn scattered material into a compact structure.
- Force clearer thinking because the current explanation feels vague, long, or unfocused.

Do not activate this skill for a simple factual answer, a long-form creative draft, or a case where the user explicitly wants exhaustive detail instead of compression.

## Core Principles

1. Three points must explain the whole issue, not merely list the three most interesting points.
2. A one-page report is a thinking constraint: problem, conclusion, evidence, action, then appendix.
3. If something is still too complex to explain, the structure is probably not high-level enough yet.
4. Plain language wins. If the reader cannot repeat it, the work is not done.
5. Numbers beat vague scale words. Replace "many", "roughly", "a lot", and "almost" with observable quantities whenever possible.

## Inputs To Collect

- `topic`: What is being summarized or reported?
- `audience`: Who must understand, decide, or act?
- `decision_or_action`: What should the reader do after reading?
- `evidence`: Facts, numbers, examples, constraints, links, and source material.
- `scope`: What must be included, and what can move to appendix?
- `length_limit`: Default to one A4 page or about 1000 Chinese characters for the main report.

If facts are missing, make conservative assumptions and label them. Ask only when a wrong assumption would materially mislead the report or create risk.

## Workflow

### 1. Step Back

Pull out of the details before writing.

Ask:

- What is the actual question?
- What does the reader need to remember?
- What decision or action should this unlock?
- Which details are evidence, and which details are only background?

Output a one-sentence `working_topic`.

### 2. Group And Prioritize

Cluster the material into logical groups before choosing the final three points.

Check:

- Which facts are about the same cause, risk, customer, cost, timing, or action?
- Which details are symptoms rather than root points?
- Which items are supporting evidence rather than headline points?
- Which parts can move to appendix without weakening the main answer?

Output `candidate_groups`.

### 3. Force The Three

Compress the candidate groups until exactly three points can cover the whole topic.

Rules:

- If there are more than three, combine upward.
- If there are fewer than three, check whether the topic is too narrow or the evidence is incomplete.
- Each point should be a plain sentence, not a label.
- The three points should be mutually distinct and collectively cover the issue.

Output `three_point_summary`.

### 4. Write In Human Language

Rewrite the three points so a non-specialist can repeat them.

Prefer:

- Short sentences.
- Concrete nouns and verbs.
- Numbers where useful.
- Direct action words.

Avoid:

- Jargon used to hide weak thinking.
- Decorative frameworks.
- Vague quantifiers without evidence.
- Long preambles before the answer.

### 5. Build The One-Page Report

Use this order:

1. Problem: state the issue directly.
2. Conclusion: give the answer before the full argument.
3. Evidence: list only the strongest support for the conclusion.
4. Action recommendation: specify who should do what, by when, and how.
5. Appendix: put detailed reasoning, source links, tables, and long context after the one-page body.

The action recommendation is mandatory. A report without a recommendation is only reference material.

### 6. Self-Check

Before finalizing, check:

- Are there exactly three summary points?
- Do the three points explain the whole issue?
- Can the intended reader repeat the points after one reading?
- Does the report start with problem and conclusion?
- Does every fuzzy quantity have a number, source, or explicit unknown?
- Is there a concrete action recommendation?
- Is the main body within the requested page or word limit?

## Output Format

Return a concise structured answer:

```markdown
## Three-Point Summary
1. ...
2. ...
3. ...

## One-Page Report
Problem: ...
Conclusion: ...
Evidence:
1. ...
2. ...
3. ...
Action Recommendation: ...
Appendix: ...

## Self-Check
- Three points cover the whole issue: yes/no
- Main report within limit: yes/no
- Fuzzy quantities replaced by numbers or marked unknown: yes/no
- Action recommendation included: yes/no
```

## Hard Rules

- Do not output four or more headline points unless the user explicitly rejects the three-point constraint.
- Do not treat "top three" as the same thing as "three points that explain the whole issue."
- Do not bury the conclusion after a long background section.
- Do not use vague scale words when a number, range, source, or "unknown" is available.
- Do not call a document a report if it has no action recommendation.
- For legal, medical, financial, compliance, safety, or other high-stakes domains, treat this skill as a thinking aid only and require domain evidence plus qualified review.

## Anti-Patterns

- Turning a report into a long background essay.
- Listing many points because choosing is uncomfortable.
- Starting from chronology instead of the reader's decision.
- Writing in slogans that sound polished but do not explain the issue.
- Hiding weak evidence behind jargon.
- Dumping all source material into the main body instead of an appendix.

## Rights And Attribution Boundary

This is an unofficial, educational, operationalized skill rewritten from the user's Notion draft. It is not endorsed by Sun Taoran, Lakala, OpenAI, Anthropic, or any referenced person or organization. Names and references are used only for attribution and descriptive context.

Do not copy proprietary books, paid-course materials, speeches, slides, articles, or third-party notes into this skill unless you have permission or a clear license. When adapting source material, publish the workflow in original wording, keep source links, and avoid long verbatim excerpts.
