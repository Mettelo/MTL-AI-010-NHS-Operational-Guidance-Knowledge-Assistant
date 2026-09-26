# MTL-AI-010 — NHS Operational Guidance Knowledge Assistant

## Project title
**NHS Operational Guidance Knowledge Assistant — Retrieval-Augmented Generation with Evidence, Citations & Evaluation**

## Project type
AI / LLM Engineering · Team project · Production-style portfolio project

## Challenge
NHS operational and statistical guidance is distributed across multiple public pages, guidance documents, methodology notes and supporting publications.

Analysts and operational users need a reliable way to ask questions and receive concise answers grounded in approved NHS source material.

Your team will build a Retrieval-Augmented Generation (RAG) assistant that retrieves relevant NHS guidance, generates evidence-grounded answers, cites its sources and refuses to answer when the approved knowledge base does not contain enough evidence.

This is **not** a generic chatbot project.

## Core use case
Examples of supported questions:

- What does an incomplete RTT pathway mean?
- How should RTT waiting-time bands be interpreted?
- What is the difference between admitted and non-admitted pathways?
- Which guidance defines a particular RTT reporting rule?
- What caveats should analysts understand when interpreting published RTT data?

The assistant must answer from the approved knowledge base rather than relying on unsupported model memory.

## Official source material

NHS England Statistics:

https://www.england.nhs.uk/statistics/

Referral to Treatment Waiting Times:

https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/

RTT Statistics User Guidance:

https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/rtt-statistics-user-guidance/

Teams should use a bounded, documented collection of approved public NHS England guidance rather than attempting to crawl the entire NHS website.

## Scope restriction
This project is for:
- operational guidance;
- statistical definitions;
- reporting methodology;
- data interpretation;
- publication notes;
- analytical support.

It must **not** provide:
- clinical diagnosis;
- treatment advice;
- patient-specific medical guidance;
- emergency advice;
- medication recommendations.

## Cost requirement
**The complete core project must be achievable at £0.**

Paid APIs must not be required.

Recommended free/local-first stack:

- Python
- Ollama or another local model runner
- a small open-source instruction model
- Sentence Transformers
- FAISS or Chroma
- optional BM25 / hybrid retrieval
- Streamlit or Gradio for a lightweight interface
- Git
- GitHub

Paid OpenAI, Anthropic, Gemini or commercial vector database APIs may be used only as optional extensions, never as a core dependency.

## Core objective
Build a reproducible RAG system that:

1. acquires and versions an approved NHS knowledge base;
2. parses HTML/PDF/text sources;
3. cleans and chunks content;
4. preserves document metadata;
5. creates embeddings locally;
6. indexes chunks in a free/local vector store;
7. retrieves relevant evidence;
8. optionally reranks retrieved passages;
9. generates grounded answers;
10. returns citations/source references;
11. refuses unsupported questions;
12. evaluates retrieval quality;
13. evaluates groundedness and citation accuracy;
14. tests hallucination behaviour;
15. tests prompt-injection resistance;
16. logs evaluation results;
17. documents limitations and monitoring.

## Required AI workflow

```
Approved NHS sources
        ↓
Document ingestion
        ↓
Cleaning + metadata
        ↓
Chunking
        ↓
Embeddings
        ↓
Vector / hybrid index
        ↓
Retrieval
        ↓
Optional reranking
        ↓
Grounded prompt
        ↓
Local LLM answer
        ↓
Citations + refusal logic
        ↓
Evaluation + safety testing
```

## Minimum system behaviour

For supported questions, the assistant should return:

**Answer → Evidence → Source / citation**

If the knowledge base does not contain sufficient evidence, the assistant should respond with an explicit insufficient-evidence response rather than inventing an answer.

Example:

> I could not find sufficient evidence in the approved knowledge base to answer this reliably.

## Evaluation rule
Success is **not** “the chatbot gives fluent answers.”

The project must demonstrate:

- retrieval quality;
- groundedness;
- citation correctness;
- refusal quality;
- hallucination control;
- prompt-injection handling;
- reproducibility.

## Team submission model
Each team creates **its own GitHub repository**.

Recommended naming:

`MTL-AI-010-<team-name>`

The Mettelo repository is the challenge specification.

Each team must:
1. create its own repository;
2. invite the designated Mettelo reviewer/collaborator;
3. follow `project/REPOSITORY_STRUCTURE.md`;
4. use issues/branches/commits/pull requests as evidence of collaboration;
5. complete `submission/FINAL_SUBMISSION.md`;
6. complete final QA;
7. tag the accepted version `v1.0-mettelo-submission`;
8. submit the repository URL.

## Project documents
- [Project brief](project/PROJECT_BRIEF.md)
- [Knowledge base guidance](data/README.md)
- [Mandatory repository structure](project/REPOSITORY_STRUCTURE.md)
- [Deliverables](project/DELIVERABLES.md)
- [Acceptance criteria](project/ACCEPTANCE_CRITERIA.md)
- [Team roles](project/TEAM_ROLES.md)
- [Contribution rules](CONTRIBUTIONS.md)
- [Final submission template](submission/FINAL_SUBMISSION.md)

---
**Mettelo — Built for What’s Next**
