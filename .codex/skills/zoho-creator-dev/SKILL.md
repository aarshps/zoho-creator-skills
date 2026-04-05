---
name: zoho-creator-dev
description: Use when working in this repo on Zoho Creator app development, Zoho Creator MCP gaps, or browser automation workflows. Read docs/HANDOFF.md first, prefer Zoho Creator MCP before Playwright MCP or CDP, and keep machine-local auth and config out of git.
---

# Zoho Creator Dev

Use this skill for substantive work in this repo.

## Start Here

1. Read `docs/HANDOFF.md`.
2. Confirm whether the task is Creator-native, browser-driven, or a workflow/setup task.

## Execution Order

1. Try Zoho Creator MCP first.
2. If it is blocked, primitive, or missing a needed operation, use Playwright MCP.
3. Use CDP when browser inspection or lower-level control is required.

## Repo Memory

- Put durable repo knowledge in tracked files inside this repo.
- Update `README.md` for project-level intent.
- Update `AGENTS.md` for repo-wide agent rules.
- Update `docs/HANDOFF.md` for durable limitations, workarounds, and open work.

## Closeout

1. Before ending a substantial session, consolidate reusable findings into the tracked repo memory files.
2. Remove temporary artifacts that are not meant to become durable repo assets.
3. Keep `SKILL.md` under 100 lines and move longer guidance into tracked docs.

## Guardrails

- Do not commit machine-local Codex config, auth, tokens, browser state, or per-clone GitHub identity setup.
- Keep repo-level guidance generic so other users and machines can clone it safely.
- If you add another skill, keep `SKILL.md` concise and move detailed references into tracked docs.
