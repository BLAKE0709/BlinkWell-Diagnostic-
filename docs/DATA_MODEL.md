# BlinkWell Diagnostic – Data Model

This document outlines the core entities used in the BlinkWell triage platform.

## Entities

### User
- **id** (UUID): Unique identifier for the user.
- **name** (string): Full name of the user.
- **date_of_birth** (date): Date of birth.
- **consent_given** (boolean): Whether the user has provided HIPAA-compliant consent.
- **demographics** (object): Additional demographic details (e.g., gender, age bracket).

### TriageSession
- **session_id** (UUID): Unique identifier for a triage session.
- **user_id** (UUID): Identifier of the user who initiated the session.
- **symptoms** (array of strings): Symptoms provided by the user.
- **triage_time** (datetime): Timestamp when the triage occurred.
- **recommendation** (string): Recommendation outcome (e.g., `self_care`, `virtual_consult`, `in_person`).
- **urgency_level** (string): Urgency category.

### Recommendation
- **id** (UUID): Unique identifier for the recommendation entry.
- **session_id** (UUID): Triage session identifier.
- **type** (string): Type of recommendation (e.g., treatment, follow_up, escalation).
- **details** (string): Additional information or instructions.
