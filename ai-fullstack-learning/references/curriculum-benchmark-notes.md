# Curriculum Benchmark Notes

Use this file when evaluating or changing the curriculum scope. Do not load it during ordinary unit sessions unless the learner asks why the path is shaped this way.

## Public Routes Considered

- Full-stack roadmaps commonly include HTML/CSS/JS, Git, package managers, frontend framework, backend APIs, databases, auth, testing, deployment, security, and CI.
- Modern backend roadmaps emphasize HTTP, API design, databases, caching/queues/search as optional breadth, security, observability, containers, and deployment.
- AI engineer/application routes add LLM APIs, prompt contracts, structured outputs, tool calling, RAG, agents/workflows, evals, safety, cost, latency, and monitoring.
- Project-based courses such as Full Stack Open and The Odin Project are effective because they keep learners building, testing, integrating, and shipping instead of only reading concepts.

## Design Decision

Keep the core at 24 units:

- Short enough to finish.
- Long enough to cover fullstack, AI product behavior, security, operations, and portfolio evidence.
- Every 2-3 units should create a visible product win.
- Optional packs hold breadth topics that would otherwise make the course feel endless.

## Coverage Targets

The core path should include:

- Fullstack product shell and TypeScript development loop.
- HTTP/API boundaries, validation, error responses, and integration testing.
- Database modeling, migrations, seed data, repository boundaries, and query basics.
- Auth, authorization, tenant scoping, and web/API security.
- AI provider adapters, server-owned model calls, streaming UX, structured output, tool calling, human approval, and RAG.
- Evals, safety, cost/latency, logs, metrics, tracing, Docker, CI, deployment, and portfolio defense.

## Anti-Dropout Rules

- Keep one product spine.
- Keep unit completion boundaries small.
- Avoid optional framework comparisons in the core.
- Add AI early enough to stay motivating, but after server-side key boundaries are safe.
- Put heavy breadth into optional packs.
- Make each phase produce evidence the learner can show or explain.
