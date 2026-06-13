# AI Fullstack Learning Path

This is a 24-unit path for a frontend engineer becoming an AI fullstack engineer. It merges backend foundations and AI application development into one product-centered curriculum.

The point is not to finish two courses. The point is to build one credible product while gradually earning the backend, AI, safety, testing, and deployment judgment needed to explain it.

## Positioning

Target roles:

- Frontend Engineer with AI/fullstack product scope.
- AI Fullstack Engineer.
- AI Application Developer.
- Full-stack Product Engineer building LLM features.
- Internal tools / workflow automation engineer.

Not the primary target:

- ML Research Engineer.
- Model Training Engineer.
- Data Scientist.
- Infrastructure-only MLOps engineer.

## Path Principles

- Unit-based, not day-based.
- One product spine, not scattered demos.
- Every unit produces code, tests, evals, docs, or a design artifact.
- AI appears early enough to stay motivating, but never before server-side boundaries are safe.
- Frontend skill is treated as an advantage: UX states, streaming, schema contracts, trust signals, and product judgment matter.
- Optional tools stay optional: NestJS, Fastify, Drizzle, LangChain, LangGraph, GraphQL, queues, realtime, and deeper observability can be added after the core is stable.
- Core length stays at 24 units to reduce dropout. Breadth topics live in optional packs.
- Every phase should leave visible portfolio evidence, even if it is rough.

## Curriculum Benchmarks

This path is shaped by common fullstack/backend/AI application roadmaps and project-based curricula:

- Fullstack foundations: frontend framework, API, database, auth, testing, deployment, and CI.
- Backend production basics: validation, errors, security, observability, containers, and deployment.
- AI application engineering: server-owned model calls, streaming UX, structured outputs, tool calling, RAG, evals, safety, cost, and monitoring.

See `curriculum-benchmark-notes.md` when updating the curriculum scope.

## Default Product Spine

Use `workbench-ai`: an AI-enhanced task, project, and knowledge workflow app.

Core product capabilities:

- Users, organizations, projects, tasks, comments, and lightweight documents.
- Authentication, authorization, and tenant scoping.
- AI task summarization, structured task extraction, tool-assisted assistant actions, and document Q&A.
- Evals, safety notes, cost/latency logs, and deployment docs.

See `project-spine.md` before creating or changing the project.

## Unit Template

Each unit should state:

1. Goal.
2. Why it matters for frontend-to-AI-fullstack transition.
3. Artifact.
4. Starter files or project area.
5. Checkpoints.
6. Verification command or manual check.
7. Completion boundary.
8. Optional stretch outside the boundary.

## Phase 1: One Fullstack Spine

### U01 - AI Fullstack Orientation and Project Shell

Goal: Replace the split-course mindset with one product path.

Build: Course state files, project shell, package scripts, and a first architecture note.

Learn:
- What belongs to UI, API, database, and AI provider boundaries.
- Why API keys and model calls stay server-side.
- How this course records progress.

Done when:
- A project shell or unit lab exists.
- Progress/state files point to U01.
- The learner can explain the one-product path in their own words.

### U02 - TypeScript, Runtime, and Project Scripts

Goal: Make the local development loop predictable.

Build: TypeScript strict setup, package scripts, and a tiny server-side utility.

Learn:
- Node LTS vs current release.
- `package.json`, scripts, dependencies, dev dependencies.
- ESM, environment variables, process boundaries.

Done when:
- `typecheck` and a basic test/check script run.
- The learner can explain what Node provides that the browser does not.

### U03 - HTTP API Boundary and Validation

Goal: Build a safe server boundary before using databases or models.

Build: A health route and one typed API endpoint with Zod validation, consistent error envelopes, and one API boundary test.

Learn:
- Request/response lifecycle.
- Status codes and error envelopes.
- Runtime validation for untrusted input.

Done when:
- Valid input succeeds.
- Invalid input returns a clear error.
- The learner can distinguish TypeScript types from runtime validation.
- One test or manual request proves the error shape.

### U04 - First Product CRUD Slice

Goal: Build the first non-AI product loop.

Build: A minimal projects/tasks slice with UI, API, in-memory or file-backed data, and tests/manual checks.

Learn:
- Service boundaries vs UI component boundaries.
- CRUD semantics and client states.
- Basic test shape.

Done when:
- The learner can create and list a task.
- Loading, empty, and error states are visible or documented.

## Phase 2: First AI Product Experience

