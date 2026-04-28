# Product Idea Excavator

> A bilingual product discovery Skill that turns vague product ideas into sharp product thinking and high-quality PRDs.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-English%20%7C%20中文-blue.svg)](docs/I18N.md)
[![PRD](https://img.shields.io/badge/output-PRD-orange.svg)](product-idea-excavator/references/en/prd-template.md)

Languages: English | [中文说明](docs/README.zh-CN.md)

See [Bilingual Strategy](docs/I18N.md) for how the Skill serves Chinese and English users without mixing the two experiences.

Product Idea Excavator is built for founders, builders, product managers, indie hackers, and anyone who has a product idea that still lives mostly in their head.

It does not start by writing a plan.

It starts by asking better questions.

## At A Glance

Product Idea Excavator is for the messy early stage before a product spec exists.

It helps an AI assistant behave less like a passive note-taker and more like a strong product partner:

- it leads the interview instead of waiting for the user to structure the idea
- it asks one high-leverage question at a time
- it separates real demand from casual interest
- it challenges weak assumptions without derailing the conversation
- it narrows the idea into a concrete MVP wedge
- it asks about technical stack, model choices, data, permissions, safety, and cost
- it produces a detailed PRD only after the user confirms discovery is complete

The result is not just a cleaner document. The result is better product thinking before the document exists.

## Who It Is For

- Founders turning a rough startup idea into a testable product
- Product managers preparing a PRD from scattered conversations
- Indie builders deciding what to build first
- AI product teams clarifying model role, data flow, and failure modes
- Engineers who need a product-quality spec before implementation
- Creators and operators who know the pain but do not yet know the product shape

## Commercial Use

This project is open source under the MIT License.

You can use it for personal, commercial, internal, client, educational, or startup work. You can copy it, modify it, package it into your own workflow, and use it to produce PRDs for real products, as long as you follow the license terms.

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

## Bilingual By Design

This repository uses one Skill for both Chinese and English users.

- Chinese prompt -> Chinese interview -> Chinese PRD
- English prompt -> English interview -> English PRD
- Mixed prompt -> follow the language of the product idea itself

The Skill keeps each session in one language unless the user explicitly asks for bilingual output. This avoids splitting the project into separate repositories while keeping the user experience clean.

Why this matters:

- English users should not feel they are using a translated Chinese project.
- Chinese users should not be pushed into English terminology unless it is natural.
- Maintainers should not have to manage two separate repos, issue trackers, release histories, and communities.
- The same product discovery method should work across both languages with language-specific examples and templates.

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

### 6. It carries a product-quality bar inside the Skill

The Skill includes reference playbooks for:

- discovery questions
- PRD structure
- product sense
- technical stack decisions
- AI product design
- example interview patterns

This makes the behavior more consistent than a generic prompt. The assistant can consult the relevant reference only when needed, keeping the conversation focused while preserving depth.

## How It Works

The Skill follows a simple but powerful loop:

1. Absorb the user's latest answer.
2. Extract one confirmed fact, assumption, or risk.
3. Offer options or a recommendation when the idea is immature.
4. Ask the next most important question.
5. Keep an internal map of users, problems, demand evidence, MVP scope, technical choices, risks, and open questions.
6. Generate the PRD after the user confirms the discovery is complete.

It does not try to ask every possible question at once. A good session should feel like a serious product conversation, not a form.

## What The PRD Covers

The final PRD can include:

- product name and one-sentence summary
- background and opportunity
- target users and personas
- problem definition
- current alternatives
- demand evidence
- narrowest wedge
- value proposition
- goals and non-goals
- MVP scope
- core user journeys
- functional requirements
- non-functional requirements
- UX requirements
- data requirements
- AI/model requirements
- technical stack recommendation
- system architecture
- roles and permissions
- integrations
- admin and operations needs
- metrics
- edge cases and failure states
- premise challenges and alternatives
- risks and validation plan
- roadmap
- open questions

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

Why the Skill helps:

- It prevents the idea from collapsing into "just make many characters."
- It asks what conversations users actually want to have.
- It surfaces identity, consent, voice, safety, knowledge-source, and evaluation questions early.
- It pushes toward a first version that can be tested before building a huge character library.

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

Why the Skill helps:

- It distinguishes summarization from decision support.
- It asks who owns the workflow today and what output they trust.
- It forces the product to cite evidence instead of inventing product strategy.

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

Why the Skill helps:

- It asks whether the real product is search, chat, workflow automation, or expert routing.
- It treats permissions and stale knowledge as product requirements, not late engineering details.
- It can recommend a practical MVP stack instead of defaulting to an overbuilt architecture.

### Example 4: Churn Prediction For Customer Success

Input:

> I want to build a SaaS product for customer success teams that predicts churn and tells them what action to take.

The Skill will explore:

- which customer segment has enough clean data for the first version
- whether the user needs prediction, prioritization, playbooks, or workflow automation
- what current signals customer success teams already trust
- whether the product should start as an alerting tool, dashboard, or action workspace
- what false positives and false negatives cost
- what model quality bar is required before users rely on it

Possible MVP:

- connect one source of customer activity data
- compute a simple risk score with transparent reasons
- show the top accounts needing attention
- recommend one next action per account
- let the user mark whether the recommendation was useful

### Example 5: Personal Growth App

Input:

> I want to build an app for personal growth, but I do not know the exact product yet.

The Skill will not get stuck. It can suggest several possible directions:

- daily reflection and journaling
- decision coaching
- goal tracking
- emotional pattern discovery
- habit accountability

Then it will recommend a path, ask the user to choose or correct it, and continue into target users, first-use moment, retention loop, safety boundaries, and MVP.

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

docs/
  INSTALL.md
  USAGE.md
  README.zh-CN.md
  I18N.md
  EXAMPLES.md
  EVALUATION.md
  SAFETY.md
  ROADMAP.md
```

## Quick Start

1. Copy `product-idea-excavator/` into your local Skills directory.
2. Start a new session with your AI coding assistant.
3. Ask something like:

English:

```text
I have a product idea, but it is still fuzzy. Use product-idea-excavator to help me excavate it through questions.
```

中文：

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
- additional language and domain packs
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
