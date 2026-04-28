# PRD Template And Quality Bar

Use this template when the user confirms that product discovery is complete. Adapt it to the product; do not mechanically fill every section if it does not apply.

## PRD Title

Format: `# [Product Name] PRD`

## 1. One-Sentence Summary

State:

- who it is for
- what problem it solves
- how it solves it
- what outcome it creates

## 2. Background And Opportunity

Explain:

- why this product is needed now
- why current solutions are insufficient
- what opportunity window exists

Mark what is confirmed, inferred, recommended, or still open.

## 3. Target Users And Personas

Include:

- first user segment
- user, buyer, decision-maker, and operator if different
- current workflow
- pain frequency and severity
- motivation to switch

## 4. Problem Definition

Describe the problem through a concrete user scenario:

- trigger moment
- current behavior
- cost of the pain
- why the problem is worth solving

Avoid generic phrases such as "low efficiency" or "bad experience."

## 5. Current Alternatives

List what users do today:

- manual work
- spreadsheets or docs
- chat tools
- internal systems
- competitors
- doing nothing

Explain the cost and weakness of each alternative.

## 6. Demand Evidence

Separate:

- strong evidence
- medium evidence
- weak signals
- unvalidated assumptions

Strong evidence can include payment, prepayment, repeated use, real data shared, workflow dependency, or urgent complaints when the process breaks.

## 7. Narrowest Wedge

Define:

- first user segment
- smallest valuable result
- smallest deliverable form
- why this wedge is better than a full platform for v1
- what is intentionally out of scope

## 8. Core Value Proposition

State the core promise and the first moment when the user feels value.

## 9. Goals And Non-Goals

Goals:

- what the MVP validates
- what user behavior should happen
- what business or learning outcome matters

Non-goals:

- what v1 intentionally does not do
- tempting features to defer

## 10. MVP Scope

Use P0/P1/P2:

- P0: required to validate value
- P1: valuable but deferrable
- P2: future roadmap

For each feature, include user value, description, and priority rationale.

## 11. Core User Journey

At minimum, include:

1. entry point
2. starting state
3. user input or selection
4. system processing
5. output/result
6. user confirmation, edit, share, or export
7. follow-up/retention action

Include failure and recovery paths.

## 12. Functional Requirements

For each major feature:

- feature name
- user story
- trigger
- main flow
- edge cases
- acceptance criteria

## 13. Non-Functional Requirements

Cover as relevant:

- performance
- availability
- security
- privacy
- compliance
- scalability
- observability
- multi-platform behavior

## 14. UX Requirements

Cover:

- first-run experience
- empty states
- loading states
- error states
- permission denial
- uncertainty and failure states for AI
- trust and explainability

## 15. Data Requirements

Include:

- core objects
- data sources
- fields
- permissions
- lifecycle
- import/export

## 16. AI / Model Requirements

If applicable:

- AI role
- inputs
- outputs
- model capability requirements
- RAG / Agent / tool calling / multimodal needs
- eval metrics
- hallucination and error handling
- human review
- latency and cost constraints

## 17. Technical Stack Recommendation

Use:

```text
Recommended stack:
- Frontend:
- Backend:
- Database:
- Auth:
- AI / model layer:
- File / object storage:
- Payments:
- Notifications:
- Analytics:
- Deployment:
- Monitoring and logs:
- Admin tooling:

Why this fits:
- ...

Tradeoffs:
- ...

MVP shortcut:
- ...

When to switch:
- ...
```

## 18. System Architecture

Explain:

- main modules
- data flow
- third-party integrations
- async jobs
- permission boundaries
- logs and auditability

## 19. Roles And Permissions

Define relevant roles such as user, admin, reviewer, teammate, or external collaborator.

## 20. Integrations

List required and optional integrations, APIs, webhooks, imports, and exports.

## 21. Admin / Operations

Explain what operators need to view, edit, review, approve, or fix.

## 22. Metrics

Include:

- north-star metric
- activation metric
- retention metric
- conversion metric
- quality metric
- business metric
- guardrail metric

For AI products, also include accuracy, correction rate, hallucination rate, latency, and cost per task when relevant.

## 23. Edge Cases And Failure States

Include:

- no data
- bad data
- permission denied
- integration failure
- AI failure
- user abandons flow
- payment failure
- duplicate submission

## 24. Premise Challenge And Alternatives

Write:

- key premises
- riskiest premise
- at least two alternative paths
- recommended path and why
- what the user confirmed or still needs to decide

## 25. Risks And Validation Plan

Cover product, technical, market, data, compliance, and AI quality risks.

For each risk, include impact and validation method.

## 26. Roadmap

Split into:

- MVP
- V1
- V2
- long-term direction

## 27. Product Recommendations

State:

- recommended wedge
- scope to cut
- key validation experiment
- capability worth designing early
- metric or assumption most likely to mislead the team

## 28. Open Questions

List unresolved questions. Do not hide uncertainty.