### U05 - First Server-Owned AI Feature

Goal: Add a real model call without leaking secrets or mixing concerns.

Build: A task-summary or project-assistant feature that calls an AI provider from the server.

Learn:
- Provider adapter.
- `.env.example` and server-only keys.
- Request/response shape and fallback errors.

Done when:
- A model-backed response works or is mockable behind the same adapter.
- API keys are not exposed to the client.
- One failure path is handled.

### U06 - Streaming UX, Cancel, and Retry

Goal: Make model output feel responsive and controllable.

Build: Streaming response UI with cancel, retry, disabled states, and partial rendering.

Learn:
- Token streaming.
- Abort behavior.
- Message lifecycle states.

Done when:
- Output visibly streams or a mock stream proves the state logic.
- Cancel and retry behave predictably.

### U07 - Prompt Contract and Tiny Evals

Goal: Treat prompts as testable product behavior.

Build: Prompt versions plus a tiny eval set for one AI feature.

Learn:
- System/developer/user instructions.
- Examples and constraints.
- Regression thinking for AI behavior.

Done when:
- At least three eval cases exist.
- One prompt failure is recorded and improved.

### U08 - Structured Output for UI and Business Logic

Goal: Stop parsing prose when the UI needs reliable data.

Build: A "requirement to tasks" or "meeting note to action items" feature with schema validation.

Learn:
- JSON/schema contracts.
- Refusal and malformed output handling.
- Rendering structured AI output.

Done when:
- Output is validated before use.
- Invalid or refused output does not break the UI.

## Phase 3: Database, Auth, and Trustworthy Product State

### U09 - PostgreSQL and Prisma Foundations

Goal: Move product state into a real database.

Build: Prisma schema, migration, seed, and repositories for users, projects, and tasks.

Learn:
- Tables, relations, constraints, indexes.
- Migrations and seeds.
- Repository boundary.

Done when:
- The local database can be reset and seeded.
- The app reads/writes through Prisma or a documented DB adapter.

### U10 - Product CRUD Depth

Goal: Make the product feel like a real business app.

Build: Comments, task status changes, pagination/filtering, integration tests, and documented API contracts.

Learn:
- Nested resources.
- Pagination and filtering.
- API contract discipline.
- Integration test setup and repeatable fixtures.

Done when:
- Core CRUD routes are tested or manually verified.
- A frontend client could implement against the documented responses.
- At least one negative case is covered.

### U11 - Authentication

Goal: Understand identity and session boundaries.

Build: Register/login/logout or a documented auth integration, plus `GET /me`.

Learn:
- Password/session/JWT tradeoffs.
- Cookies and bearer tokens.
- Secret handling.

Done when:
- Auth success and failure paths are tested or manually verified.
- The learner can explain why credentials are sensitive backend state.

### U12 - Authorization and Tenant Scoping

Goal: Prevent cross-user and cross-organization data leaks.

Build: Membership roles and tenant-scoped queries.

Learn:
- Authentication vs authorization.
- Role/policy checks.
- Tenant-aware data access.

Done when:
- Tests or manual checks prove one user cannot access another organization's data.
- AI features are also scoped to authorized data.

## Phase 4: AI as a Product System

### U13 - Tool Calling With Server-Owned Tools

Goal: Let the assistant use app functions safely.

Build: Two typed tools, such as search tasks and draft a task update.

Learn:
- Tool schemas.
- Server-owned execution.
- Tool traces and permission checks.

Done when:
- Tool calls are inspectable.
- Unsafe or unauthorized tool calls are rejected.

### U14 - Human Approval for AI Mutations

Goal: Keep the model from directly mutating sensitive state.

Build: A draft/confirm flow for AI-created tasks, comments, or status updates.

Learn:
- Confirmation boundaries.
- Auditability.
- UX for AI suggestions.

Done when:
- AI can propose a change.
- The user must approve before persistent mutation.

### U15 - RAG Basics Over Product Documents

Goal: Answer from project documents instead of model memory.

Build: Document ingestion, chunking, retrieval, answer generation, and citations.

Learn:
- Chunking.
- Embeddings or mock retrieval for early setup.
- Grounded answers and "I don't know."

Done when:
- Answers cite retrieved sources.
- Weak retrieval leads to refusal or uncertainty.

### U16 - RAG Quality and Retrieval Evals

Goal: Improve answer quality deliberately.

Build: Retrieval eval questions, metadata filters, before/after comparison, and citation quality notes.

