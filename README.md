# AI-Driven Multi-Agent Negotiation Training & Simulation Platform

An intelligent, multi-agent negotiation platform powered by Generative AI. Built with **React**, **FastAPI**, **MongoDB**, and custom agent orchestration engines, this platform operates in two distinct modes:

1. **Simulation Mode**: User observes two autonomous LLM-powered agents negotiate with each other.
2. **Practice Mode**: User participates directly as one of the negotiating parties against intelligent AI agents.

---

## 🌟 Key Features

- **3 Pre-Built Scenario Templates**:
  1. *Vendor Pricing Negotiation*: Price, quantity, warranty, and payment terms.
  2. *Job Offer Negotiation*: Base salary, signing bonus, remote days, and equity.
  3. *Project Budget Allocation*: Department funding, contingency reserves, and phase 1 release milestones.
- **Orchestrator Engine**: Manages turn-taking loops, state transitions, context isolation, deadlock detection, and max round timeouts.
- **Strict Context Isolation**: Guarantees zero leakage of private goals, constraints, or long-term memory between agents.
- **Tool Calling Layer**: 6 schema-defined tools (Price Calculator, Policy Retriever, Currency Converter, Product DB, Budget Validator, Market Price Search).
- **RAG Knowledge Retrieval & Grounding**: Vector search over scenario policy benchmarks with automated grounding score calculation.
- **Negotiation Arena UI**: Live transcript, stance badges (`ACCEPT`, `COUNTER`, `HOLD`, `CONCEDE`), confidence meters, RAG citations, and Estimated ZOPA progress bar.
- **Structured Outcome Report**: Performance scorecards, final agreed terms, narrative summary, and export options.

---

## 🏗️ Tech Stack

- **Frontend**: React (Vite), Lucide Icons, Modern Vanilla CSS (Glassmorphism design system)
- **Backend**: FastAPI (Python 3.12), Pydantic v2, Uvicorn
- **Database**: MongoDB (via Motor async client with automatic in-memory fallback)
- **Vector DB / RAG**: Dedicated in-memory vector retriever with TF-IDF similarity
- **LLM Layer**: Agnostic interface supporting Gemini API (`google-generativeai`), OpenAI API, and Custom Reasoning Engine fallback.
