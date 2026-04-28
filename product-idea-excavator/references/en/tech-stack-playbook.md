# Technical Stack Playbook

Technical recommendations must serve the product stage, team ability, and user outcome.

## Principles

- Mature by default: prefer proven technology unless new technology clearly improves the product.
- Reversible early: choose options that are easy to replace in the MVP.
- Complete enough: do not defer error handling, logging, permissions, and basic tests if they are cheap to include.
- Validate before scaling architecture.
- Observability is a product capability: key flows should expose success, failure, latency, cost, and behavior.

## Decision Variables

Ask:

- target platform
- team skills
- launch timeline
- budget
- expected scale
- data sensitivity
- compliance needs
- payments
- real-time collaboration
- third-party integrations
- admin operations
- AI requirements
- reversible vs. irreversible choices

## Web SaaS MVP

Default:

- Frontend: Next.js + TypeScript + React + Tailwind
- Backend: Next.js API routes / server actions; split services later if needed
- Database: Postgres
- ORM: Prisma or Drizzle
- Auth: Clerk or Auth.js
- Payments: Stripe
- Analytics: PostHog
- Deployment: Vercel
- Monitoring: Sentry plus platform logs

Quality gate:

- key journey events tracked
- visible error states
- admin path for bad data
- export for important data
- basic automated tests or explicit test plan

## AI Web Product

Default:

- Web layer: Next.js + TypeScript
- Model layer: Vercel AI SDK or similar abstraction
- Database: Postgres
- Retrieval: pgvector first; dedicated vector DB only when justified
- File storage: S3 / R2 / Blob
- Queue: add when long-running tasks appear
- Evals: small eval set from day one
- Cost logs: model, tokens, latency, output quality

Validate quality before building complex Agent workflows.

## AI Agent Product

Must define:

- tool permissions
- task state machine
- human confirmation points
- retry behavior
- audit logs
- rollback or undo
- cost ceilings
- observability
- eval harness

Default safety posture:

- suggestions before execution
- drafts before publishing
- human confirmation before irreversible actions
- every action logged

## RAG Product

Must define:

- data sources
- chunking
- metadata
- permission filtering
- retrieval
- reranking
- citations
- confidence
- evals
- user feedback loop

The core experience is not "it answers"; it is "the answer is trustworthy."

## Internal Tool

Default:

- earliest: Retool / Appsmith / spreadsheet automation
- custom: Next.js + Postgres + RBAC
- must-have: operation logs, permissions, import/export, exception handling

Internal tools usually fail from missing permissions, auditability, and correction workflows, not from ugly UI.

## Mobile Product

Default:

- MVP: React Native / Expo
- Native: Swift / Kotlin when deep platform capabilities or high performance are required
- Backend: Postgres + API
- Push: platform push
- Analytics: mobile event tracking

## Enterprise B2B

Prioritize:

- SSO/SAML
- RBAC
- audit logs
- data isolation
- webhooks
- queues
- monitoring
- backups
- compliance path

If the first customers are not enterprise buyers, do not promise full enterprise capability too early.

