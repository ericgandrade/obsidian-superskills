# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**obsidian-superskills** is a focused AI skills package for Obsidian knowledge management. Part of the Superskills family.

- **npm package**: `obsidian-superskills` (v1.0.1) — `npx obsidian-superskills` — **6 skills**
- **Claude Code plugin**: `claude --plugin-dir ./obsidian-superskills` — native plugin, no npm needed
- **GitHub**: `https://github.com/ericgandrade/obsidian-superskills`
- **Part of**: [claude-superskills](https://github.com/ericgandrade/claude-superskills) family

## Skills (6)

```
skills/
├── obsidian-markdown/
├── obsidian-links/
├── obsidian-frontmatter/
├── obsidian-automation/
├── obsidian-note-builder/
└── obsidian-canvas/
```

## Version Management

Current version: **v1.0.1**

Files to keep in sync:
- `cli-installer/package.json` — source of truth
- `.claude-plugin/plugin.json` — must match npm version
- `README.md` — title, badges, footer
- `CHANGELOG.md` — release notes

Use `node scripts/release.js [patch|minor|major]` to bump all files atomically.

## Development

```bash
cd cli-installer && npm install
npm link
obsidian-superskills --help
```

## Publishing

Publishing is automated via GitHub Actions on `v*` tag pushes.
```bash
git tag v1.0.1 && git push origin v1.0.1
```
