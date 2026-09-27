# Start here

## What this is

This blueprint is a plain-language guide to thinking about AI-assisted operations in a small business. It helps owners and operators describe what they want to improve, make sensible early decisions, and give a developer a useful brief. It aims to remain provider-neutral: the ideas should not depend on one vendor or product.

**Right now, this is documentation only.** There is no proven installation, setup, runnable kit, or validated combination of components here. The guide will grow in stages: first orientation and shared vocabulary, then architecture and workflows, and only later any implementation guidance that has been checked. Examples of products, if discussed, are illustrative—not proof that they work together.

## What this is not

- Not a ready-to-install application or an automated employee.
- Not a promise that AI will make decisions safely or correctly without oversight.
- Not a requirement to use a specific provider or tool.
- Not a substitute for your business's privacy, legal, security, or professional advice.

## The basic layers

Think of these as jobs a system may need to do, not products you need to buy. A future guide may explain possible designs; this page does not claim these layers are implemented or integrated.

1. **Assistant and orchestration:** The place a person makes a request, plus the coordination of steps and permissions needed to respond or act.
2. **Memory and continuity:** Approved information that needs to carry forward between interactions, such as stable preferences or operating procedures. Decide what may be retained and who controls it.
3. **Tools and integrations:** Connections to business systems—such as calendars or customer records—that let a system retrieve information or perform actions. Each connection needs an owner, limited permissions, and careful review.
4. **Workflows:** The repeatable process: what starts it, what steps happen, where a person reviews, and what happens when something fails or is uncertain.
5. **Verification:** Evidence that the intended result actually happened and is correct enough for its purpose. A success message alone is not proof; define what someone should check.

## First decisions

Start with one narrow, recurring task—not “automate the business.” Write down:

- Who does the task today, and what useful outcome should improve?
- What starts it, what information is needed, and what steps or exceptions occur?
- What information is sensitive, and what must never be shared or retained?
- Which actions may be suggested, and which require a person to approve them?
- What evidence would show the result is correct, and who will check it?
- What systems or accounts might be involved, and who owns them?

Use the [glossary](glossary.md) for terms such as orchestration, local memory, and task verification.

## When you need technical help

You can make the business decisions first: choose a task, describe the current process, identify risks, and say what a good result looks like. Involve a developer before connecting accounts or business data, granting permissions, storing sensitive information, or allowing a system to send messages, change records, or spend money. Ask for technical and security review when access, privacy, reliability, or recovery from mistakes is unclear. Do not treat this documentation as setup instructions.

## Developer handoff

Copy and fill in this brief; leave unknowns marked **TBD** rather than guessing.

```text
Business task:
Current process and people involved:
Desired outcome (how we will measure/check it):
Trigger and expected frequency:
Information needed (and sensitive information to exclude):
Systems/accounts involved and their owners:
Actions the system may suggest:
Actions requiring human approval:
Exceptions and failure/recovery steps:
Who verifies each result, and what evidence they check:
Access, privacy, retention, and security constraints:
What is unknown / needs investigation:
```

## About this project

GitHub is the public project shelf/library where these guide files are stored; you do not need to use it to read this page. For the project's current guide index, see [Documentation](README.md).