# Verify the work: evidence, not a “done” message

A completion message tells you what someone—or an automated system—claims happened. It does not by itself show that the intended change reached the right place, persisted, or meets your need. A request can fail, affect the wrong record, or time out after the system has already made the change. Treat the message as a prompt to check, not as proof.

This guide is for business owners and the developers helping them. The basic habit is the same at either level: agree on what “done” means before acting, check a source that can establish the result, and report exactly what the evidence does and does not show.

## Before action: define “done”

Write one or more observable acceptance criteria before anyone or anything acts. Prefer specific statements that a person can check over broad goals such as “handle this correctly.” For example: “The designated record shows the approved status.” If a task has several important outcomes, give each its own criterion. Identify which actions need human authorization or approval, and who can provide it.

Choose the **source of truth** in advance: the system or artifact whose state matters for the criterion. Decide what evidence you expect to inspect there—such as a fresh read-back of the target record, a saved document, or a result from an authoritative system. A tool’s “success” response or a screenshot of an input form may be useful context, but may not prove the final state. Match evidence to the claim; do not infer more than was checked.

## After action: check and report

1. **Confirm authorization.** Check that the action was within the approved boundary. If approval was required and is missing, stop; do not treat the action as authorized.
2. **Read the target back.** Use the intended source of truth, freshly and at the target that was supposed to change. Compare its state with each prewritten criterion. A response that a request was accepted is not the same as confirming the persisted result.
3. **Record the outcome and limits.** Note the status, what was checked, when it was checked if timing matters, and any error, missing evidence, or limitation. Link to a safe evidence reference or use a redacted description. If evidence is incomplete, say so plainly.
4. **Choose the next step safely.** If the result is wrong, absent, or uncertain, pause and investigate. Do not blindly retry a write: it may already have succeeded despite a timeout or lost response, and repeating it could duplicate or compound the change. First inspect the target and any available operation history; then follow an approved recovery path or ask an authorized person.

Use these statuses consistently:

- **Verified** — The source-of-truth read-back or other named evidence directly supports the stated acceptance criterion. State the scope of that check.
- **Unverified** — The action may have happened, but available evidence does not establish the criterion. Keep the uncertainty visible; do not call it done.
- **Blocked** — A prerequisite, approval, access, or safe verification path is missing, or an error prevents progress. State what is needed next.

Verified completion is a narrow statement about the agreed criterion and the evidence checked. It does not mean the work was high quality in every respect, created business value, or had meaningful impact. Those are separate judgments that require their own criteria and evidence. Do not turn verification into a numerical score or imply that a checklist measures impact.

## Keep evidence minimal and private

Collect only what is needed to establish the criterion. Prefer an opaque reference (for example, a non-sensitive internal ticket or operation reference) or a redacted description over copying business data. Do not put customer, employee, financial, credential, or other sensitive records in public issues, public documentation, or screenshots shared publicly. Store any necessary detailed evidence only in an approved, access-controlled place; follow your organization's retention and privacy practices. If safe evidence cannot be shared, record where an authorized reviewer can find it without exposing the underlying record.

## Illustrative walk-through — illustrative, not tested

This generic example is a paper illustration only; it was not tested and uses no integration.

- **Criterion:** A designated generic record displays the approved status.
- **Authorization:** An authorized person approves the status change; the operator confirms the target before acting.
- **Action:** The operator requests the single intended update.
- **Read-back:** The operator opens the target record in the chosen source of truth and checks that its status matches the approved value.
- **Outcome:** If the fresh read-back matches, report **verified** for that criterion and cite a safe, opaque reference. If the read-back is unavailable or does not establish the state, report **unverified** (or **blocked** if access/approval is missing), record the limitation, and investigate before considering another write.

This checklist is practice guidance. It is not a compliance certification, a security review, or a guarantee that an action or system is safe or correct.

## Developer notes

Keep the acceptance criterion, target identity, authorization decision, write result, and read-back distinct in logs or audit records. A transport/API success response is not necessarily persisted state. For timeouts and ambiguous write results, prefer a read-before-retry or a documented idempotent recovery procedure, when available; do not assume repeating a request is safe. Limit evidence capture and access to what is necessary, and avoid recording sensitive payloads in general-purpose logs or public issue trackers. Report the exact target/environment and verification time when they matter to the claim.