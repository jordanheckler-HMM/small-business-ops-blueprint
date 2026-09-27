# Illustrative examples

These examples are teaching material, not a ready-to-run integration. The YAML is intentionally **not plug-and-play**: its angle-bracket placeholders are not valid commands, hostnames, URLs, or credentials. Do not copy it into a live configuration and expect it to work.

Before choosing any MCP server, find and vet the server yourself. Confirm its upstream documentation, version, authentication model, permissions, and privacy/data-retention behavior. Start with least privilege and only grant the access the task requires. Never put secrets in committed files; use a suitable secret-management method for your own environment.

The example shows the general shape of a stdio connection and an HTTP connection. It does not recommend or validate a particular server, declare compatibility, or provide deployment instructions. No wrapper or deployment instructions for the custom local-memory component are provided; Mem0 is an upstream foundation only, not that wrapper.

## Developer details

- See [`mcp-connections.example.yaml`](mcp-connections.example.yaml) for inert, illustrative YAML.
- See [Evidence labels](../docs/evidence-labels.md) for the exact status vocabulary and what each status does—and does not—mean.
- The YAML is syntax-checked as documentation only. Parsing it does not test a server, establish valid runtime configuration, or verify behavior.
