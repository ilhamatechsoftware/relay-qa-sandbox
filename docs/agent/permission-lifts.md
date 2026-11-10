# Permission lifts — relay-qa-sandbox

> Every lift of a `deny` rule and its restore. Append-only. Lead-only.
> - The user authorises **one named change**. Lift only the deny that change needs.
> - Restore it in the landing commit, and always before any seat is spawned.
> - A lift open at spawn reaches every seat: `distribute-tasks` preflight refuses it.
> Procedure: skill `distribute-tasks`, "Hand-ups and lifts".

| Lifted | Rule | Authorised by, words | For (one named change) | Restored | Restore commit |
|---|---|---|---|---|---|
