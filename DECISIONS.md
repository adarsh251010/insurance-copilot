# Architecture Decision Records

Significant technical decisions for Insurance Copilot, with the context and trade-offs behind each.

---

## ADR-001: Python as the primary language

- **Date:** 2026-10-07
- **Status:** Accepted

**Context**
The core of this project is LLM orchestration, retrieval, and evaluation. The most mature tooling for this work (LangGraph, Ragas, Langfuse, and the official LLM SDKs) is Python-first.

**Decision**
Build the backend in Python with FastAPI and Pydantic.

**Consequences**
- Direct access to the AI ecosystem without wrappers or ports.
- FastAPI's async support suits I/O-heavy LLM calls.
- Trade-off: Python's raw runtime performance is lower than JVM languages. This is acceptable because end-to-end latency is dominated by LLM and database calls.