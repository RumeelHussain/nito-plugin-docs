# Nito Plugin Documentation

Documentation site for the **Nito plugin**, the incognito privacy layer for Claude Code and Codex. It covers installing the plugin, the in-chat commands (`/nito:` in Claude Code, `$nito:` in Codex), the `nito` CLI, privacy tiers, plans, and help.

Built with [Mintlify](https://mintlify.com).

## Local Development

You need [Node.js](https://nodejs.org) and the Mintlify CLI:

```bash
npm i -g mintlify
```

From the repository root (where `docs.json` lives), start the local preview:

```bash
mintlify dev
```

This serves the site at `http://localhost:3000` (or the next free port) and reloads as you edit.

## Structure

Navigation is defined in [`docs.json`](docs.json). The content is organized into tabs:

| Tab | Folder | What it covers |
| :-- | :-- | :-- |
| Get Started | `get-started/` | What the plugin is, install (Claude Code and Codex), first steps |
| Commands | `commands/` | Every in-chat command: ask, private, fusion, session, and more |
| Models | `models/` | The model catalog, defaults, and privacy reach |
| Privacy | `privacy/` | The four privacy tiers, what each command protects, attestation |
| Plans and Billing | `plans/` | Free usage, what paid unlocks, checking usage, upgrading |
| CLI | `cli/` | Running Nito from the terminal, session launchers, health checks |
| Help | `help/` | Troubleshooting and FAQ |

Brand assets live in `images/`, custom styles in `style.css`.

## Editing

- Pages are MDX files. Add a page by creating the `.mdx` file and listing it under the right group in `docs.json`.
- Each page starts with frontmatter (`title`, `description`).
- Keep links as absolute doc paths (for example `/commands/private`).

## Deployment

The site deploys through the Mintlify GitHub app. Install it on this repository and point it at the default branch; Mintlify builds from `docs.json` on every push. Use the standard GitHub integration rather than the AI site-generation flow.
