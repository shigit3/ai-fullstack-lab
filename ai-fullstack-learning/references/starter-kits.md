# Starter Kits

Use starter kits to reduce setup friction while preserving real practice. The default is guided starter, not a blank page and not a finished solution.

## Modes

### guided-starter

Default. Create the smallest useful scaffold:

- Unit folder or project area.
- README or task brief.
- TODO markers.
- Thin code stubs.
- Sample data.
- Test, eval, or manual check.
- `.env.example` when external services are involved.

Leave the core implementation to the learner.

README and TODO files are not the main teacher. They exist to record the task, commands, acceptance criteria, and future resume point. The chat response must still provide the learner's next action without requiring them to open the file.

### blank-build

Use only when the learner asks to start from zero. Provide requirements, acceptance criteria, edge cases, and verification. Do not generate files unless asked.

### walkthrough

Use only after the learner has attempted the task or explicitly asks for a full explanation. Show implementation in small chunks and explain decisions.

## Exercise Prompt Contract

Every generated checkpoint, lab, or TODO file should start from the task boundary, not the answer.

Include:

- Deliverable: the exact file, function, route, UI state, eval, or document to produce.
- Acceptance criteria: observable conditions that make the work acceptable.
- Edge case: one failure, invalid input, permission issue, slow path, or changed requirement to handle.
- Verification: a command, test, eval, curl/browser check, or manual inspection step.
- Hint policy: state that hints are available, but do not include the solution unless the learner asks.
- Knowledge check: one small prompt such as predict output, explain a boundary, or identify a failure mode.

Keep explanations short and placed near the task they unlock. Avoid broad theory sections in starter files.

Starter files should mirror the chat task card. Avoid long README tutorials that compete with the live coaching flow.

## TODO Quality Contract

Generated TODOs must be neither answer-shaped nor cliff-shaped.

Answer-shaped TODOs are not allowed:

- Do not leave commented-out final code.
- Do not write comments that say the exact chain of methods, operators, or statements to use.
- Do not make the learner's job "uncomment, assign, paste, or copy this solution."
- Do not put full solutions in README, TODO, fixture comments, or test names.

Cliff TODOs are not allowed:

- Do not write vague tasks like "implement auth", "add RAG", or "handle errors" without a first move.
- Do not require multiple new concepts in one TODO.
- Do not ask for architecture design before the learner has seen a small concrete version.

Good TODOs should include:

- Intent: what behavior should exist.
- Boundary: what file/function/route is in scope.
- Inputs and outputs.
- One edge case.
- Verification.
- The first observable move, not the whole implementation.

Example:

```ts
// TODO: Implement createTask(input).
// Scope: validate title/status, return a Task object, and do not mutate the input.
// Edge case: reject an empty title with a clear Error.
// Check: npm test -- createTask
```

Do not write:

```ts
// TODO: return { id: crypto.randomUUID(), title: input.title.trim(), status: input.status ?? "todo" }
```

## Difficulty Ladder

Use three TODO levels:

- Level 1, mechanical: small syntax or wiring task for unfamiliar tooling.
- Level 2, guided: one function, route, component state, test, eval, or schema with clear boundaries.
- Level 3, independent: a small feature slice after the learner has already practiced the pattern.

Default to Level 2. Use Level 1 briefly, then move on. Use Level 3 only after a related Level 2 task was completed.

If the learner finishes by copy/paste or comment removal, the TODO was too revealing. If the learner cannot identify the first edit, the TODO was too broad.

## Scaffold Fading

Choose the lightest scaffold that keeps the learner moving:

1. Task only: for familiar patterns.
2. TODO scaffold: for most implementation work.
3. Adjacent worked example: for a new concept, using a similar but not identical problem.
4. Partial sketch: when the learner is stuck after a real attempt.
5. Full walkthrough: only on explicit request or after repeated blockers.

Starter files should be easy to delete or complete. Avoid hiding important logic inside opaque helper code.

## Code Ownership

Starter files should make ownership visible:

- Codex may write setup, imports, empty function signatures, test harnesses, sample data, schema shells, route shells, and TODO boundaries.
- Learner should write core branching, data transformation, validation decisions, permission checks, provider calls, retrieval logic, eval assertions, and production tradeoff notes.
- If Codex writes a full solution in walkthrough mode, add a transfer task immediately after: change one requirement, explain one boundary, or add one edge case.

## Default Layout

If no suitable project exists:

```text
ai-fullstack-lab/
  AI_FULLSTACK_PROGRESS.md
  ai-fullstack-labs/
    LEARNING_STATE.md
    Uxx-unit-name/
      README.md
      TODO.md
      samples/
      test-or-evals/
  workbench-ai/
```

Use `ai-fullstack-labs/` for early standalone units and `workbench-ai/` for the long-running product once it exists.

## Safety Rules

- Inspect the current directory before creating files.
- Reuse existing package manager and conventions.
- Ask before installing dependencies or using network access.
- Ask before overwriting broad project areas.
- Never request API keys in chat.
- Create `.env.example`, not `.env`, unless the learner explicitly asks and provides local values outside chat.
- Do not commit secrets, generated build output, database files, logs, coverage reports, or `node_modules`.

## Starter Expectations By Phase

### U01-U04

Create:

- Course state files.
- Project shell or unit lab.
- `package.json` scripts.
- TypeScript config if needed.
- Minimal UI/API stubs.
- Basic check or test.

Leave TODOs for core logic and explanation prompts.

### U05-U08

Create:

- Provider adapter stub.
- `.env.example`.
- AI route stub.
- UI states for loading, error, empty, streaming, cancel, and retry as needed.
- Prompt/eval templates.
- Structured output schema stubs.

Leave TODOs for provider call, stream handling, schema decisions, and error paths.

### U09-U12

Create:

- Database schema starter.
- Migration/seed command notes.
- Repository/service boundaries.
- Auth route or integration placeholders.
- Tenant-scope test cases.

Leave TODOs for queries, policies, and negative tests.

### U13-U17

Create:

- Tool schema stubs.
- Tool trace display or logs.
- Approval-flow TODOs.
- Document corpus samples.
- Retrieval/eval templates.
- File privacy checklist when needed.

Leave TODOs for tool execution, permission checks, retrieval, citations, and refusal behavior.

### U18-U24

Create:

- Red-team checklist.
- Cost/latency logging TODOs.
- Health/metrics stubs.
- Docker/CI templates only when the project shape is known.
- Deployment notes template.
- Portfolio README sections.

Leave TODOs for real verification, tradeoff notes, and final defense.
