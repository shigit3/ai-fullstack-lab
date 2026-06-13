# Current Source Checklist

Use this file when the learner asks for current APIs, latest model/provider behavior, pricing, SDK usage, deployment guidance, or framework recommendations.

Last designed: 2026-06-13.

## Verify Before Teaching Implementation Details

Check official or primary sources for:

- Node.js LTS/current status and release schedule.
- Nuxt/Vue framework APIs.
- Express 5 behavior.
- Prisma setup and migrations.
- Vercel AI SDK APIs, especially streaming and Nuxt support.
- OpenAI, DeepSeek, Anthropic, or other provider API behavior.
- Model names, pricing, rate limits, deprecations, and structured output/tool calling support.
- Model Context Protocol APIs.
- LangChain/LangGraph JavaScript APIs if an optional pack uses them.
- Deployment platform details.

## Primary Sources

- Node.js releases: https://nodejs.org/en/about/previous-releases
- Node.js docs: https://nodejs.org/docs/latest/api/
- TypeScript docs: https://www.typescriptlang.org/docs/
- Nuxt docs: https://nuxt.com/docs
- Vue docs: https://vuejs.org/guide/introduction.html
- Express docs: https://expressjs.com/
- PostgreSQL docs: https://www.postgresql.org/docs/
- Prisma docs: https://www.prisma.io/docs
- Zod docs: https://zod.dev/
- Vercel AI SDK docs: https://ai-sdk.dev/docs
- Vercel AI SDK Nuxt guide: https://ai-sdk.dev/docs/getting-started/nuxt
- OpenAI platform docs: https://platform.openai.com/docs
- DeepSeek API docs: https://api-docs.deepseek.com/
- Model Context Protocol docs: https://modelcontextprotocol.io/docs
- LangChain JavaScript docs: https://docs.langchain.com/oss/javascript/langchain/overview
- LangGraph JavaScript docs: https://docs.langchain.com/oss/javascript/langgraph/overview
- OWASP API Security: https://owasp.org/www-project-api-security/
- OpenTelemetry JavaScript docs: https://opentelemetry.io/docs/languages/js/
- Docker Node.js guide: https://docs.docker.com/guides/nodejs/
- GitHub Actions docs: https://docs.github.com/actions
- roadmap.sh full stack roadmap: https://roadmap.sh/full-stack
- roadmap.sh backend roadmap: https://roadmap.sh/backend
- roadmap.sh AI engineer roadmap: https://roadmap.sh/ai-engineer
- Full Stack Open: https://fullstackopen.com/en/
- The Odin Project: https://www.theodinproject.com/

## Stable Direction

- Prefer LTS runtime choices for required units.
- Prefer TypeScript-first implementation.
- Prefer server-owned AI provider calls.
- Prefer provider-adapter boundaries so provider changes do not rewrite the product.
- Prefer structured outputs for UI/business logic.
- Prefer tool execution on the server with explicit permissions.
- Prefer RAG with citations and refusal behavior for private or changing knowledge.
- Prefer evals before major prompt, retrieval, or model changes.
- Prefer simple explicit workflows before agent frameworks.
- Prefer Vue/Nuxt for this learner unless an existing project requires React/Next.js.

## Update Procedure

When updating the course:

1. Verify current facts against official docs.
2. Update only the units affected by real ecosystem changes.
3. Keep the course spine stable unless the learning path is materially improved.
4. Record the new review date here.