Learn:
- Recall vs precision.
- Chunk size and metadata.
- Reranking as an optional tool.

Done when:
- At least one measured retrieval failure improves.
- The learner can explain the tradeoff that changed.

### U17 - Files or Multimodal Input

Goal: Add one non-plain-text input without turning the course into ML research.

Build: Either file upload analysis, screenshot feedback, or voice-note summarization.

Learn:
- File boundaries.
- Privacy and retention concerns.
- Structured analysis results.

Done when:
- One real file/image/audio path is accepted or convincingly mocked.
- Privacy and size/type checks are documented.

## Phase 5: Safety, Reliability, and Operations

### U18 - Web and AI Security

Goal: Defend the product against common API risks and unsafe model/tool behavior.

Build: API abuse cases, prompt-injection cases, tool permission checks, output validation, rate-limit or abuse notes, and audit notes.

Learn:
- Broken access control and sensitive data exposure.
- Prompt injection.
- Data exfiltration risks.
- Defense in depth.

Done when:
- At least three API/AI attack cases are tested or documented.
- Mitigations are implemented or clearly scoped.

### U19 - Cost, Latency, and Resilience

Goal: Make AI features operable.

Build: Timeouts, retries, fallbacks, estimated cost tracking, and slow-provider behavior.

Learn:
- Retry boundaries.
- Model/provider fallback.
- Cost and latency UX.

Done when:
- A slow or failed model response has a predictable fallback.
- Cost/latency can be inspected.

### U20 - Logging, Metrics, and Basic Tracing

Goal: Debug production behavior without guessing.

Build: Request IDs, structured logs, health checks, and basic metrics/traces.

Learn:
- Correlation IDs.
- Liveness/readiness.
- RED metrics and trace basics.

Done when:
- One request can be followed through logs.
- Health checks and at least one metric exist.

### U21 - Docker Local Stack

Goal: Make the app reproducible outside the learner's machine.

Build: Dockerfile and Compose setup for app plus database.

Learn:
- Images, containers, networks, volumes.
- Production vs development builds.
- Readiness and startup order.

Done when:
- A fresh local stack can start from documented commands.
- The app serves a health route in a container.

## Phase 6: Shipping and Portfolio

### U22 - CI and Quality Gates

Goal: Catch regressions automatically.

Build: A single `check` command and CI workflow for typecheck, lint, tests, and build.

Learn:
- Quality gates.
- Test isolation.
- Service containers when database tests need them.

Done when:
- One command catches common mistakes.
- CI would fail on a type, test, lint, or build error.

### U23 - Deployment and Production Config

Goal: Explain how the product runs outside local development.

Build: Deployment notes or config for one platform, env docs, migration plan, and secrets checklist.

Learn:
- Build vs runtime.
- Secrets and environment separation.
- Migration deployment risks.

Done when:
- The learner can explain app, database, secrets, migrations, and AI provider config in production.

### U24 - Portfolio Review and Interview Defense

Goal: Turn the learning product into credible evidence.

Build: Final README, architecture diagram, demo flow, eval report, safety notes, and next-improvement plan.

Learn:
- Technical storytelling.
- Tradeoff defense.
- Honest limitations.

Done when:
- The app runs locally or has clear run instructions.
- Quality checks pass or gaps are documented.
- The learner can defend major decisions and name the next three improvements.

## Optional Packs

Use only after the core is stable or when the learner explicitly requests them:

- Fastify or NestJS comparison.
- Drizzle comparison.
- GraphQL or realtime updates.
- Redis/BullMQ background jobs.
- LangChain/LangGraph orchestration.
- MCP integration.
- Deeper OpenTelemetry and load testing.
- Provider/model comparison.
- Realtime voice or WebRTC assistant.
- Advanced agent workflows with durable state and human-in-the-loop.

## Phase Exit Evidence

After each phase, the learner should have something concrete:

- Phase 1: runnable shell, API boundary, first CRUD slice.
- Phase 2: first AI feature, streaming UX, prompt/eval notes, structured output.
- Phase 3: database-backed product state, auth, authorization, tenant scope.
- Phase 4: tool calling, approval flow, RAG, retrieval quality evidence, file/multimodal boundary.
- Phase 5: security notes, cost/latency handling, logs/metrics/tracing, Docker stack.
- Phase 6: CI, deployment plan, portfolio README, architecture diagram, eval/safety report, interview defense.
