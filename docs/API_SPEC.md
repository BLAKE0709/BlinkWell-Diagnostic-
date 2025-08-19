# BlinkWell Diagnostic – API Specification

This document describes the endpoints for the BlinkWell ocular triage engine.

## POST /triage
Submits a symptom description and optional images for triage.

**Request body (JSON):**

- `user_id` (string): Unique user identifier.
- `symptoms` (array of strings): List of symptom descriptions.
- `attachments` (array of file objects, optional): Uploaded images (e.g. eye photos).

**Response (JSON):**

- `triage_recommendation`: A recommendation such as `self_care`, `virtual_consult`, or `in_person`.
- `urgency_level`: The urgency category (e.g., low, medium, high).
- `follow_up_actions`: Next steps for the user (e.g., schedule appointment, home care instructions).

## POST /schedule
Schedules a consultation with a provider.

**Request body (JSON):**

- `user_id`: Unique user identifier.
- `preferred_time`: Preferred consultation time (ISO 8601 string).
- `provider_type`: Type of provider (e.g., optometrist, ophthalmologist).

**Response (JSON):**

- `confirmation_id`: Unique identifier for the appointment.
- `scheduled_time`: Final scheduled time.

## POST /feedback
Collects user satisfaction and outcomes.

**Request body (JSON):**

- `session_id`: Identifier of the triage session.
- `rating` (integer 1–5): User rating for the triage experience.
- `comments`: Additional user comments.

**Response (JSON):**

- Acknowledgement message indicating successful feedback collection.
