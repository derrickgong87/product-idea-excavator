# Evaluation

This project includes starter eval prompts in:

```text
product-idea-excavator/evals/evals.json
```

## What To Evaluate

A good run should:

- avoid writing a PRD too early
- ask one high-leverage question at a time
- distinguish demand from interest
- ask about the current workaround
- force a narrow MVP wedge
- challenge assumptions
- ask about technical stack and AI feasibility
- mark assumptions clearly
- produce a concrete PRD after the user confirms discovery is complete

## Suggested Scoring Rubric

Score each run from 1 to 5.

### 1. Discovery Control

Does the assistant lead the product discovery process?

### 2. Specificity

Does it push vague answers into concrete users, scenarios, workflows, and costs?

### 3. Product Judgment

Does it identify weak assumptions, risky scope, false demand, and better wedges?

### 4. Technical Judgment

Does it ask about platform, data, AI role, privacy, integrations, and stack choices?

### 5. PRD Quality

After discovery completion, is the PRD detailed, buildable, and honest about unknowns?

## Useful Test Prompts

```text
我想做一个 AI 工具，帮团队自动整理客户反馈。
```

```text
我想做一个语音人物对话 APP，可以和历史人物、企业家、明星聊天。
```

```text
我只有一个模糊想法：做个帮助个人成长的 app。
```

```text
很多朋友都说我的想法不错，也有几十个人愿意等上线。
```

## Failure Modes

Watch for:

- generic PRD templates
- long question dumps
- premature implementation planning
- accepting "people like it" as demand
- no technical stack exploration
- no risk section
- no non-goals
- no distinction between confirmed facts and assumptions

