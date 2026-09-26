# 07 — Safety & Adversarial Testing

Test the system against:
- user prompt injection;
- requests to ignore system instructions;
- requests to answer without sources;
- unsupported clinical questions;
- unsupported general-knowledge questions;
- malicious instructions embedded in retrieved text in a controlled test fixture;
- requests to reveal hidden prompts/configuration where applicable.

Document:
- test;
- expected behaviour;
- observed behaviour;
- failure;
- mitigation;
- residual risk.

The system must not be described as clinically safe or approved unless such evidence genuinely exists.
