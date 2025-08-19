# BlinkWell Diagnostic – SLO & COGS Analysis

This document describes the Service Level Objectives (SLOs) and Cost of Goods Sold (COGS) targets for the BlinkWell triage engine.

## Service Level Objectives

- **p95 latency:** \u2264 1.0 s for triage response (targeting sub-second user experience).
- **Maximum inference cost per session:** \u2264\u00a0$0.10 to ensure sustainable gross margins.
- **Availability:** \u2265 99.9% uptime with automated retries and graceful degradation.
- **Data privacy:** All PHI must remain encrypted at rest and in transit; no raw PHI leaves the compliant environment.

## Cost of Goods Sold

- **Model inference cost:** Estimated at $0.08 per triage session using GPT‑5 Pro, leaving headroom for other platform costs.
- **Infrastructure cost:** Additional $0.02 per session covers compute, storage, and networking (serverless functions, database writes, etc.).
- **Gross margin target:** \u2265 60% after three months, assuming price per consult of $0.25 and volume scaling to at least 1,000 sessions.

## Notes

These targets are used as hard gates in the evaluation pipeline. Candidates breaching latency or cost budgets will not be promoted. Continuous monitoring is required to ensure SLO adherence as usage scales.
