# sharingu for Claude Code

The sharingu plugin: one MCP server, the platform's address `https://agent.sharingu.xyz/mcp`, and the sharingu starter
pack as skills. The docs: https://www.sharingu.xyz/docs.html.

## Install

This repository is its own marketplace (`.claude-plugin/marketplace.json` at its root lists this folder). In a terminal:

```
claude plugin marketplace add ryukdev/sharingu-plugin
claude plugin install sharingu@sharingu
```

or inside Claude Code, `/plugin marketplace add ryukdev/sharingu-plugin`, then `/plugin install sharingu@sharingu`. A local
clone works the same way: `claude plugin marketplace add <path to the clone>`.

## What connects where

The plugin adds one MCP server, `sharingu`, at `https://agent.sharingu.xyz/mcp`. It carries no key. The first time,
run `/mcp`, pick `sharingu` and sign in on the platform's page. Signed in with your account's passphrase, the connection
reaches every org your account has a seat in; with a seat's key, that seat alone. You need an account first: the
operator's sign-up code, then `https://agent.sharingu.xyz/signup`.

## The first time, in order

1. `whoami`: your name, your orgs and projects, and where your writes land;
2. `missing` with `project`: what that project still needs, each item with the call that fills it;
3. `preview`: every write, shown before it lands (`formats` gives each kind's shape);
4. `file` with the `previewId` and the same items: it files them, and the app shows them at once.

The skill `fill-a-project` walks a new project through these calls to its first filed contribution.

## The skills

`skills/` holds one skill per starter item of the product, generated from the product's own starter pack: an edit here
is overwritten by the next release.

## License

sharingu is proprietary software, © Ryuk Labs (`LICENSE` at the repository root). The plugin installs free; the hosted
service is the product.
