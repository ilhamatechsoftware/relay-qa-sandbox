# Item 01 — Add README purpose section — Evidence Map & Slice Ledger

> **Pinned at commit: `4b290a1`** · Slug: `readme-purpose` · Seat: single agent
> Lane: direct — one new doc file, no behavior
> Depends on: none · Contract: user ruling in chat, 2026-11-10
> Behaviors: none · new: 0
> Re-pin note: none

## Evidence Map
| Tag | Path | Symbol / fact |
|---|---|---|
| [V] | `README.md` | absent at the pin |

## Slice ledger
1. **Write README** — DETAILED BELOW

### 1 · Write README   [behaviors: none · risk: ordinary]

**Done when (MUST)**
- `README.md` exists with a `## Purpose` section.
`verify: grep -c "^## Purpose" README.md` — guards: section missing

**The set (MUST)** — `README.md` → 1 site.

**Ownership rows (MUST)** — `README.md`.
Contested: none

**Constraints (MUST)**
- `knoco-qa/` unchanged.

**Hand up if:** `README.md` exists at the pin.

---
**Report** — landed `0f353f2`. Gate: NOT RUN, all gates `none`. Verify: 1 match.
