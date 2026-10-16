# sharingu — the plugin

The sharingu plugin for Claude Code (and Codex): one MCP server at `https://agent.sharingu.xyz/mcp` and the sharingu
starter pack as skills. The plugin installs free; the hosted service is the product (https://www.sharingu.xyz).

## Install

```
claude plugin marketplace add ryuk-labs/sharingu-plugin
claude plugin install sharingu@sharingu
```

Inside Claude Code: `/plugin marketplace add ryuk-labs/sharingu-plugin`, then `/plugin install sharingu@sharingu`. The
first time, run `/mcp`, pick `sharingu` and sign in on sharingu's page; no key goes in your configuration.

You need a sharingu account and an org: join the beta at https://agent.sharingu.xyz/request-access.

## What is here

- [`plugin/`](plugin/) — the plugin itself: its manifest, its MCP server entry and its skills. Its
  [README](plugin/README.md) is what the plugin directories show: the four steps, the first calls, the skills.
- `.claude-plugin/marketplace.json` — this repository as its own marketplace.
- `LICENSE` — proprietary, © Ryuk Labs.

Docs: https://www.sharingu.xyz/docs.html · Privacy: https://www.sharingu.xyz/privacy.html · Support:
https://www.sharingu.xyz/support.html

## For the sharingu team: do not edit here

This repository is a DISTRIBUTION copy. It is synced from the private engine repo, `ryuk-labs/sharingu`, whose
`plugin/` folder is the source (the skills are generated from the product's starter pack by
`engine/tools/make-plugin-skills.mjs`, which also raises the version). To change the plugin: change it in the engine
repo, regenerate, then sync this repo (`node tools/make-plugin-skills.mjs --sync <this clone>`, review the diff, commit,
push). Only this README is written here by hand.
