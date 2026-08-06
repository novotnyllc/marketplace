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
codex plugin add dotnet-artisan --marketplace novotnyllc
codex plugin add agent-utilities --marketplace novotnyllc
codex plugin add tart-xcode-runner --marketplace novotnyllc
codex plugin add railyard --marketplace novotnyllc
codex plugin add roundhouse --marketplace novotnyllc
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
claude plugin install tart-xcode-runner@novotnyllc
claude plugin install railyard@novotnyllc
claude plugin install roundhouse@novotnyllc
```

## Included Plugins

- `dotnet-artisan` from `novotnyllc/dotnet-artisan`
- `agent-utilities` from `novotnyllc/agent-utilities` - the craft-skill toolbox: browser automation, CLI design, frontend design, profiling, 1Password, and skill auditing
- `tart-xcode-runner` from `novotnyllc/tart-xcode-runner` - isolated Xcode builds and XCUITests in reusable Tart macOS VMs
- `railyard` from `novotnyllc/railyard` - the delivery system for agent work: model routing, goal-driven delivery, task orchestration, cross-machine placement, and review gates
- `roundhouse` from `novotnyllc/roundhouse` - machine and infrastructure administration: fleet readiness, inventory, parity, packages, dotfiles, auth, SSH transport, privileged installs, and UniFi

## Marketplace Manifests

- Codex: `.agents/plugins/marketplace.json`
- Claude Code: `.claude-plugin/marketplace.json`

Plugins published to both manifests use the same repository and subdirectory
path.
