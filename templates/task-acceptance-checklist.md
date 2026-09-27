# Task acceptance and verification checklist

Copy this for a task. Define acceptance before action; fill in the result after checking the source of truth. See the [verification guide](../docs/verify-work.md) for context and safe handling of uncertain writes.

> Practice guidance only—not compliance certification or a guarantee. Do not put sensitive records in public issues or documentation. Use an opaque reference or redacted description; keep detailed evidence only in an approved, access-controlled location.

## Before action

- **Goal / intended outcome:**
- **Acceptance criteria (observable, agreed before action):**
  - [ ]
- **Source of truth (system or artifact to inspect):**
- **Expected evidence for each criterion:**
- **Authorization / approval boundary:**
  - Action(s) allowed without further approval:
  - Action(s) requiring approval, and approver:
  - Approval obtained / reference, if required:
- **Target identity confirmed (use a safe identifier/reference):**

## After action

- **Result / status (choose one):** `verified` / `unverified` / `blocked`
- **Evidence reference (opaque reference or redacted description; no sensitive payload):**
- **Read-back performed from the source of truth? What was checked:**
- **Timestamp(s), if relevant (include timezone when useful):**
- **Errors, uncertainty, or limitations:**
- **Next step (pause/investigate/approved recovery/escalate/none):**
- **Person responsible for next step, if applicable:**

## Status reminder

- **Verified:** Named evidence directly supports the stated criterion. This says nothing by itself about overall quality, value, or meaningful impact.
- **Unverified:** The criterion is not established by available evidence. Do not report as done.
- **Blocked:** A prerequisite, authorization, access, or safe way to verify is missing, or an error prevents progress.

If a write timed out or returned an unclear result, do not blindly retry. First inspect the target state and available operation history; repeating the write may duplicate a change that already succeeded. Record what remains uncertain and use an approved recovery path.