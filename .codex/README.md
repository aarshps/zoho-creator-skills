# Local GitHub Identity Guardrails

This folder pins Git and GitHub CLI usage to the GitHub identity `aarshps` only.

Use these wrappers:
- `bash ./.codex/bin/git`
- `bash ./.codex/bin/gh`

Git commit identity:
- name: `Aarsh`
- email: `aarshps@gmail.com`
- username: `aarshps`

Authentication setup:
- Put a valid `aarshps` GitHub token in `.codex/gh-token`, or
- Export `GH_AARSHPS_TOKEN` in the shell that launches Codex.

The wrappers verify that the token resolves to `aarshps` and fail closed otherwise.
