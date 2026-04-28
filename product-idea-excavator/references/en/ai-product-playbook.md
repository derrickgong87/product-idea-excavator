# AI Product Playbook

## Is AI Necessary?

Ask:

- Can this be solved without AI?
- Is AI the core value or an efficiency layer?
- Will users accept uncertainty?
- What damage happens if the AI is wrong?
- Does AI create a 10x result, or just replace a button with a chat box?

If rules, search, or workflow automation are enough, do not force AI.

## AI Role Types

Common roles:

- generate
- summarize
- search
- recommend
- classify or judge
- plan
- execute
- collaborate

## Quality Standards

Define:

- accuracy
- recall
- user satisfaction
- correction rate
- hallucination rate
- average latency
- cost per task
- recovery rate

If these are not defined, mark AI quality as a high-risk assumption.

## Failure Handling

When AI fails, the product can:

- show uncertainty
- ask for confirmation
- cite sources
- allow editing
- fall back to templates or rules
- route to a human
- save drafts instead of executing

High-risk use cases should default to "suggest -> user confirms -> execute."

## Agent Boundaries

Agent products must define:

- which tools can be called
- which tools cannot be called
- which actions require confirmation
- how every step is logged
- how to undo actions
- how to limit cost
- how to stop loops and failures

High-risk actions include sending messages, publishing content, modifying production data, charging/refunding, deleting data, or calling external systems with irreversible effects.

## RAG

RAG fits when:

- users need answers grounded in private or changing knowledge
- citations are required
- data updates frequently
- fine-tuning is not appropriate

RAG requires permissions, chunking, retrieval, reranking, citations, and evals.

## Model Choice

Do not assert latest model capabilities, prices, or context limits from memory. If the user needs current details, verify them.

Choose models based on:

- text, image, audio, video, code, or multimodal need
- long context
- latency
- cost
- privacy
- tool calling
- structured output
- stability

