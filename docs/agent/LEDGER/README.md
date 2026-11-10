# Lead ledger — one file per batch

The lead writes state here and drops it from context; it re-reads what it needs. Both flows.

- File: `docs/agent/LEDGER/<batch>.md`. `batch-retrospective` closes it and opens the next.
- Read it at resume, at every wave open, and before any ruling that might contradict an earlier one.
- One line per row, about 200 characters at most. Newest last.
- **Never rewrite a row.** Supersede it with a new row that names the one it replaces.
- A ruling or a cross-item fact is committed before it is messaged. Seats re-read the file at every
  slice start.
- Nothing that `git log`, a behavior entry or an item plan already holds.
- Single-agent flow: `ruling` and `state` rows only.

## Row kinds — no other kind

| Kind | Written when |
|---|---|
| `ruling` | the lead or the user decides something a seat or a later session must honour; triage rulings; owner-explicit decisions. The answer to an ESCALATE NOW question starts `escalate-now:` |
| `state` | item state: lane, ownership rows, merged, in flight; quota stops; a cross-item fact a live seat needs |
| `seat-close` | a seat reports; one line, the transcript dropped (team flow) |
| `hand-up` | item · lane · failing axis · how far into the seat's life; also a line in `hand-ups.jsonl` (team flow) |
| `wave` | wave opens: `open wave <n>`, seats, items, session quota · wave closes, after its review round only: `closed wave <n> · review <findings path> round <label> · exit <clean\|bounded> · session <q> %` (team flow) |

## File shape

```markdown
# Ledger — batch <batch>

| When | Kind | Row |
|---|---|---|
| <YYYY-MM-DD> | ruling | <what was decided> · <by whom> · <source> |
```
