# Unit Checkpoints

Give the learner only the next checkpoint unless they ask for the whole map.

## U01 - AI Fullstack Orientation and Project Shell

1. Create or confirm course state files.
2. Create the project shell or first unit lab.
3. Write a four-box system map: UI, API, database, AI provider.
4. Explain why this is one course, not two.

## U02 - TypeScript, Runtime, and Project Scripts

1. Add TypeScript strict config.
2. Add `typecheck` and one check/test script.
3. Print or inspect runtime/config information.
4. Explain what Node provides beyond the browser.

## U03 - HTTP API Boundary and Validation

1. Add a health route.
2. Add one typed endpoint.
3. Validate input with Zod or equivalent.
4. Return a consistent error envelope.

## U04 - First Product CRUD Slice

1. Create a task/project data shape.
2. Add create/list API flow.
3. Add minimal UI states.
4. Verify success and one error path.

## U05 - First Server-Owned AI Feature

1. Create `.env.example`.
2. Add provider adapter stub.
3. Add server route for one AI feature.
4. Render response in the UI.
5. Handle provider failure or mock fallback.

## U06 - Streaming UX, Cancel, and Retry

1. Identify current non-streaming flow.
2. Stream or mock incremental output.
3. Render partial output.
4. Add cancel.
5. Add retry.

## U07 - Prompt Contract and Tiny Evals

1. Pick one behavior to stabilize.
2. Write prompt v1 and three eval inputs.
3. Record outputs and one failure.
4. Improve prompt and compare.

## U08 - Structured Output for UI and Business Logic

1. Choose a structured feature.
2. Define schema and TypeScript type.
3. Validate model output.
4. Render structured result.
5. Handle malformed/refused output.

## U09 - PostgreSQL and Prisma Foundations

1. Confirm local database approach.
2. Define core models.
3. Run migration or document setup.
4. Seed sample data.
5. Read/write through a repository.

## U10 - Product CRUD Depth

1. Add comments or status transitions.
2. Add pagination/filtering.
3. Document API contract.
4. Add one integration or repeatable manual test.
5. Cover one negative case.

## U11 - Authentication

1. Choose session/JWT/local auth approach.
2. Implement register/login or integration stub.
3. Add `GET /me`.
4. Test success and failure paths.

## U12 - Authorization and Tenant Scoping

1. Model membership and roles.
2. Add policy helper.
3. Scope queries by organization.
4. Add a negative access test.
5. Ensure AI features use scoped data.

## U13 - Tool Calling With Server-Owned Tools

1. Define two safe tools.
2. Write tool schemas.
3. Execute tools server-side.
4. Show traces or logs.
5. Reject unauthorized tool use.

## U14 - Human Approval for AI Mutations

1. Pick one AI-suggested mutation.
2. Generate a draft.
3. Add confirm/cancel UI.
4. Persist only after approval.
5. Log or document the audit boundary.

## U15 - RAG Basics Over Product Documents

1. Create a small document corpus.
2. Chunk documents.
3. Retrieve relevant chunks.
4. Generate grounded answer.
5. Render citations.
6. Refuse weak-context answers.

## U16 - RAG Quality and Retrieval Evals

1. Create five retrieval eval questions.
2. Record current failures.
3. Adjust chunking, metadata, or ranking.
4. Compare before/after.
5. Explain the quality tradeoff.

## U17 - Files or Multimodal Input

1. Add upload or capture UI.
2. Validate file size/type.
3. Send or mock non-text input.
4. Render structured analysis.
5. Document privacy and retention.

## U18 - Web and AI Security

1. Write three API/AI attack cases.
2. Add input/tool/output mitigations.
3. Add permission checks or abuse boundary notes.
4. Re-test attack cases.
5. Document residual risk.

## U19 - Cost, Latency, and Resilience

1. Add request timing.
2. Track estimated cost or token usage if available.
3. Add timeout.
4. Add fallback behavior.
5. Simulate slow/failing provider.

## U20 - Logging, Metrics, and Basic Tracing

1. Add request IDs.
2. Add structured logs.
3. Add liveness/readiness health checks.
4. Add one metric.
5. Trace one request path.

## U21 - Docker Local Stack

1. Add Dockerfile.
2. Add Compose app and database services.
3. Add `.dockerignore`.
4. Document startup commands.
5. Verify health route in container.

## U22 - CI and Quality Gates

1. Add one `check` command.
2. Add typecheck/lint/test/build steps.
3. Add CI workflow.
4. Include database service if needed.
5. Verify a failing check fails locally or in CI design.

## U23 - Deployment and Production Config

1. Pick one deployment target.
2. Document env vars and secrets.
3. Document migration plan.
4. Document AI provider config.
5. Explain rollback or failure handling.

## U24 - Portfolio Review and Interview Defense

1. Run quality gate.
2. Finish README and demo flow.
3. Add architecture diagram.
4. Add eval and safety notes.
5. Practice interview defense.
6. Name next three improvements.
