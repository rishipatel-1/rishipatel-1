# Hi, I'm Rishi

Software engineer who builds agentic AI systems and ships them to production. I like working on problems where LLMs meet real infrastructure — orchestration, retrieval, evaluation, security, and making things actually reliable at scale.

## What I'm building

### AgentLens
A platform where AI agents answer questions over your documents using retrieval — and every step they take is traced, evaluated, and searchable. Not a wrapper around an API. The whole pipeline from scratch:
- RAG with chunking, embeddings, pgvector search, and recall@k scoring to measure if retrieval is actually good
- Agent layer with tool calling, multi-step reasoning, and grounded citations
- LLM-as-judge evaluation — the system scores its own outputs so I know if a change made things better or worse
- Failure intelligence — past agent failures get embedded and become searchable (RAG on ops data)
- Distributed job queue on Postgres SKIP LOCKED with retries and DLQ
- 49 tests. TDD throughout. Built to be explainable end-to-end.

`Python` `FastAPI` `pgvector` `PostgreSQL` `Google Gemini` `Next.js` `Docker`

### Production MCP Starter
Infrastructure that lets AI agents securely call external tools at scale. The kind of plumbing most people skip:
- Streamable HTTP transport (JSON-RPC + SSE) — agents get streaming responses
- OAuth 2.1 + PKCE with Redis-backed single-use state
- AES-256-GCM token vault — encrypted at rest, per-record IV, tamper detection tests
- Per-user rate limiting, idempotency cache, circuit breakers
- Hexagonal architecture enforced by linter — domain never touches infra
- Multi-stage Docker, Cloudflare Workers as edge runtime

`TypeScript` `Hono` `PostgreSQL` `Redis` `Docker` `Cloudflare Workers`

## Stack

Python, TypeScript, FastAPI, Node.js, NestJS, React, Next.js, PostgreSQL, pgvector, Redis, LangGraph, LangChain, AWS (Lambda, SQS, Kafka, DynamoDB), Docker

## Beyond what's public

Most of my production work lives in private repos — multi-agent orchestration systems, event-driven backends on AWS, real-time streaming applications, and full-stack products with React/Next.js + NestJS. The green squares are real.

![Contribution Activity](./assets/contributions.png)

## Links

- Email: patelris2001@gmail.com
