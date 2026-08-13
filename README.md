# Comic Sol Codex Plugin

[Comic Sol](https://github.com/wenn-id/comicsol) is a local-first Codex Skill for producing original manga/anime comics from prompts, prose, or source files.

## What this plugin provides

- Editable story plans and character bibles
- Storyboards and panel prompts
- Image-generation capability detection through the active Codex session
- Per-panel visual QA and selective repair
- Deterministic lettering and page composition
- PDF export, manifest, hashes, and transparent QA evidence
- Resume-safe interrupted projects

This plugin is **skills-only**. It does not require a hosted service or MCP server. The underlying Comic Sol repository includes an optional deterministic CLI/MCP surface for local development, but this plugin exposes the Codex-native skill workflow.

The bundled skill is self-contained: its deterministic scripts, templates, references, fonts, and font licenses are included under `skills/comic-sol/`. The canonical engine repository remains the source of truth for future engine releases.

## Install from the source repository

```bash
npx skills add wenn-id/comicsol --skill comic-sol --agent codex
```

## Install through Codex plugin marketplace

```bash
codex plugin marketplace add wenn-id/comic-sol-codex-plugin
codex plugin list
codex plugin add comic-sol@comic-sol-marketplace
```

The exact plugin installation surface can vary by Codex build. The repository includes `.codex-plugin/plugin.json` and `.agents/plugins/marketplace.json` for local/repo marketplace testing.

## Use

Start a fresh Codex session after installation, then ask:

> Make a 2-page manga about a courier delivering sunlight to an underground city.

Generated projects remain local and preserve editable intermediates beneath the selected output root.

## Source

- Engine and canonical Skill: https://github.com/wenn-id/comicsol
- License: MIT
- Publisher: Alwan Juliawan

## Status

This repository is a packaging wrapper for the public Comic Sol Codex Skill. Official public Plugin Directory publication requires submission and review through OpenAI's plugin portal.
