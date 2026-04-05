# zoho-creator-skills

Workspace for building apps in Zoho Creator with a layered toolchain:

- Zoho Creator MCP for first-party Creator operations
- Playwright MCP when the Zoho Creator MCP cannot do what we need yet
- Chrome DevTools Protocol for browser-level inspection and control
- Agent skills and repo-local Codex rules for repeatable workflows

## Intent

The Zoho Creator MCP is still primitive. This repo is meant to capture the working setup, guardrails, and skills needed to bridge gaps with browser automation and agent-driven workflows.

## Local-only config

Some project settings are intentionally local and are not committed:

- `.codex/config.toml` for this folder's Zoho MCP connection
- `.codex/gh-token` for the `aarshps` GitHub token used by local wrappers

Committed project-local helpers live under `.codex/` and enforce this folder's Git/GitHub identity and workflow rules.
