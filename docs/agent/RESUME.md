# RESUME — 2026-11-10 adopt

## Live state
- Start folder: D:/My Work/ATech Solutions/Relay Board/relay-qa-sandbox
- Production: none · nothing deploys
- Branch: main · adopt commit not pushed
- Running: seats none · servers none
- Fixtures left: `knoco-qa/triage/knoco-qa-pending.md` — Knoco QA fixture, kept as is

## Decisions for you
- none

## Owner checks still open
- none

## NEXT
1. no row — first design pass: fill `docs/agent/PROJECT.md` "What this is", single-agent flow

## THEN
- Pick a stack, then fill the five gates in `docs/agent/TEAM-PARAMS.md`

## Known half-state shipping — do not file it
- All gates `none` — no stack yet · closed when a stack is chosen · wrong fix: a vacuous gate script

## Standing facts — do not re-derive
- `.claude/settings.json` loads from the next session started in `D:/My Work/ATech Solutions/Relay Board/relay-qa-sandbox`, not in the session that wrote it
- Global `core.hooksPath` = `~/.teamtrics/hooks` (`post-commit`); repo git hooks never fire — check: `git config --global core.hooksPath`
- Team flow unavailable: `CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS` not set — check: `echo $CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS`
