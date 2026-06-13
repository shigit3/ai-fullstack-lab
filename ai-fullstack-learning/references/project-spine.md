# Project Spine: workbench-ai

Use this file to keep the course from becoming scattered.

## Product Idea

`workbench-ai` is an AI-enhanced task, project, and knowledge workflow app. It starts as a traditional fullstack product and grows AI features only where they serve real product workflows.

## Core Domain

Entities:

- User.
- Organization.
- Membership and role.
- Project.
- Task.
- Comment.
- Document or note.
- AI request log.
- Eval case.

Core flows:

- Create and manage projects/tasks.
- Comment on tasks.
- Authenticate users.
- Scope data by organization.
- Ask AI to summarize, draft, extract, search, or answer from authorized data.

## AI Features

Add these in order:

1. Task or project summary.
2. Streaming assistant response.
3. Structured task extraction.
4. Tool-assisted assistant that can search authorized tasks.
5. Human-approved AI draft mutation.
6. Document Q&A with citations.
7. Retrieval evals and safety checks.

Do not add autonomous mutation before auth, authorization, and confirmation boundaries are clear.

## Architecture Defaults

Use a shape like:

```text
workbench-ai/
  app-or-src/
  server-or-api/
  prisma/
  tests/
  evals/
  docs/
```

Exact folders should follow the chosen framework.

Keep boundaries visible:

- UI components own interaction state.
- API/server routes own validation, auth, provider calls, and response envelopes.
- Services own business decisions.
- Repositories own database queries.
- AI adapters own provider-specific details.
- Evals own repeatable behavior checks.

## What Not To Build Early

Avoid early expansion into:

- Multiple AI providers before one path works.
- Agent frameworks before simple tool calling is understood.
- Full realtime/voice before basic streaming is stable.
- Complex vector infrastructure before a small RAG loop works.
- Admin dashboards before core user flows work.

Record these ideas as future work and return to the current unit.

## Portfolio Evidence

By U24, the project should show:

- Fullstack CRUD with database persistence.
- Auth and tenant-aware permissions.
- At least two AI product features.
- Streaming or responsive AI UX.
- Structured output or tool calling.
- RAG or document-grounded answers.
- Evals and safety notes.
- Cost/latency or logging evidence.
- Deployment or local run instructions.
- Honest limitations and next improvements.

