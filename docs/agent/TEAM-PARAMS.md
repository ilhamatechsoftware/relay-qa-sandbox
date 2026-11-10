# TEAM-PARAMS — relay-qa-sandbox

> Values the workflow skills and scripts read for this repo. Written by `bootstrap-workflow`; edited by
> hand after that. Method lives in the plugin skills, never here.
> **A field with no value holds `none`.** Never leave a placeholder in angle brackets: a reader takes
> it as the value. Exception: under Script parameters, delete the line instead.

- Template: `devteam 0.1.5` · adopted `2026-11-10`
- Scope: `repo`
- Ownership: `own`

## Gates

| Gate | Command | Who |
|---|---|---|
| Focused test | `none` | seat, every slice |
| Typecheck | `none` | seat, every slice |
| Lint | `none` | seat, every slice |
| Full suite | `none` | lead, once, before deployment (release) |
| Build | `none` | lead, at batch close |

In flight, run the related set only (`execute-plan`, Testing policy). The full gate is every row, once,
on a HEAD export, before deployment.

**Never pipe a gate.** Redirect output to a file and read the exit code.

## Paths

- Frozen paths (denied in `.claude/settings.json`): `none`
- Secret files (read denied): `none` — `.env` and `.env.*` are denied by default
- Review folder: `docs/agent/review/`
- Release log: `none`

## Branch and push

- Base branch: `main`
- Seats push: `no` — `yes` also moves the six push rules (`Bash(git push*)`, `Bash(git -C * push*)`,
  `Bash(env * git push*)` and their `PowerShell(...)` twins) from `ask` to `allow` in `.claude/settings.json`:
  the batch overlay denies every `ask` rule
- Git policy: `own` — strict is the default for `client`: feature branch and PR only, never
  merge or approve a PR
- Protected branches (denied in workspace settings): `none`
- AI attribution trailer: `on` — `off` for `client` unless the client allows it
- Test policy: `allowed` — `client` default `local-only`

## Deploy

- Deploy command: `none` — lead only, after the user's "go"; an `ask` rule in settings
- Detached run: `{deploy} > {log} 2>&1 && echo DEPLOY-OK >> {log} || echo DEPLOY-FAILED >> {log}` —
  `{deploy}` the deploy command, `{log}` a log file outside the repo
- Deploy checks: `none`
- Pre-deploy check and deploy window: `none`
- Production migrations: `none`
- Rollback: `none`

## External services

A seat never writes to these; it reports NOT RUN and names the target.

- `none`

## Team

- Name pool: Ada · Brook · Cyrus · Dana · Ezra · Faye · Gil · Hana · Ivo · Juno
- Quota overrides: `none` — else one line per override: a profile field and its value for this repo

## Browser QA

Field meanings: skill `ui-verification` → "Fields read from `TEAM-PARAMS.md`".

- Stack pack: `none`
- Dev server: `none`
- Seat ports: `none`
- Production build: `none`
- Playwright: `none`
- Login: `none`
- QA accounts: `none`
- Seed: `none`
- QA scripts: `none`
- QA output: `none`
- Viewports: `none`
