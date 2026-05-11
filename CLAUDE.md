# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**obsidian-superskills** is a focused AI skills package for Obsidian knowledge management. Part of the Superskills family.

- **npm package**: `obsidian-superskills` (v1.0.3) — `npx obsidian-superskills` — **6 skills**
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

Current version: **v1.0.3**

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
git tag v1.0.3 && git push origin v1.0.3
```

## Language

All content in this repository — code comments, documentation, commit messages, skill files, and AI instructions — must be written in **English**. No Portuguese or any other language.

## graphify

This project has a graphify knowledge graph at graphify-out/.

Rules:
- Before answering architecture or codebase questions, read graphify-out/GRAPH_REPORT.md for god nodes and community structure
- If graphify-out/wiki/index.md exists, navigate it instead of reading raw files
- After modifying code files in this session, run `graphify update .` to keep the graph current (AST-only, no API cost)
- **After any important change, run `/graphify --update` before ending the session.** Important changes include: adding or removing a skill, modifying SKILL.md or README.md of any skill, bumping version, or any structural refactor. Do not skip this step — an outdated graph leads to stale answers in future sessions.
