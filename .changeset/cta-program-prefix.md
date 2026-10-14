---
'incur': patch
---

Fixed CTA prefixing for multi-word CLI names (e.g. `Cli.create('tempo request')`): CTA commands that start with the program name (e.g. `tempo wallet login`) are now kept as full command lines instead of being rendered as `tempo request tempo wallet login`. String CTAs now follow the same rule as object CTAs, so a string CTA that already starts with the CLI name is no longer prefixed twice.
