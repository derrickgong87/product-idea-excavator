# Installation

Product Idea Excavator is a bilingual, markdown-first Skill package.

## Install From This Repository

Copy the `product-idea-excavator/` folder into your local Skills directory.

The installed folder should look like:

```text
skills/
  product-idea-excavator/
    SKILL.md
    references/
      en/
    evals/
    demo/
```

Then start a new assistant session so the Skill metadata can be discovered.

## Verify Installation

Try this prompt:

```text
我有一个产品想法，但还很模糊。请用产品想法挖掘器的方式来问我问题。
```

Or this English prompt:

```text
I have a product idea, but it is still vague. Use product-idea-excavator to interview me and sharpen it.
```

Expected behavior:

- It should not immediately write a PRD.
- It should ask one high-value product discovery question.
- It should identify missing assumptions.
- It should eventually ask about technical implementation and MVP scope.
- It should respond in the same language as the user's product idea.

## Manual Use Without Installing

If your environment does not support Skill installation, open:

```text
product-idea-excavator/SKILL.md
```

Then paste its instructions into your assistant context, followed by your product idea.

## Updating

Pull the latest repository changes and replace the installed `product-idea-excavator/` folder.

If you have local edits, back them up before replacing.
