# Privacy and safety boundaries

This public repository is for general guidance. It is not a place to store operational records, secrets, or personal context. The examples are illustrative and do not establish that a workflow is safe or suitable for a particular organization.

## Keep private information out of public material

Never include credentials or tokens; customer, employee, or other business records; personal memory or conversation transcripts; private profiles; machine-specific paths; or real operational data in issues, documentation, examples, or screenshots. Use synthetic data and obvious placeholders such as `[CUSTOMER_NAME]`, `[BUSINESS_NAME]`, and `[EXAMPLE_TOKEN]`. Do not use real data even if names have been removed: details can still identify people or reveal confidential operations.

Before publishing, inspect the complete commit and diff for secrets, personal information, identifying details, and private paths. If sensitive material is exposed, remove or restrict it where possible and revoke or rotate exposed credentials; removing a post may not erase copies already made.

## Understand data flows

Local storage does not mean local model processing. A locally stored record may still be sent to a hosted model, API, plugin, or other provider when a workflow runs. Before using real data, map where it is stored and transmitted, review the current data-handling terms and settings of every relevant provider, and decide whether the data is appropriate to share. Do not assume that a provider retains, uses, or deletes data in a particular way without checking its current terms and configuration.

Use least privilege: grant each tool or integration only the access needed for its task, and avoid broad access to mailboxes, files, databases, and business systems. Keep approval gates for consequential actions such as sending messages, changing records, issuing refunds, or making commitments. Treat the live system of record as authoritative; verify a change by safely reading back the exact target when authorized, rather than relying on an assistant's claim. Keep only the minimum evidence needed to explain what was checked, and redact unnecessary personal or confidential details.

Examples and checklists here are not guarantees of safety, security, correctness, or suitability. They are not legal advice and make no regulatory compliance claim. Organizations must assess their own data, providers, obligations, and risks.

## Upstream projects and licensing

This blueprint points to upstream projects as sources; it does not replace their documentation or policies. Consult official upstream sources for current behavior, security guidance, and license terms. Do not copy upstream documentation, configuration, screenshots, or other assets into this repository. Link to the source and review its licensing and attribution requirements before including any third-party material.