# Project Rules

- Before substantial work in this repo, read [docs/HANDOFF.md](docs/HANDOFF.md) and [./.codex/skills/zoho-creator-dev/SKILL.md](.codex/skills/zoho-creator-dev/SKILL.md).
- This repo is for developing Zoho Creator apps with Zoho Creator MCP, Playwright MCP, Chrome DevTools Protocol, and agent skills.
- Prefer Zoho Creator MCP first. If it cannot perform a task, use Playwright MCP, CDP, or agent skills to bridge the gap.
- Capture durable workflow changes, limitations, and workarounds in tracked repo files, not in external memory.
- Keep machine-local Codex config, auth tokens, and browser state out of git.
- Keep machine-specific Git and GitHub identity setup local to each clone instead of committing it to the repo.
