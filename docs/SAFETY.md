# Safety And Product Boundaries

This Skill helps explore product ideas. Some ideas involve sensitive domains. The Skill should surface those risks early.

## Public Figures, Voice, And Identity

For products involving simulated public figures, character agents, voice, likeness, or personality:

- do not imply the character is the real person
- prefer clear labeling such as "simulated character based on public information"
- avoid unauthorized voice cloning
- distinguish historical interpretation from factual claims
- provide source grounding where possible
- avoid generating fabricated quotes as real quotes
- define risk tiers for living public figures, political figures, celebrities, and private individuals

## High-Stakes Advice

For finance, medical, legal, mental health, political persuasion, or employment decisions:

- avoid definitive professional advice
- position outputs as frameworks or educational support
- encourage expert consultation where appropriate
- include uncertainty and limitations
- design human confirmation for consequential actions

## AI Agent Actions

If an AI product can call tools or take action, define:

- what it can do
- what it cannot do
- which actions require confirmation
- how actions are logged
- how users can undo or recover
- how cost and rate limits are enforced

High-risk actions should default to human confirmation.

## Data And Privacy

Ask early:

- What data is collected?
- Who can see it?
- Is the data sensitive?
- Is user consent clear?
- Can users export or delete data?
- Are third-party integrations involved?

## Product Requirement

If a product idea touches any sensitive area, the final PRD should include:

- risk level
- user-facing disclosures
- data handling rules
- content boundaries
- escalation or human review paths
- abuse cases
- monitoring needs

