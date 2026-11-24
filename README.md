# CadenceUX Skills for Claris FileMaker

Claude skills for FileMaker developers from [CadenceUX](https://cadenceux.com.au), in one
plugin marketplace. Add it once, then install only the skills you need. Each skill updates on
its own when a new release ships.

Built to work with Claris's **FileMaker Agentic Development Kit (ADK)**: with ADK installed
(FileMaker Pro 26.1 or later), Claude reads and changes your FileMaker file directly (schema,
scripts, layouts), so there's no clipboard XML and no copy and paste. These skills add the
verified reference, conventions, decisions and operations knowledge ADK doesn't carry, and they
work without ADK too.

Built and maintained by [Darrin Southern](https://www.linkedin.com/in/darrin-southern/).

## Install

**Claude Code** (terminal, desktop app Code tab, VS Code):

```bash
claude plugin marketplace add https://github.com/CadenceUX/cadenceux-skills.git
claude plugin install cadenceux-dx@cadenceux
```

Or inside a session: `/plugin marketplace add https://github.com/CadenceUX/cadenceux-skills.git`,
then pick skills from `/plugin`.

**claude.ai and Cowork** (web, desktop and mobile chat): **Customize → Plugins → Add →
marketplace from GitHub**, enter `CadenceUX/cadenceux-skills`, then install the skills you want.
Plugins you install on claude.ai also appear in Claude Code.

Updates: run `claude plugin update`, or turn on auto-update for the `cadenceux` marketplace.

## Skills

| Skill | What it does |
|---|---|
| `cadenceux-dx` | Start here. Routes each FileMaker task to the skill or ADK tool that owns it, checks your stack is current, and guides the decisions around the code: native or web viewer, data access, FileMaker 26.0.3 and earlier, reviews, linter tests, security and deployment. |
| `claris-filemaker-pro` | FileMaker Pro reference, current to 26.1: every function and script step with exact syntax, versions and platform support, plus Data API, OData, SQL, WebDirect and Go. Defers to ADK's engine when installed. |
| `fmp-dev-design-patterns` | Scripting conventions and patterns: error handling, JSON parameters, transactions, AI steps, naming and anti-patterns. Applies the `cadenceux` standards pack, through ADK or without it. |
| `cadenceux-filemaker-standards` | The `cadenceux` standards pack for ADK (a plugin, not a skill): `adk standards use cadenceux`. |
| `cadenceux-fms-docker-setup` | FileMaker Server on Docker (macOS, Apple silicon): install, certificates, upgrades and rollback. |
| `cadenceux-ottofms-docker-setup` | OttoFMS on a Docker-hosted FileMaker Server: install and activation. |
| `monkeybread-mbs-plugin` | MBS FileMaker Plugin reference. |
| `goya-be-plugin` | BaseElements plug-in reference. |
| `beezwax-bbox-plugin` | bBox plug-in reference. |
| `cadenceux-fms-security` | Security check of a FileMaker Server you manage: exposure, CVEs, accounts, logs (several servers together) and backups. |
| `cadenceux-github` | Sharing skills on GitHub safely, checking accounts and repos for known attacks, and scanning skills before you install them. |
| `cadenceux-skill-creator` | Builds, updates and reviews Claude skills to Anthropic's best practices: evals first, a validator script, Haiku/Sonnet/Opus testing and release packaging. |

Each skill lives in its own repository (linked from `/plugin`), with its own changelog and issues.

**Staying current.** [`versions.json`](versions.json) lists each skill's latest release and the
toolchain the set was last tested with (FileMaker Server and plugin versions).
`cadenceux-dx` reads it once per session and reports anything out of date, including Claris
ADK, the FileMaker Pro version ADK needs, and your ADK project's standards pack and packages,
all read from your own install. It's read-only.

**Same skill, two names:** `fmp-dev-orchestrator` is `cadenceux-dx` under its earlier name,
built from the cadenceux-dx repo so existing installs and links keep working. Install one.

**Retired:** `fmp-dev-full-script` (clipboard XML script generation, replaced by
ADK) and `agentic-gate` (October 2026; their repositories were deleted in November 2026).

## Troubleshooting

- *"Permission denied (publickey)"* when installing: your git is trying SSH. This marketplace
  uses HTTPS URLs, so update the marketplace (`claude plugin marketplace update cadenceux`). If
  you added it as `CadenceUX/cadenceux-skills`, re-add it with the `https://` URL above, or set
  `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1`.
- A retired skill still showing after an update: uninstall it with
  `claude plugin uninstall fmp-dev-full-script@cadenceux` (or `agentic-gate@cadenceux`).

## Licence

Each skill carries its own licence (CC BY 4.0).
