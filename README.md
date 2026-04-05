# zoho-creator-skills

Workspace for building apps in Zoho Creator with a layered toolchain:

- Zoho Creator MCP for first-party Creator operations
- Playwright MCP when the Zoho Creator MCP cannot do what we need yet
- Chrome DevTools Protocol for browser-level inspection and control
- Agent skills and repo-local Codex rules for repeatable workflows

## Intent

The Zoho Creator MCP is still primitive. This repo is meant to capture the working setup, guardrails, and skills needed to bridge gaps with browser automation and agent-driven workflows.

## Durable Repo Memory

Tracked context for future agents should stay inside this repo:

- `README.md` for project purpose and structure
- `AGENTS.md` for repo-wide agent rules
- `docs/HANDOFF.md` for durable handoff notes, open work, and known workflow constraints
- `.codex/skills/zoho-creator-dev/SKILL.md` for the concise repo skill

Update those files when the workflow changes. Avoid external or machine-global memory for repo knowledge.

## Working Order

1. Try Zoho Creator MCP first.
2. If it is blocked, incomplete, or too primitive, use Playwright MCP.
3. Use CDP when browser inspection or lower-level control is needed.
4. Record durable MCP gaps and workarounds in `docs/HANDOFF.md`.

## Local-only config

Some project settings are intentionally local and are not committed:

- `.codex/config.toml` for this folder's Zoho MCP connection
- `.codex/local/` for machine-specific helper scripts and per-clone workflow glue

Machine-specific Git and GitHub identity setup should stay local to each clone and should not be committed to the repo.
