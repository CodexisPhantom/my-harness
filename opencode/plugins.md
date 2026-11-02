# Plugins

## List

| Name            | Via        | Repo                                                              |
| --------------- | ---------- | ----------------------------------------------------------------- |
| envsitter-guard | standalone | [envsitter-guard](https://github.com/boxpositron/envsitter-guard) |
| rtk             | tokless    | [rtk](https://github.com/rtk-ai/rtk)                              |
| codegraph       | tokless    | [codegraph](https://github.com/colbymchenry/codegraph)            |
| context-mode    | tokless    | [context-mode](https://github.com/mksglu/context-mode)            |
| headroom        | tokless    | [headroom](https://github.com/headroomlabs-ai/headroom)           |
| projectmem      | tokless    | [projectmem](https://github.com/riponcm/projectmem)               |
| magic-context   | standalone | [magic-context](https://github.com/cortexkit/magic-context)       |

## Envsitter-guard

- Docs: https://github.com/boxpositron/envsitter-guard

```json
{
  "$schema": "https://opencode.ai/config.json",
  "plugins": ["envsitter-guard@latest"]
}
```

or

```sh
opencode plugin add envsitter-guard@latest
```

## Magic-context

- Docs: https://docs.cortexkit.io/magic-context/getting-started/installation/
- Node:

```sh
npx @cortexkit/magic-context@latest setup --harness opencode
```

- Bun:

```sh
bunx @cortexkit/magic-context@latest setup --harness opencode
```

- `opencode.jsonc`:

```json
{
  "plugin": ["@cortexkit/opencode-magic-context@latest"]
}
```

- Set compaction `auto: false`.

## Via tokless

- Linux/macOS:

```sh
curl -fsSL https://raw.githubusercontent.com/HoangP8/tokless/main/scripts/install.sh | bash
```

- Windows:

```powershell
irm https://raw.githubusercontent.com/HoangP8/tokless/main/scripts/install.ps1 | iex
```

- Install tools:

```sh
tokless --tools rtk,codegraph,context-mode,headroom,projectmem --agents opencode
```

- Verify

```sh
tokless doctor
```
