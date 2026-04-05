# Handoff

## Scope

This repo is the tracked workspace for building Zoho Creator apps with a layered toolchain:

- Zoho Creator MCP first
- Playwright MCP when Zoho Creator MCP cannot do the job
- Chrome DevTools Protocol for browser inspection and lower-level control
- Repo-local agent skills and rules for repeatable workflows

## Current State

- The repo is intentionally minimal and currently holds workflow memory, not app code.
- `main` is the primary branch and is already connected to `origin`.
- Machine-specific auth and Codex config are local-only and must stay out of git.
- Ignored `.codex/config.toml` and `.codex/local/` files are expected clone-local state, not tracked repo artifacts to clean up.

## Durable Rules

- Keep durable repo knowledge in tracked files inside this repo.
- Prefer updating `README.md`, `AGENTS.md`, this file, or the repo skill instead of relying on external memory.
- Keep repo-level guidance generic. Do not commit one machine's GitHub identity, tokens, browser profiles, or local auth wiring.

## Workflow

1. Start with Zoho Creator MCP.
2. If a required action is missing or unreliable there, move to Playwright MCP.
3. Use CDP when Playwright alone is not enough for inspection or control.
4. When a gap or workaround is likely to matter again, record it here.

## Known Limitations

- In this environment, the project-scoped `zoho_hora` MCP URL on `*.zohomcp.com` can be blocked by Zscaler before MCP initialization completes.
- The observed failure mode is an HTTPS MITM certificate from `Zscaler Inc.`, followed by `HTTP/1.1 403 Forbidden` with a Zscaler HTML block page instead of an MCP JSON or SSE response.
- The current block reason is `Not allowed to browse Miscellaneous or Unknown category`, so this is a network policy issue rather than an MCP payload or Codex config issue.
- Workaround: ask network/security to allowlist or recategorize the Zoho MCP host, or use Playwright/CDP to continue browser-driven Creator work while Zoho MCP remains blocked.

## Open Work

- Add the first real Zoho Creator app scaffold or example workflow.
- Capture the actual Zoho Creator MCP tool surface and its known limitations once exercised.
- Add Playwright/CDP patterns only after they are proven in this repo's real workflows.

## Update Discipline

- Replace stale notes instead of appending noisy session logs.
- Keep this file concise and durable.
- If a new reusable workflow emerges, prefer a repo skill or a short tracked reference over long AGENTS prose.
