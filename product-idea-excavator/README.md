# Product Idea Excavator Skill

This folder is the installable Skill package.

## What It Does

It turns vague product ideas into a structured product discovery conversation and, after the user confirms discovery is complete, synthesizes a detailed PRD.

The Skill is Chinese-first and optimized for:

- product idea excavation
- founder/product discovery interviews
- MVP narrowing
- demand evidence checking
- technical stack exploration
- AI product feasibility
- PRD generation

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
evals/
  evals.json
demo/
  sample-run.md
```

## Try It

```text
我有一个产品 idea，但还不成熟。请你像顶级产品经理一样，通过提问帮我把它挖掘清楚。
```

Expected behavior:

- asks one strong question at a time
- pushes vague answers toward concrete evidence
- challenges weak assumptions
- asks about technical implementation
- generates a PRD only after confirmation

