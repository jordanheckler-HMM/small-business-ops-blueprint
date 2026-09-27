# Appointment scheduling or change

New here? Start with the [plain-language Start Here guide](../start-here.md), then return to the [workflow index](README.md). This illustrative example shows how an assistant could prepare a proposed appointment booking or change for a person to review. It does not reserve or change a time on its own.

**Evidence: illustrative—not tested.** This is a conceptual example, not an exercised integration. No integrations, setup, system access, or end-to-end workflow have been verified. See the [evidence-label guide](../evidence-labels.md).

## Plain-language summary

A person asks about an appointment or requests a change. The assistant can organize the request and prepare a proposed option for a human to check. A time is not booked, changed, or confirmed until a human approves the action, required consent is clear, and the live schedule is checked afterward.

## Developer-oriented steps and controls

### Purpose and when to use

Use as a discussion template for preparing a proposed appointment or change for human review. Do not use it to decide business availability policy, resolve competing priorities, or make commitments.

### Trigger

A person submits a new appointment request or asks to change an existing appointment through a business-designated channel. No channel, booking tool, or integration is assumed.

### Minimal inputs

Use only what is needed to locate or prepare the requested appointment:

- Request type: new appointment, reschedule, or cancellation.
- A reference to the existing booking when a change requires one; use the minimum identifier needed.
- The person's requested date/time range and time zone, if relevant.
- A preferred contact method only if follow-up is needed and the person provides it.

Use placeholders such as `[booking reference]`, `[requested time range]`, and `[time zone]`. Do not include actual names, schedules, or booking details.

### Live system of record

The business's designated live scheduling system is the system of record; it is unspecified here. A proposed time in a draft is not a reservation or confirmation. Identify the authoritative schedule and its owner before implementation.

### What the assistant may draft or prepare

- A neutral summary of the request and any essential missing details.
- A proposed availability query or candidate time for human review, if an authorized person supplies current availability.
- A draft confirmation, rescheduling, or cancellation message, clearly marked for approval and not sent automatically.
- A proposed schedule action for human review, without submitting it.

The assistant must not invent availability, treat a suggestion as a reservation, or represent a request as confirmed.

### Approval boundary

A human must review and explicitly approve any booking, schedule change, or cancellation before it is written to the live schedule. A human must approve any message before it is sent and ensure required consent is present. No sends or schedule writes without human approval and consent, unless a separately specified and reviewed future workflow explicitly defines safe authority. Silence, a displayed candidate, or a tool response is not approval.

### Failure or uncertainty path

If availability is stale or conflicting, the request is ambiguous, a booking cannot be confidently identified, or the scheduling system is unavailable, stop and hand off to a human. Do not guess, double-book, imply confirmation, or blindly retry an uncertain write. Ask the responsible person to resolve it and communicate through the approved process.

### Evidence and read-back

After an approved action, read the exact booking back from the live schedule. Verify the intended booking reference, status, date/time, and time zone where applicable; confirm a cancellation or change is reflected rather than assuming it from a success response. For an approved notice, verify its sent state and recipient in the designated channel. Keep only appropriate evidence of approval and read-back.

### Privacy and data minimization

Use the least information needed to find or prepare the appointment. Avoid copying unrelated notes or sensitive details into drafts and logs. Limit access and retention according to the business's applicable policy. Use placeholders in documentation and tests, not real schedule or customer data.

This example is not professional, legal, or booking-policy advice and does not set cancellation, availability, or notice rules.
