# Suryakant Verma

**Principal Software Architect · 20+ years · 9+ in AI**

I build secure, production-grade AI platforms — RAG, agentic workflows, MCP — and the identity, isolation, observability, and evaluation that make them safe to run in an enterprise. Previously at OpenText and Siemens. Based in Bengaluru.

Secure by design is not a tagline here: every repo below ships with OIDC or token-exchange auth, environment-driven config with no committed secrets, and tests that run without network.

## Selected work

| Repo | What it is | Why it matters |
|---|---|---|
| [**corpus-rag**](https://github.com/suryakantverma2013/corpus-rag) | Enterprise RAG chatbot. FastAPI + LangGraph, PostgreSQL/pgvector hybrid (dense + BM25) retrieval, cross-encoder reranking, Keycloak OIDC, MinIO, arq ingestion workers, DeepEval scoring, React 19 UI. | A chat turn is a checkpointed state machine — *screen → route → retrieve → rerank → generate → gate → finalize* — and nothing reaches the user until the groundedness gate passes. Every claim carries a citation that resolves to its passage. |
| [**mcp-mastery**](https://github.com/suryakantverma2013/mcp-mastery) | Eight-phase, production-grade MCP curriculum in Python, targeting the 2026-07-28 spec. Each phase is runnable in isolation with its own `THEORY.md`. | Goes from primitives to a hardened multi-tenant gateway: OAuth 2.1, RFC 8693 token exchange via Keycloak, per-tenant routing, rate limiting, audit trail, and a measured Code Mode demonstration. 118 tests, 5 gated live. |
| [**graphrag-pipeline**](https://github.com/suryakantverma2013/graphrag-pipeline) | Graph RAG over technical documentation. LangGraph + Neo4j (graph + vector + full-text), Docling parsing, local GPU reranking (BGE), PostgreSQL checkpointing. | Not an embed-and-cosine demo: content-type-aware chunking, calibrated confidence scores, benchmarked retrieval variants, and resumable human-in-the-loop review via LangGraph `interrupt()`. |
| [**RAGWithGroundednessSupport**](https://github.com/suryakantverma2013/RAGWithGroundednessSupport) | Haystack + Milvus hybrid RAG with a three-tier answer path and Langfuse tracing. | The semantic answer cache is kept in a physically separate collection from the documents, so a cached LLM answer can never be retrieved and cited as source material. |

## How I work

- **Architecture first.** Each repo has an `ARCHITECTURE.md` or `THEORY.md` that explains the decisions, not just the setup.
- **Security as a constraint, not a feature.** Auth, tenancy, and secrets handling are designed in from the first commit.
- **Measured, not asserted.** Evaluation harnesses, benchmarks, and confidence calibration are part of the deliverable.

## Elsewhere

- [LinkedIn](https://www.linkedin.com/in/suryakant-verma-ba573537/) — I write weekly on production RAG and agentic AI.
- Co-founder, [Jivatu Technologies](https://jivatu.tech) — AI, cybersecurity, and digital trust.
