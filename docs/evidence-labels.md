# Evidence labels and status guidance

This page explains how to read evidence statements in this guide. In plain language, a label tells you what was actually checked—not whether a component is secure, reliable, deployable, or suitable for your business. A narrow check must stay narrow: seeing a connection or reading documentation is not proof of a working end-to-end system.

## Developer details

Use exactly one of these labels when describing evidence:

- **tested by us** — State precisely what we exercised, when we exercised it, and the environment or target checked. Name the source of the result (for example, a command/test and its output, or a read-back of the target state). Keep the claim limited to that check; do not imply broader compatibility, security, or production readiness.
- **based on upstream documentation** — Name the upstream project/documentation source and the date reviewed. State which documented fact supports the statement. Documentation review is not a local test and does not establish that the documented behavior works in a particular deployment.
- **illustrative—not tested** — Say the example is conceptual or schematic, and identify that it was not exercised as a working integration. This label must not imply installation, runtime validity, interoperability, or deployability.

For every status statement, provide what was verified, when, and the source. If any of those details are unavailable, do not imply verification; describe the limitation plainly. Use dates in an unambiguous format such as `YYYY-MM-DD`.

## Applying labels here

The architecture page's named roles are examples, not an assertion that the components are integrated. Its local MCP connection/tool-discovery checks are narrowly described as connection and discovery checks on 2026-09-27; they do not prove installation, independent deployment, end-to-end workflows, or interoperability. The public guide provides no wrapper or deployment instructions for the custom local-memory component. Mem0 is identified only as an upstream foundation.

The [configuration example](../examples/mcp-connections.example.yaml) is **illustrative—not tested** as a server configuration. YAML parsing can verify syntax only; it cannot establish that placeholders are valid runtime values, that a server exists, or that a connection or workflow works.

When status changes, update the statement with the exact check, date, and source rather than broadening the label. A label is evidence provenance, not a security certification or endorsement.
