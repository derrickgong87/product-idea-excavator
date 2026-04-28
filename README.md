# Product Idea Excavator

> A Chinese-first product discovery Skill that turns vague product ideas into sharp product thinking and high-quality PRDs.

Product Idea Excavator is built for founders, builders, product managers, indie hackers, and anyone who has a product idea that still lives mostly in their head.

It does not start by writing a plan.

It starts by asking better questions.

## Why This Exists

Most planning workflows assume the goal is already clear. But early product ideas are rarely clear.

Users often start with:

- "I want to build an AI app."
- "I have a startup idea."
- "Help me write a PRD."
- "I want to make a product like..."
- "I know the feeling, but I cannot describe the product yet."

Ordinary planning mode can decompose a known goal. This Skill is different: it helps discover whether the goal is right in the first place.

It pushes on:

- who the first real user is
- what evidence proves demand
- what the current workaround costs
- what the narrowest useful version is
- where the product may fail
- what technical path is actually practical
- when to stop exploring and synthesize a PRD

## What Makes It Different

### 1. It interviews like a top product partner

The Skill leads the conversation. It asks one high-leverage question at a time, absorbs the user's answer, sharpens the assumptions, and moves to the next product dimension.

It avoids long questionnaires. The experience feels like a live product discovery session.

### 2. It treats interest and demand differently

"People like the idea" is not enough.

The Skill asks for stronger signals:

- users already paying
- users spending time or money on a workaround
- users asking when it ships
- users depending on a manual process
- users who would feel pain if the solution disappeared

### 3. It forces a narrow wedge

Instead of letting the product become a giant platform too early, the Skill looks for the smallest version that can create real value.

It asks:

- what can be useful this week
- what can be validated manually first
- which features are distracting
- what should explicitly not be in the MVP

### 4. It includes technical product judgment

The Skill does not stop at user needs. It also explores:

- target platform
- AI/model role
- data sources
- privacy and compliance
- permission boundaries
- integration needs
- technical reversibility
- MVP stack vs. long-term architecture

### 5. It automatically produces a PRD when discovery is complete

When the user confirms there is nothing else to add, the Skill synthesizes a PRD with:

- confirmed user intent
- inferred assumptions
- recommendations
- open questions
- MVP scope
- user journeys
- AI/model requirements
- technical stack
- metrics
- risks
- roadmap

## Example Use Cases

### Example 1: Voice Character App

Input:

> I want to build a voice app. Users say who they want to talk to, and the app constructs a character based on public information, background knowledge, voice style, and conversational personality.

The Skill will explore:

- whether the core use case is entertainment, learning, decision support, history immersion, or emotional companionship
- whether the first version should support any person or a curated character library
- how to handle public figures, voice likeness, disclaimers, and safety boundaries
- whether characters should answer from a knowledge base, a scripted persona card, or a hybrid system
- how to evaluate whether a character feels deep, useful, and safe
- what the MVP should include before scaling the character library

Possible PRD direction:

> A curated voice-based character intelligence app where users bring real questions and enter immersive conversations with high-quality simulated characters built from public sources, clear boundaries, and non-misleading voice design.

### Example 2: AI Customer Feedback Analyst

Input:

> I want an AI tool that helps product teams organize customer feedback and generate product requirements.

The Skill will push beyond "summarize feedback" and ask:

- where the feedback comes from
- who currently organizes it
- how much time the workaround costs
- what evidence proves teams need this
- whether the first version should integrate with tools or accept manual uploads
- how to distinguish evidence-backed insights from AI guesses

Possible MVP:

- paste or upload raw feedback
- generate insight cards
- cite representative customer quotes
- let the product manager select insights
- generate a PRD draft with assumptions clearly marked

### Example 3: Internal Knowledge Assistant

Input:

> I want to make an internal knowledge base for small teams.

The Skill will ask:

- what knowledge employees fail to find
- what happens when they cannot find it
- what current tools are used
- whether search, chat, workflow automation, or expert routing is the real product
- what permission model is required
- whether RAG is actually needed in v1

## Repository Structure

```text
product-idea-excavator/
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

docs/
  INSTALL.md
  USAGE.md
  EXAMPLES.md
  EVALUATION.md
  SAFETY.md
  ROADMAP.md
```

## Quick Start

1. Copy `product-idea-excavator/` into your local Skills directory.
2. Start a new session with your AI coding assistant.
3. Ask something like:

```text
我有一个产品 idea，但还不成熟。请用 product-idea-excavator 的方式来挖掘。
```

See [Installation](docs/INSTALL.md) and [Usage](docs/USAGE.md) for details.

## What A Good Session Feels Like

The Skill should not immediately write a PRD.

It should first ask:

- who is the first user
- what real situation triggered the idea
- what the user currently does instead
- what evidence proves the pain
- what the narrowest useful version is
- what technical choices are reversible or risky
- what needs to be true for this product to work

Only after discovery is complete should it synthesize the PRD.

## Safety And Boundaries

This Skill is designed for product discovery and specification writing. It does not encourage impersonation, deception, harmful automation, or unsafe advice.

For products involving public figures, voice, identity, financial decisions, medical advice, legal advice, emotional support, children, or political content, the Skill should surface safety, consent, labeling, and compliance questions early.

Read [Safety](docs/SAFETY.md).

## Evaluation

The repo includes starter evals in:

[product-idea-excavator/evals/evals.json](product-idea-excavator/evals/evals.json)

These test whether the Skill:

- asks instead of prematurely writing
- distinguishes demand from interest
- handles vague ideas
- challenges scope
- explores technology and AI implementation
- produces concrete PRD-ready material

Read [Evaluation](docs/EVALUATION.md).

## Roadmap

Planned improvements:

- more realistic multi-turn evals
- richer PRD examples
- packaging scripts
- multilingual support
- benchmark reports comparing this Skill against baseline planning behavior
- domain-specific packs for AI apps, marketplaces, B2B SaaS, internal tools, and consumer apps

Read [Roadmap](docs/ROADMAP.md).

## Contributing

Contributions are welcome. The most valuable contributions are:

- sharper interview questions
- better PRD examples
- stronger eval prompts
- new product archetype playbooks
- safety improvements
- real-world transcripts with sensitive details removed

Read [Contributing](CONTRIBUTING.md).

## License

MIT License. See [LICENSE](LICENSE).

