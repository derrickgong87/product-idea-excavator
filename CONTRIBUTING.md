# Contributing

Thanks for helping improve Product Idea Excavator.

## Good Contributions

The best contributions improve the Skill's product judgment.

Examples:

- sharper interview questions
- better examples
- stronger PRD templates
- eval prompts that reveal failures
- new playbooks for product categories
- safety improvements
- clearer install docs

## Contribution Principles

- Keep the core `SKILL.md` focused.
- Put long reference material in `references/`.
- Prefer concrete examples over abstract advice.
- Avoid long questionnaires.
- Preserve the one-question-at-a-time interview style.
- Mark assumptions clearly.
- Do not add unsafe impersonation, deception, or high-risk automation guidance.

## Suggested Workflow

1. Create or edit a focused file.
2. Add or update an eval prompt if behavior changes.
3. Check that the Skill still avoids premature PRD generation.
4. Open a pull request with:
   - what changed
   - why it improves discovery quality
   - which examples or evals were used

## Local Checks

At minimum:

- read `product-idea-excavator/SKILL.md`
- run through one example prompt manually
- verify `product-idea-excavator/evals/evals.json` remains valid JSON

