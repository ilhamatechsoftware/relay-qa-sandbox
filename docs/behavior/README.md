# Behavior catalog — highest authority

Given/When/Then entries for observable behavior. Each entry has a stable ID, **never renumbered**.
**When this layer conflicts with anything else in `docs/`, this layer wins.**

## Rules

- **No file lists.** To find the code for a behavior, grep the repository for its ID.
- **Lazy fill.** An area gets its file when work first touches it. No backfill pass over existing
  features.
- One file per area: `<AREA>.md`. IDs are `<AREA>-<n>`. In team flow, the lead allocates IDs at
  dispatch.
- An entry is never deleted or renumbered. A changed behavior is amended in place, with a dated line.
- **Inline markers** record how a point was settled:
  - `FLAGGED` — an assumption taken during the build; confirmed or overturned later.
  - `DECIDED` — an internal, reversible choice; one line.
  - `OWNER DECISION <date>` — the user chose against the recommendation; never changed without a new
    ruling.
- Entry edits are code: they are reviewed with the change that makes them true.

## Entry shape

```markdown
# <AREA> — <what the area does for the user>

Design: <link to docs/design/...>

## <AREA>-1 — <behavior in one line>

**Given** <state>,
**When** <action or event>,
**Then** <observable result>.

- FLAGGED: <assumption>, item <id>.
- **Amended <YYYY-MM-DD>, item <id>.** <what changed and why>.
```
