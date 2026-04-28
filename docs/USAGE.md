# Usage Guide

## Start With A Rough Idea

You do not need a mature product spec.

Example:

```text
我想做一个语音类 APP，用户可以说想和谁聊天，系统构建一个对应人物来语音对话。
```

The Skill should respond by:

- restating the idea more precisely
- identifying early risks
- offering possible product directions
- asking the next strongest question

## Let The Skill Lead

The Skill works best when the assistant leads the interview.

You can answer briefly. The Skill should keep the state internally and move through:

- product origin
- target users
- demand evidence
- current workaround
- value proposition
- MVP
- AI and technical feasibility
- business model
- metrics
- risks

## When You Are Unsure

Say:

```text
我还不确定，你给我几个方向。
```

The Skill should provide options, recommend one, and continue discovery.

## When You Want The PRD

Say:

```text
我确认没有其他补充了，可以总结 PRD。
```

The Skill should automatically produce a structured PRD.

## Good Session Pattern

```text
User: I want to build an AI app for X.
Assistant: Here are three possible product directions. I recommend B because...
Assistant: First question: who feels this pain most urgently?
User: Probably small teams.
Assistant: "Small teams" is still broad. Let's make it concrete...
```

## Avoid

Avoid asking the Skill to skip discovery unless you already have a strong spec.

If you say:

```text
直接写 PRD。
```

The Skill should still flag missing information and mark assumptions clearly.

