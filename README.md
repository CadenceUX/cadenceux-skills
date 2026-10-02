# CadenceUX Skills for Claris FileMaker

Claude skills for FileMaker developers from [CadenceUX](https://cadenceux.com.au), in one
plugin marketplace. Add it once, then install only the skills you need. Each skill updates
on its own when you bump to a new release.

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
| `claris-filemaker-pro` | FileMaker Pro reference — every function and script step, exact syntax, versions, platform support, Data API, OData, SQL, WebDirect, Go. Works with Claris's Agentic Development Toolkit (ADT). |
| `fmp-dev-design-patterns` | Scripting rules and conventions — error handling, variables, loops, JSON parameters |
| `fmp-dev-full-script` | Generate complete FileMaker scripts |
| `fmp-dev-orchestrator` | Routes FileMaker questions to the right installed skill |
| `monkeybread-mbs-plugin` | MBS FileMaker Plugin reference |
| `goya-be-plugin` | BaseElements Plugin reference |
| `beezwax-bbox-plugin` | bBox plugin reference |
| `cadenceux-fms-docker-setup` | FileMaker Server on Docker (macOS, Apple silicon) |
| `agentic-gate` | Referees calls between skill packs, plugins and MCP servers |

Each skill lives in its own repository (linked from `/plugin`), with its own changelog and issues.

## Works well with

**Andrew Kear's** open-source FileMaker skills from
[Clockwork Creative Technology](https://www.clockworkct.co.uk) — install them from his
repositories:

- [FileMaker-XMLsnippet-Claude-Skill](https://github.com/andykear/FileMaker-XMLsnippet-Claude-Skill) — paste-ready script XML (`filemaker-xml`)
- [FileMaker-XMLsnippet-Layout-Claude-Skill](https://github.com/andykear/FileMaker-XMLsnippet-Layout-Claude-Skill) — layout XML (`filemaker-layout-xml`)
- [FileMaker-XML-field-definitions](https://github.com/andykear/FileMaker-XML-field-definitions) — field and table XML (`filemaker-field-xml`)
- [FileMaker-AI-Grammar](https://github.com/andykear/FileMaker-AI-Grammar) — engine-measured calculation rules (`filemaker-ai-grammar`)
- [FileMaker-AI-vocabulary](https://github.com/andykear/FileMaker-AI-vocabulary) — compact function and step vocabulary (`filemaker-ai-vocabulary`)
- [FileMaker-XML-bit-flags](https://github.com/andykear/FileMaker-XML-bit-flags) — Save as XML option bit flags
- [FileMaker-XML-inspector-open-source](https://github.com/andykear/FileMaker-XML-inspector-open-source) and [FileMaker-XML-scrubber](https://github.com/andykear/FileMaker-XML-scrubber) — browser tools

And **Claris's Agentic Development Toolkit (ADT)**, which installs its own Claude plugin.

## Troubleshooting

- *"Permission denied (publickey)"* when installing: your git is trying SSH. This marketplace
  uses HTTPS URLs, so update the marketplace (`claude plugin marketplace update cadenceux`). If
  you added it as `CadenceUX/cadenceux-skills`, re-add it with the `https://` URL above, or set
  `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1`.

## Licence

Each skill carries its own licence (most are [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)).
