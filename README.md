# Vehicle Recall Assistant (agent-eval-lab)

An AI agent that answers vehicle recall questions from **public NHTSA recall data**, built to
practise **testing and evaluating AI systems**: RAG quality, tool calling, hallucinations and
prompt injection.

> 🚧 Work in progress. Started Nov 2026.

## Why this project
Most AI demos stop at "it answers." This one focuses on **how to prove it answers correctly**:
- Exact questions (counts, lookups) go to deterministic, unit-tested code (pandas), never the LLM
- Open questions go to vector search (RAG) with every answer citing an NHTSA campaign number
- A golden dataset and automated evals measure quality and catch regressions

## Stack
Python · LangChain / LangGraph · Chroma · Ollama or OpenAI · Streamlit · Pytest · GitHub Actions

## Roadmap
- [ ] Week 1: data pipeline, RAG, agent with 2 tools, Streamlit UI, unit tests
- [ ] Week 2: golden dataset + RAGAS evaluation
- [ ] Week 3: tool-call correctness and LLM-as-judge tests
- [ ] Week 4: prompt-injection and hallucination tests, model comparison
- [ ] Month 2: evals as a CI quality gate, Docker

## Data
[NHTSA Recalls API](https://www.nhtsa.gov/nhtsa-datasets-and-apis) (public, no key needed).
This project is for learning and is not legal or repair advice.