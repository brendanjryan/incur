---
'incur': patch
---

Fixed `--mcp` in bundled and compiled CLIs (e.g. `bun build --compile`, esbuild) by loading `@modelcontextprotocol/server/stdio` through a literal dynamic import that bundlers can include.
