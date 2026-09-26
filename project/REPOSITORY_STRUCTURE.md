# Mandatory Team Repository Structure

Each team must create a separate repository named:

`MTL-AI-010-<team-name>`

Minimum structure:

```
MTL-AI-010-<team-name>/
│
├── README.md
├── CONTRIBUTIONS.md
├── requirements.txt
├── .gitignore
├── .env.example
│
├── config/
│   └── README.md
│
├── data/
│   ├── raw/
│   │   └── README.md
│   ├── processed/
│   │   └── README.md
│   ├── evaluation/
│   │   └── README.md
│   └── metadata/
│       └── README.md
│
├── docs/
│   ├── 01-problem-and-scope/
│   │   └── README.md
│   ├── 02-knowledge-base/
│   │   └── README.md
│   ├── 03-ingestion-and-chunking/
│   │   └── README.md
│   ├── 04-retrieval/
│   │   └── README.md
│   ├── 05-generation-and-citations/
│   │   └── README.md
│   ├── 06-evaluation/
│   │   └── README.md
│   ├── 07-safety-and-adversarial-testing/
│   │   └── README.md
│   └── 08-technical-handover/
│       └── README.md
│
├── src/
│   ├── ingestion/
│   ├── chunking/
│   ├── embeddings/
│   ├── retrieval/
│   ├── generation/
│   ├── evaluation/
│   ├── safety/
│   └── utils/
│
├── app/
│   └── README.md
│
├── tests/
├── notebooks/
├── indexes/
├── outputs/
│   ├── evaluations/
│   └── examples/
│
└── submission/
    └── FINAL_SUBMISSION.md
```

## Repository rules

### Source documents
Do not commit very large or unnecessary copied documents.

Maintain a reproducible source manifest and download/ingestion workflow.

### Secrets
Paid APIs are not required.

If optional credentials are used, never commit them.

### Local models
Do not commit multi-GB model weights to the repository.

Document how to install/pull the selected local model.

### Indexes
Large vector indexes should not be committed unless small enough and useful.

The build process must be reproducible.

### Notebook rule
Notebooks may support exploration/evaluation but core RAG logic must live in reusable modules under `src/`.

### Collaboration
Use:
- issues;
- branches;
- meaningful commits;
- pull requests;
- peer review.

## Final version
After QA and Mettelo review:

`v1.0-mettelo-submission`
