# my-harness

Personal harness. It holds agents, commands, and rules for daily work.

## Philosophy

One main agent (orchestrator) plus subagents (coder/explorer/librarian/reviewer) for a better structure and productivity.
Security: tools allowed by default so new plugins and MCP servers just work, agents deny only what their role must not do, unknown shell commands ask, hard policies block force push, `sudo`, and secret files. Review gate on every non-trivial change.

## Harnesses

### Opencode

- [Installation](opencode/installation.md)
- [Plugins](opencode/plugins.md)
