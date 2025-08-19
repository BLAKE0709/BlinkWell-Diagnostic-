# BlinkWell Diagnostic – Product Requirements Document (PRD)

## Purpose

Design and launch an ocular triage service (code‑name **BlinkWell**) that quickly evaluates eye‑related symptoms and directs users to the appropriate level of care: self‑care, virtual consultation, or in‑person appointment.

## Features

- **Symptom intake** with clarifying questions.
- **Real‑time triage** using OpenAI’s Responses API and multi‑agent workflows.
- **Recommendation engine** suggesting next steps (self‑care guidance, virtual consult, urgent referral).
- **EMR & scheduling integration** via FHIR/HL7 for seamless referrals and follow‑ups.
- **Secure onboarding** with HIPAA‑compliant consent flows (web, mobile, kiosk).

## Success Metrics

- **Time‑to‑first‑revenue (TTR)**: achieve paying users within 60 days of project inception.
- **p95 latency** for triage response ≤ 1 second.
- **Conversion**: ≥ 70% of sessions convert to a scheduled consultation.
- **Gross margin**: ≥ 60% per session after three months.

## Compliance & Constraints

- **Regulatory**: full HIPAA and FTC adherence; triage decisions must follow evidence‑based optometric practice.
- **Budget**: $50 k total development spend; runtime cost ≤ $5 per triage session for the first 1,000 sessions.
- **Non‑negotiables**: no unverified treatments or misleading marketing; PHI must remain encrypted; any latency or cost budget breach is a hard veto.

