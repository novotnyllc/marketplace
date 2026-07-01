# Claire Novotny LLC Plugins

Shared plugin marketplace for Claire Novotny LLC plugins, published for both
Codex and Claude Code.

## Install (Codex)

Add the marketplace once:

```bash
codex plugin marketplace add novotnyllc/marketplace
```

Then install the plugins you want:

```bash
codex plugin add codex-director --marketplace novotnyllc
codex plugin add subagent-orchestration --marketplace novotnyllc
codex plugin add dotnet-artisan --marketplace novotnyllc
codex plugin add browser-control --marketplace novotnyllc
codex plugin add agent-utilities --marketplace novotnyllc
```

## Install (Claude Code)

Add the marketplace once:

```bash
claude plugin marketplace add novotnyllc/marketplace
```

Then install the plugins you want:

```bash
claude plugin install dotnet-artisan@novotnyllc
claude plugin install agent-utilities@novotnyllc
```

The `codex-director` and `subagent-orchestration` plugins are Codex-only; they
orchestrate Codex threads and `multi_agent_v2` subagents, which have no Claude
Code equivalent, so they are not published to the Claude marketplace.

## Included Plugins

- `codex-director` from `novotnyllc/codex-director` - project Director workflow with quiet, signal-first worker monitoring
- `subagent-orchestration` from `novotnyllc/subagent-orchestration`
- `dotnet-artisan` from `novotnyllc/dotnet-artisan`
- `browser-control` from `novotnyllc/browser-control`
- `agent-utilities` from `novotnyllc/agent-utilities` - agent utility skills for browser control, remote Macs, 1Password, Oracle, native profiling, and CLI design

## Marketplace Manifests

- Codex: `.agents/plugins/marketplace.json`
- Claude Code: `.claude-plugin/marketplace.json`

Both manifests reference the same plugin repositories and subdirectory paths, so
a plugin resolves identically from either agent.
