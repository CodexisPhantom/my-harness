# Installation

No install command in this repo. Target is `~/.config/opencode`.

## Prerequisites

- `git`, `bun` installed.
- `opencode` installed (creates `~/.config/opencode/opencode.json`).

## Steps

1. Install opencode first.
2. Copy `opencode/agents/`, `opencode/commands/`, `opencode/instructions/` from this repo into `~/.config/opencode/`.
3. Copy `AGENTS.md` to `~/.config/opencode/AGENTS.md` (`~/AGENTS.md` optional).
4. Merge: copy content of this repo `opencode/opencode.jsonc` INTO `~/.config/opencode/opencode.jsonc`. Remove what you don't want. Keep `permissions` and `policies` in the global file: policies there override project configs.
5. Verify: run `opencode`.

## Troubleshooting

- Config missing: check `~/.config/opencode/opencode.json` exists.
- Bun fails: retry with `npm`/`npx`.
