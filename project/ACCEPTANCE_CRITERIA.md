# Acceptance Criteria

## Scope
- Supported use cases are clearly defined.
- Clinical/patient-specific advice is explicitly out of scope.
- Approved NHS knowledge sources are documented.

## Cost & reproducibility
- Core project can be completed at £0.
- Paid APIs are not required.
- Local/open models and embeddings are documented.
- A reviewer can reproduce the index and application.

## Knowledge base
- Every indexed source has metadata.
- Source URLs and retrieval dates are recorded.
- Undocumented sources are not silently included.

## Ingestion
- HTML/PDF/text sources used are parsed reproducibly.
- Empty/malformed inputs are surfaced.
- Section/document metadata is preserved.

## Chunking
- At least two chunking approaches/settings are evaluated.
- Final choice is evidence-based.

## Retrieval
- Retrieval system works reproducibly.
- Retrieved passages include source metadata.
- Retrieval quality is quantitatively evaluated.

## Generation
- Answers are grounded in retrieved context.
- Citation output exists.
- Generation prompt restricts unsupported claims.

## Refusal behaviour
- Unsupported questions are tested.
- System can return insufficient-evidence responses.
- It does not simply answer every question.

## Citation quality
- Citation correctness is evaluated.
- Sources actually support the generated claims.

## Evaluation
- Curated evaluation set exists.
- Answerable and unanswerable questions are represented.
- Correctness, groundedness and refusal quality are reported.

## Safety
- Prompt-injection tests exist.
- Instruction-override tests exist.
- Known vulnerabilities are documented.
- Model is not presented as clinical decision support.

## Engineering quality
- Core logic exists outside notebooks.
- Code is modular.
- Dependencies reproducible.
- Logging/error handling included.
- Model weights/secrets are not improperly committed.

## Interface
- User can submit a question.
- Answer is shown.
- Citations are shown.
- Failure/refusal state is understandable.

## Documentation
- Setup is complete.
- Model/embedding choices documented.
- Knowledge refresh documented.
- Evaluation documented.
- Limitations documented.

## Collaboration
- Contributions transparent.
- Git history demonstrates meaningful participation.
- PR workflow used where practical.

## Submission
- Final submission complete.
- Reviewer has access.
- QA complete.
- Final tag `v1.0-mettelo-submission` created.
