# HeyGent Skills Marketplace

The Claude Code plugin marketplace for everything HeyGent publishes. This repo holds only the
marketplace manifest; each plugin lives in its own repository.

## Add the marketplace (once)

Open a terminal (not a Claude chat) and run:

```bash
claude plugin marketplace add heygents/heygent-skills
```

## Plugins

| Plugin | Install | What it is |
|---|---|---|
| [heygent-pm-skills](https://github.com/heygents/heygent-pm-skills) | `claude plugin install heygent-pm-skills@heygent` | 19 PM workflow skills: customer discovery → planning → PRD → tech plan → review → learn, competitor analysis, knowledge ingest, Mixpanel analysis, bring-your-own design system. |
| [ayal-doron-methodology-skills](https://github.com/heygents/ayal-doron-methodology-skills) | `claude plugin install ayal-doron-methodology-skills@heygent` | Dr. Ayal Doron's "unreplaceable" toolbox as 7 skills: challenge intake, the irreplaceable anchor, four tools for inventing a new playing field, habit infrastructure. |

## Update

```bash
claude plugin marketplace update heygent
```

```bash
claude plugin update <plugin-name>@heygent
```

## Migrating from the old marketplace location

Before September 2026 the marketplace manifest lived inside the `heygent-pm-skills` repo. If you added it
from there, switch once (installed plugins stay installed; only their update source changes):

```bash
claude plugin marketplace remove heygent && claude plugin marketplace add heygents/heygent-skills
```

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json` pointing at the plugin's git URL, then push. Users get it on
their next `claude plugin marketplace update heygent`.
