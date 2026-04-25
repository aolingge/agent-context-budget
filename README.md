<p align="center">
  <img src="assets/readme-banner.svg" alt="Agent Context Budget banner" width="100%">
</p>

<h1 align="center">Agent Context Budget</h1>

<p align="center">Estimate whether repo instructions, prompts, and docs are small enough for AI coding agents to load.</p>

<p align="center"><a href="README.zh-CN.md">中文</a> · <a href="#quick-start">Quick Start</a> · <a href="#checks">Checks</a></p>

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/node-%3E%3D18-14B8A6">
  <img alt="dependencies" src="https://img.shields.io/badge/dependencies-0-111827">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-2563EB">
</p>

## Why This Exists

AI agent tooling is growing quickly, but many repos still miss tiny checks that can run locally or in CI. This project stays zero-dependency, short-command, and easy to fork.

## Quick Start

```bash
npx github:aolingge/agent-context-budget --path AGENTS.md
```

Generate Markdown:

```bash
npx github:aolingge/agent-context-budget --path AGENTS.md --markdown > report.md
```

Use a score gate:

```bash
npx github:aolingge/agent-context-budget --path AGENTS.md --min-score 80
```

## Checks

| Check | What it looks for |
| --- | --- |
| has-purpose | Explains why this file belongs in agent context. |
| has-commands | Contains concrete commands. |
| has-boundary | Defines what should not be loaded or edited. |
| has-summary | Provides a compact summary. |

## Output

```text
Agent Context Budget score: 100/100
PASS  example-check  Useful signal found
FAIL  missing-check  Add the missing guidance
```

## Contributing

Good first PRs: add checks, add fixtures, improve docs, or add GitHub Actions examples.

## License

MIT
