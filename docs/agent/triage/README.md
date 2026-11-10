# Triage — five files by state

| File | Holds | Leaves when |
|---|---|---|
| `pending.md` | filed, not yet ruled | the user rules (`/workflow triage`) |
| `backlog.md` | open work; **file order = queue** | the work lands |
| `deferred.md` | real, not now; carries a trigger | the trigger is met, or a new ruling |
| `known-gaps.md` | real, accepted as is; never re-raised | never |
| `closed.md` | shipped, fixed or withdrawn | never |

## Rules

- **A row moves; it is never copied.** Cut it from one file; append it to the next with the ruling.
- `pending.md` need not be empty at close.
- A row deferred through three batches is a decision, not a queue state. Say so.
- Counts are recorded as their command, never as a number:
  `grep -cE '^[|] [0-9]+ [|]' docs/agent/triage/<file>.md`
- Next id: highest id in the five state files only, plus one; never `README.md` (its example row is no id):
  `grep -hoE '^[|] [0-9]+ [|]' docs/agent/triage/{pending,backlog,deferred,known-gaps,closed}.md | tr -dc '0-9\n' | sort -n | tail -1`

## Row schema — every file, same columns

```markdown
| # | Finding | Source | Lane | Sev | Filed | Class | Decision |
|---|---|---|---|---|---|---|---|
| 12 | <what is wrong, observable> | <review file, item, ticket key or session> | direct | P2 | 2026-10-06 | <class> | <ruling, date, one-line reason> |
```

- `#` — stable id. **Never renumbered**, never reused.
- `Lane` — `direct` · `design` · `strict`. `Sev` — `P1` · `P2` · `P3`.
- `Class` — one word for the failure family. A class seen twice → a change-set proposal.
  Classes `ticket` and `decision` are exempt. `decision` marks a row that waits on the user: it shows under "Decisions for you".
- `Decision` — empty in `pending.md`. A deferred row names its trigger: `defer 2026-10-06: <reason> ·
  trigger: <event>`.
- A shipped row moves to `closed.md` in the merge commit that ships it; the Decision cell names the
  commit.
