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
codex plugin add machine-utilities --marketplace novotnyllc
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
claude plugin install machine-utilities@novotnyllc
```

## Included Plugins

- `dotnet-artisan` from `novotnyllc/dotnet-artisan`
- `agent-utilities` from `novotnyllc/agent-utilities` - agent utility skills for browser control, 1Password, Oracle, native profiling, and CLI design
- `tart-xcode-runner` from `novotnyllc/tart-xcode-runner` - isolated Xcode builds and XCUITests in reusable Tart macOS VMs
- `machine-utilities` from `novotnyllc/machine-utilities` - fleet inventory and reconciliation for packages, agent tooling, projects, dotfiles, remote Macs, SSH, startup tasks, and portable authentication

## Marketplace Manifests

- Codex: `.agents/plugins/marketplace.json`
- Claude Code: `.claude-plugin/marketplace.json`

Plugins published to both manifests use the same repository and subdirectory
path.
