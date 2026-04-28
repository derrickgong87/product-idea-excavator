# Product Idea Excavator Skill

This folder is the installable Skill package.

## What It Does

It turns vague product ideas into a structured product discovery conversation and, after the user confirms discovery is complete, synthesizes a detailed PRD.

The Skill is bilingual and optimized for:

- product idea excavation
- founder/product discovery interviews
- MVP narrowing
- demand evidence checking
- technical stack exploration
- AI product feasibility
- PRD generation

## Language Behavior

The Skill mirrors the user's language for the whole session:

- Chinese input -> Chinese interview and Chinese PRD
- English input -> English interview and English PRD
- mixed input -> follow the language of the product idea itself

It should not mix languages unless the user explicitly asks for bilingual output.

## Files

```text
SKILL.md
references/
  prd-template.md
  discovery-question-bank.md
  product-sense-playbook.md
  tech-stack-playbook.md
  ai-product-playbook.md
  example-interviews.md
  en/
    prd-template.md
    discovery-question-bank.md
    product-sense-playbook.md
    tech-stack-playbook.md
    ai-product-playbook.md
    example-interviews.md
evals/
  evals.json
demo/
  sample-run.md
```

## Try It

```text
我有一个产品 idea，但还不成熟。请你像顶级产品经理一样，通过提问帮我把它挖掘清楚。
```

Or in English:

```text
I have a rough product idea. Act like a top product manager and help me excavate it through questions.
```

Expected behavior:

- asks one strong question at a time
- pushes vague answers toward concrete evidence
- challenges weak assumptions
- asks about technical implementation
- generates a PRD only after confirmation
