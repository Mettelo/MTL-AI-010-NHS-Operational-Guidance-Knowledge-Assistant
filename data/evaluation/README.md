# Evaluation Dataset

Create a curated question set.

Required categories:
- answerable;
- partially answerable;
- unanswerable;
- misleading/adversarial.

Recommended fields:
- question_id
- question
- category
- expected_source_ids
- reference_answer or key evidence
- should_answer
- notes

Do not generate the entire evaluation set automatically from the same model being evaluated without human review.
