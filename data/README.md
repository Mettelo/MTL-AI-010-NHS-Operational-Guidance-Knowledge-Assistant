# Knowledge Base Sources

## Official NHS England sources

### NHS England Statistics
https://www.england.nhs.uk/statistics/

### Referral to Treatment Waiting Times
https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/

### RTT Statistics User Guidance
https://www.england.nhs.uk/statistics/statistical-work-areas/rtt-waiting-times/rtt-statistics-user-guidance/

## Recommended core knowledge collection
Build a bounded knowledge base containing selected material such as:
- RTT definitions;
- RTT statistics user guidance;
- RTT rules/guidance;
- recording/reporting guidance;
- methodology notes;
- selected publication notes;
- selected relevant FAQs.

Do not crawl the entire NHS website.

## Source manifest
Every source should be recorded in a manifest with fields such as:

- source_id
- title
- URL
- source_type
- retrieved_at
- publication/update date where available
- included_sections
- checksum/version where practical
- status

## Raw source principle
Preserve original downloaded HTML/PDF/text where practical.

Do not manually rewrite source content and then treat it as authoritative source data.

## Knowledge-boundary rule
The assistant should answer from the approved indexed sources.

General model knowledge must not silently fill gaps.

## Clinical boundary
The knowledge base and assistant are for operational/statistical guidance.

Do not extend the system into clinical diagnosis, treatment or patient-specific medical advice.
