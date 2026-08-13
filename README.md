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

This plugin is **skills-only**. It requires no hosted service or MCP server. The
bundled workflow uses the image-generation capability exposed by the active Codex
session and runs deterministic local scripts for validation and export.

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

The repository includes `.codex-plugin/plugin.json` and `.agents/plugins/marketplace.json`
for local/repo marketplace testing.

## Use

Start a fresh Codex session after installation, then ask:

> Make a 2-page manga about a courier delivering sunlight to an underground city.

Generated projects remain local and preserve editable intermediates beneath the selected output root.

## Source

- Engine and canonical Skill: https://github.com/wenn-id/comicsol
- License: MIT
- Publisher: Alwan Juliawan

## Legal and support

- Privacy: [PRIVACY.md](PRIVACY.md)
- Terms: [TERMS.md](TERMS.md)
- Support: [SUPPORT.md](SUPPORT.md)
- Submission materials: [submission/](submission/)

## Status

This repository is a packaging wrapper for the public Comic Sol Codex Skill.
It is tested through a repo marketplace. Universal public Plugin Directory
publication still requires the OpenAI submission portal, verified developer
identity, Apps Management write access, and OpenAI review.
