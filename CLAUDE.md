# CLAUDE.md

Project context for AI coding assistants.

## Project
Insurance Copilot: an AI assistant that explains insurance policies, answers questions with page-level citations, and assists with claims.

## Stack
Python 3.11+, FastAPI, Pydantic, SQLAlchemy + Alembic, PostgreSQL + pgvector, Redis, LangGraph, pytest.

## Conventions
- Type hints on all functions; Pydantic models for request and response schemas.
- pytest tests for every new module.
- Record significant design decisions in DECISIONS.md (ADR format).
- Secrets go in .env, never in code.