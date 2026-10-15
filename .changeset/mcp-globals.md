---
'incur': patch
---

Fixed `globals` being dropped from MCP tools and the generated OpenAPI document. Global options are now merged into every MCP tool's input schema (stdio `--mcp` and HTTP `/mcp`) and into each OpenAPI operation's query parameters or request body. MCP tool calls split them back out, apply the globals schema's defaults and validation, and pass them to commands and middleware as `globals`. `Mcp.serve` accepts a `globals` schema for CLIs that serve their command map directly. A global wins over a command option of the same name, as on the CLI.
