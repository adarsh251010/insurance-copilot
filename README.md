# Insurance Copilot

An AI assistant that explains insurance policies in plain English and Hindi, with answers grounded in the policy document and cited down to the page.

> **Status:** Work in progress. Features are being built in phases; see the roadmap below.

## The problem

Insurance policies are long and dense. Most policyholders don't know what is covered, what the waiting periods are, or how to file a claim until they need to. Insurance Copilot turns a policy PDF into clear, verifiable answers.

## Roadmap

- [ ] **Policy summary**: extracts key terms (sum insured, waiting periods, room rent limit, co-pay, sub-limits, exclusions) into a structured format
- [ ] **Q&A with citations**: answers questions from the policy with page-level references
- [ ] **Policy comparison**: compares 2–3 policies side by side
- [ ] **Claim assistant**: an agent that lists required documents, checks coverage, and drafts next steps with human approval
- [ ] **Evaluation suite**: a benchmark of policy questions with published accuracy metrics
- [ ] **Hindi + English**: answers in the user's language
- [ ] **Production safeguards**: tracing, cost tracking, PII masking, prompt-injection defense

## Tech stack

| Layer | Tools |
| --- | --- |
| Backend | Python, FastAPI, Pydantic |
| Data | PostgreSQL + pgvector, SQLAlchemy, Alembic, Redis |
| AI | LLM APIs (Claude / OpenAI), LangGraph, MCP |
| Quality | pytest, Ragas, Langfuse |
| Frontend | React, Tailwind CSS |
| Infra | Docker |

## Getting started

Requires Python 3.11+.

```bash
git clone https://github.com/adarsh251010/insurance-copilot.git
cd insurance-copilot
python -m venv .venv
# Windows: