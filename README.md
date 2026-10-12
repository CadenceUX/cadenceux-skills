# CadenceUX Skills for Claris FileMaker

Claude skills for FileMaker developers from [CadenceUX](https://cadenceux.com.au), in one
plugin marketplace. Add it once, then install only the skills you need. Each skill updates on
its own when a new release ships.

Built to work with the **Claris Agentic Development Toolkit (ADT)**: with ADT installed, Claude
reads and changes your FileMaker file directly (schema, scripts, layouts), so there's no
clipboard XML and no copy and paste. These skills add the verified reference, conventions and
operations knowledge ADT doesn't carry.

Built and maintained by [Darrin Southern](https://www.linkedin.com/in/darrin-southern/).

## Install

**Claude Code** (terminal, desktop app Code tab, VS Code):

```bash
claude plugin marketplace add https://github.com/CadenceUX/cadenceux-skills.git
claude plugin install claris-filemaker-pro@cadenceux
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
| `claris-filemaker-pro` | FileMaker Pro reference: every function and script step with exact syntax, versions and platform support, plus Data API, OData, SQL, WebDirect and Go. Defers to ADT's engine when installed. |
| `fmp-dev-design-patterns` | Scripting conventions and patterns: error handling, JSON parameters, transactions, AI steps, naming and anti-patterns. Writes scripts into the file through ADT. |
| `fmp-dev-orchestrator` | Routes each FileMaker topic to the skill or tool that owns it, ADT included. |
| `cadenceux-fms-docker-setup` | FileMaker Server on Docker (macOS, Apple silicon): install, certificates, upgrades and rollback. |
| `cadenceux-ottofms-docker-setup` | OttoFMS on a Docker-hosted FileMaker Server: install and activation. |
| `monkeybread-mbs-plugin` | MBS FileMaker Plugin reference. |
| `goya-be-plugin` | BaseElements plug-in reference. |
| `beezwax-bbox-plugin` | bBox plug-in reference. |
| `cadenceux-skill-creator` | Builds, updates and reviews Claude skills to Anthropic's best practices: evals first, a validator script, Haiku/Sonnet/Opus testing and release packaging. |

Each skill lives in its own repository (linked from `/plugin`), with its own changelog and issues.

**Staying current.** [`versions.json`](versions.json) lists each skill's latest release and the
toolchain the set was last tested with (FileMaker Server and plugin versions).
`fmp-dev-orchestrator` reads it once per session and reports anything out of date, including
Claris ADT, the FileMaker Pro version ADT needs, and your ADT project's packages, all read
from your own install. It's read-only.

**Retired in October 2026:** `fmp-dev-full-script` (clipboard XML script generation, replaced
by ADT) and `agentic-gate`. Their repositories are archived.

## Troubleshooting

- *"Permission denied (publickey)"* when installing: your git is trying SSH. This marketplace
  uses HTTPS URLs, so update the marketplace (`claude plugin marketplace update cadenceux`). If
  you added it as `CadenceUX/cadenceux-skills`, re-add it with the `https://` URL above, or set
  `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1`.
- A retired skill still showing after an update: uninstall it with
  `claude plugin uninstall fmp-dev-full-script@cadenceux` (or `agentic-gate@cadenceux`).

## Licence

Each skill carries its own licence (CC BY 4.0).
