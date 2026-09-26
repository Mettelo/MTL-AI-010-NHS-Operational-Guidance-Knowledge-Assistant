# Required Deliverables

## D1 — Problem & scope
Define:
- user;
- supported use cases;
- excluded use cases;
- approved knowledge scope;
- success criteria.

Output:
`docs/01-problem-and-scope/`

## D2 — Knowledge base manifest
Provide a documented list of approved NHS sources including:
- title;
- URL;
- retrieval date;
- type;
- inclusion rationale.

Output:
`docs/02-knowledge-base/` and `data/metadata/`

## D3 — Document ingestion pipeline
Build reproducible ingestion for:
- HTML;
- PDF where used;
- text cleanup;
- metadata preservation;
- error handling.

Output:
`src/ingestion/`

## D4 — Chunking experiment
Compare at least two sensible chunking strategies/settings.

Document:
- size;
- overlap;
- section awareness;
- effect on retrieval.

Output:
`src/chunking/` and `docs/03-ingestion-and-chunking/`

## D5 — Embedding & index layer
Implement a free/local embedding pipeline and vector index.

Output:
`src/embeddings/` and `indexes/`

## D6 — Retrieval system
Implement and evaluate retrieval.

At minimum:
- vector search;
- top-k configuration;
- metadata returned;
- retrieval evaluation.

Optional:
- BM25;
- hybrid retrieval;
- reranking.

Output:
`src/retrieval/` and `docs/04-retrieval/`

## D7 — Grounded generation
Implement:
- local LLM generation;
- evidence-only prompt;
- citation generation;
- insufficient-evidence refusal.

Output:
`src/generation/` and `docs/05-generation-and-citations/`

## D8 — Evaluation dataset
Create a curated evaluation set containing:
- answerable questions;
- partially answerable questions;
- unanswerable questions;
- adversarial/misleading questions.

Output:
`data/evaluation/`

## D9 — Evaluation framework
Measure at least:
- retrieval relevance/Recall@k or equivalent;
- answer correctness;
- groundedness;
- citation correctness;
- refusal quality.

Output:
`src/evaluation/`, `docs/06-evaluation/`, `outputs/evaluations/`

## D10 — Safety & adversarial tests
Test:
- prompt injection;
- unsupported knowledge requests;
- instruction override attempts;
- citation-bypass requests;
- malicious instructions embedded in retrieved content where safely simulated.

Output:
`src/safety/` and `docs/07-safety-and-adversarial-testing/`

## D11 — Lightweight interface
Provide either:
- CLI;
- Streamlit;
- Gradio;
- equivalent free local interface.

It must expose answer + citations.

Output:
`app/`

## D12 — Technical handover
Document:
- prerequisites;
- local model installation;
- building the knowledge base;
- generating embeddings/index;
- running the assistant;
- running evaluations;
- updating sources;
- troubleshooting;
- known limitations.

Output:
`docs/08-technical-handover/`

## D13 — Collaboration & submission
Complete:
- `CONTRIBUTIONS.md`;
- GitHub evidence;
- `submission/FINAL_SUBMISSION.md`;
- final tag.
