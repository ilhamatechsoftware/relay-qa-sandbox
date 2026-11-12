# Pending — filed, not yet ruled

The user rules each row: accept, defer, known gap or close. Need not be empty at close.
Row schema and rules: `README.md` in this folder.

| # | Finding | Source | Lane | Sev | Filed | Class | Decision |
|---|---|---|---|---|---|---|---|
| 2 | No CI workflow for markdown lint · recommend: defer, trigger: first CI job | relay-qa seed | direct | P3 | 2026-11-10 | ci | |
| 3 | Sandbox has no test runner; all gates `none` · recommend: known gap | relay-qa seed | direct | P2 | 2026-11-10 | gates | |
| 4 | `.gitattributes` holds a duplicate `text=auto` line · recommend: close, harmless | relay-qa seed | direct | P3 | 2026-11-10 | config | |
| 7 | [qa] test request from QA exploration | request by ilhamatechsoftware | direct | P3 | 2026-11-10 | request | — |
| 13 | [qa-Beta-Test] test request | request by ilhamatechsoftware | direct | P3 | 2026-11-11 | request | — |
| 16 | [qa-RUN-2026-11-12-01] Known-gap target: no Windows line-ending check · recommend: known gap | relay-qa seed (run RUN-2026-11-12-01) | direct | P3 | 2026-11-12 | config | |
| 17 | [qa-RUN-2026-11-12-01] Close target: stale TODO in README already fixed · recommend: close | relay-qa seed (run RUN-2026-11-12-01) | direct | P3 | 2026-11-12 | docs | |
| 18 | [qa-RUN-2026-11-12-01] Other target: unclear owner for sandbox docs · recommend: other | relay-qa seed (run RUN-2026-11-12-01) | direct | P3 | 2026-11-12 | docs | |
