# Pending — filed, not yet ruled

The user rules each row: accept, defer, known gap or close. Need not be empty at close.
Row schema and rules: `README.md` in this folder.

| # | Finding | Source | Lane | Sev | Filed | Class | Decision |
|---|---|---|---|---|---|---|---|
| 1 | README has no link to Relay Board · recommend: accept | relay-qa seed | direct | P3 | 2026-11-10 | docs | |
| 2 | No CI workflow for markdown lint · recommend: defer, trigger: first CI job | relay-qa seed | direct | P3 | 2026-11-10 | ci | |
| 3 | Sandbox has no test runner; all gates `none` · recommend: known gap | relay-qa seed | direct | P2 | 2026-11-10 | gates | |
| 4 | `.gitattributes` holds a duplicate `text=auto` line · recommend: close, harmless | relay-qa seed | direct | P3 | 2026-11-10 | config | |
