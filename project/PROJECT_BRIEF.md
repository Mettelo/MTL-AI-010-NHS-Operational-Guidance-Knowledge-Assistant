# Project Brief

## 1. Business context
Operational and statistical guidance is often spread across multiple web pages and documents. Analysts may spend significant time locating definitions, methodology notes and reporting rules.

A well-designed RAG assistant can reduce search effort while preserving source traceability.

## 2. Problem statement
Build a local-first AI knowledge assistant that answers operational/statistical questions using only an approved NHS England knowledge base and provides source-backed citations.

The system must demonstrate retrieval quality, grounded generation, refusal behaviour and robust evaluation.

## 3. Primary users
Assume the system supports:
- NHS analysts;
- operational reporting teams;
- performance teams;
- data professionals;
- policy/statistics users.

## 4. Knowledge scope
The core knowledge base should include a bounded set of public NHS England material such as:
- RTT statistics user guidance;
- RTT definitions;
- RTT recording/reporting guidance;
- RTT rules and supporting documents;
- relevant methodology notes;
- selected publication notes/FAQs.

Every included source must be documented.

## 5. Source acquisition
Teams must:
- record source URL;
- record source title;
- record retrieval date;
- record file/page type;
- preserve original document where practical;
- maintain a source manifest;
- avoid silently mixing undocumented sources into the index.

## 6. Parsing & cleaning
The ingestion pipeline must:
- extract useful text;
- remove obvious navigation/noise where appropriate;
- preserve headings/section context;
- retain page/document metadata;
- handle malformed or empty documents visibly.

## 7. Chunking
Chunking strategy must be documented and tested.

Teams should compare at least two reasonable strategies or parameters, for example:
- fixed token/character chunks;
- heading-aware chunks;
- recursive splitting;
- overlap/no-overlap variants.

Do not assume smaller chunks are automatically better.

## 8. Embeddings
Use a free/local embedding model.

Document:
- model name;
- dimensionality where relevant;
- reason for selection;
- runtime/hardware requirements.

## 9. Retrieval
Implement vector retrieval and evaluate it.

Optional:
- BM25;
- hybrid retrieval;
- reranking.

At minimum report a retrieval metric such as:
- Recall@k;
- Hit Rate@k;
- MRR;
- nDCG where justified.

## 10. Generation
Use a local/open-source LLM for the core implementation.

The generation prompt must:
- restrict answers to retrieved evidence;
- request concise source-grounded answers;
- require citation/reference output;
- instruct refusal when evidence is insufficient.

## 11. Citations
Every substantive answer must expose the source used.

Citation format may include:
- document title;
- URL;
- section heading;
- page number where available;
- chunk/source identifier.

The team must evaluate citation correctness, not merely display links.

## 12. Unsupported questions
The system must detect or handle cases where retrieval does not support a reliable answer.

Refusal behaviour should be explicit and consistent.

## 13. Hallucination testing
Create an evaluation set containing:
- answerable questions;
- partially answerable questions;
- unanswerable questions;
- misleading questions.

Measure whether the system invents unsupported facts.

## 14. Prompt injection / adversarial testing
Test attacks such as:
- instructions embedded in source documents;
- user attempts to override system rules;
- requests to ignore citations;
- requests to answer beyond the approved knowledge base.

Document observed failures and mitigations.

## 15. Evaluation
The project must include a manually curated evaluation dataset.

Minimum evaluation dimensions:
- retrieval relevance;
- answer correctness;
- groundedness;
- citation correctness;
- refusal quality.

Optional:
- latency;
- token/runtime efficiency;
- model comparison.

## 16. Interface
A lightweight UI is recommended but not the core project.

Possible:
- Streamlit;
- Gradio;
- command-line interface.

The UI should show:
- user question;
- answer;
- citations;
- retrieved evidence where useful.

## 17. Monitoring
Explain how a real implementation would monitor:
- source freshness;
- ingestion failures;
- retrieval quality;
- unanswered-question rate;
- hallucination rate;
- model/runtime changes.

## 18. Out of scope
The core project does **not** require:
- paid LLM APIs;
- clinical decision support;
- patient data;
- medical diagnosis;
- full NHS website crawling;
- fine-tuning a foundation model;
- production cloud hosting.

## 19. Success definition
A reviewer should be able to clone the repository, build the documented NHS knowledge base, create the index, run the assistant, execute the evaluation suite and reproduce the reported results without paid services or undocumented manual steps.
