# AGENTS.md

The plugin catalog for `novotnyllc` plugins, published to both Codex and
Claude Code. It carries no plugin source — only pins to other repositories.

## Always

- Three files describe the catalog and must never diverge:
  - `.claude-plugin/marketplace.json` — Claude Code schema, carries `version`
  - `.agents/plugins/marketplace.json` — Codex schema, sha only
  - `.agents/plugins/plugin-versions.json` — version companion to the Codex
    manifest, plus each entry's `path` and `repository`
- Never hand-edit those files to repin. Run:

  ```sh
  scripts/repin NAME SHA VERSION
  ```

  It updates the sha in both marketplace manifests, the `version` in
  `.claude-plugin/marketplace.json` and `plugin-versions.json`, and
  `plugin-versions.json`'s `generatedAt` — then verifies. Each entry's
  `path` is preserved untouched.
- Pins are full 40-character shas. `repin` rejects anything shorter before
  writing a byte.
- A plugin whose source has no `sha` (unpinned, or `ref`-tracked) is not
  repinnable — `repin` fails loudly rather than inventing a field.

## Verify

```sh
scripts/repin check
```

Fails on any sha disagreement between the two marketplace manifests, any
version disagreement between `.claude-plugin/marketplace.json` and
`plugin-versions.json`, and any catalog entry missing from
`plugin-versions.json`. `repin` runs it automatically after every write.

`scripts/repin` is python3 stdlib only — no dependencies, no install step.
This repo has no CI; `repin check` is the gate.
