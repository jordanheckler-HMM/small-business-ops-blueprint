# New service-request intake

New here? Start with the [plain-language Start Here guide](../start-here.md), then return to the [workflow index](README.md). This illustrative example shows how an assistant could organize a new request so a person can review it. It does not take on the business's decisions or contact anyone.

**Evidence: illustrative—not tested.** This is a conceptual example, not an exercised integration. No integrations, setup, system access, or end-to-end workflow have been verified. See the [evidence-label guide](../evidence-labels.md).

## Plain-language summary

A person provides a request. The assistant organizes only the details needed to understand it and prepares a draft for a human to check. The human decides what happens next. Until a separately defined and reviewed workflow grants safe authority, the assistant does not send a reply or create or change a live record without human approval and the required consent.

## Developer-oriented steps and controls

### Purpose and when to use

Use as a discussion template for routing a new, ordinary service inquiry to a responsible person. Do not use it to make eligibility, safety, legal, or service commitments.

### Trigger

A person submits a new request through a channel the business has designated for intake. The channel and intake mechanism are unspecified placeholders; no particular integration is assumed.

### Minimal inputs

Collect only what is needed for a human to understand and follow up:

- A short description of the requested service or question.
- A preferred contact method and contact detail, only when needed and voluntarily provided.
- A broad location or timing detail only if needed to route the request.
- Any stated constraint essential to triage; avoid collecting sensitive details by default.

Use placeholders such as `[request summary]` and `[preferred contact method]` in drafts. Do not add real or identifying customer examples.

### Live system of record

The business's designated live intake or customer-record system is the system of record. It is not specified here. A draft or assistant conversation is not the authoritative record. Confirm the actual system and its owner before any implementation.

### What the assistant may draft or prepare

- A concise, neutral summary from the information provided.
- A proposed category or routing suggestion clearly marked for human review.
- A draft acknowledgment or follow-up for review; it must not be sent automatically.
- A checklist of missing, necessary details to ask about, without inventing answers.

### Approval boundary

A human must review and explicitly approve any message before it is sent, and ensure required consent is present. A human must also approve any creation or change in the live system. No sends or live record writes occur without human approval and consent; any future exception requires a separately specified and reviewed safe-authority workflow. The assistant must not infer approval from silence.

### Failure or uncertainty path

If the request is ambiguous, incomplete, sensitive, outside the agreed scope, or the system is unavailable, stop and route the draft to a human. Do not guess, promise service, retry a write blindly, or send a message. Ask a human to resolve uncertainty using the appropriate business process.

### Evidence and read-back

After an approved human action, verify the exact target in the live system: confirm the intended record exists or reflects the approved change and that its content matches the approved draft. For an approved message, check the designated channel's sent state and recipient. Retain only the minimum business-appropriate evidence of approval and read-back. A tool success response alone does not prove the business outcome.

### Privacy and data minimization

Collect and retain only information necessary for intake and follow-up. Prefer a short summary over full message histories; omit sensitive or unrelated details. Restrict access and retention according to the business's applicable policy. Do not put personal information in examples, test data, or unnecessary logs.

This example is not professional or legal advice and does not define a business's service or privacy policy.
