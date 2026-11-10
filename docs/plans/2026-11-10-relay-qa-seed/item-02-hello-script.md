# Item 02 — Add tiny hello script — Evidence Map & Slice Ledger

> **Pinned at commit: `4b290a1`** · Slug: `hello-script` · Seat: single agent
> Lane: direct — one new script, no shared code
> Depends on: none · Contract: user ruling in chat, 2026-11-10
> Behaviors: none · new: 0
> Re-pin note: none

## Evidence Map
| Tag | Path | Symbol / fact |
|---|---|---|
| [V] | `scripts/` | absent at the pin |

## Slice ledger
1. **Write script** — DETAILED BELOW

### 1 · Write script   [behaviors: none · risk: ordinary]

**Done when (MUST)**
- `node scripts/hello.mjs` prints `hello relay` and exits 0.
`verify: node scripts/hello.mjs` — guards: wrong output, non-zero exit

**The set (MUST)** — `scripts/hello.mjs` → 1 site.

**Ownership rows (MUST)** — `scripts/hello.mjs`.
Contested: none

**Constraints (MUST)**
- No dependencies. Node built-ins only.
- `knoco-qa/` unchanged.

**Hand up if:** `scripts/` exists at the pin.
