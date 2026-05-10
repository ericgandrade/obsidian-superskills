# 🧠 Obsidian Superskills v1.0.1

Master Obsidian knowledge management with AI-powered skills for notes, wikilinks, frontmatter, automation, and canvas. Install once across all 8 AI platforms.

![Version](https://img.shields.io/badge/version-1.0.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Skills](https://img.shields.io/badge/skills-6-brightgreen.svg)
![Platforms](https://img.shields.io/badge/platforms-8-orange.svg)

## 🚀 Quick Install

**One-liner (recommended):**
```bash
curl -fsSL https://raw.githubusercontent.com/ericgandrade/obsidian-superskills/main/scripts/install.sh | bash
```

**Or use NPX (zero-install):**
```bash
npx obsidian-superskills
```

The installer detects and installs to all 8 AI platforms on your machine: Claude Code, GitHub Copilot, OpenAI Codex, OpenCode, Gemini CLI, Antigravity, Cursor IDE, AdaL CLI.

**Other methods:**
```bash
# npm global
npm install -g obsidian-superskills

# With bundles
npx obsidian-superskills --bundle all -y
```

**Local install (no npm/npx required):**
```bash
git clone https://github.com/ericgandrade/obsidian-superskills
cd obsidian-superskills

./scripts/local-install.sh        # Interactive
./scripts/local-install.sh -y     # Auto-install to all detected platforms
./scripts/local-install.sh -y -q  # Silent (CI / scripted)
```

**Uninstall:**
```bash
curl -fsSL https://raw.githubusercontent.com/ericgandrade/obsidian-superskills/main/scripts/uninstall.sh | bash
```

## 🔌 Claude Code Plugin (Native)

Requires **Claude Code v1.0.33+** (`claude --version` to check).

**Method 1: Interactive UI (Inside a running `claude` session) — Recommended**

```text
/plugin marketplace add ericgandrade/obsidian-superskills
/plugin install obsidian-superskills@obsidian-superskills
```

**Method 2: Local test (no install needed)**

```bash
git clone https://github.com/ericgandrade/obsidian-superskills
claude --plugin-dir ./obsidian-superskills
```

### Once installed — all 6 skills under the `obsidian-superskills:` namespace

```
/obsidian-superskills:obsidian-markdown
/obsidian-superskills:obsidian-links
/obsidian-superskills:obsidian-frontmatter
/obsidian-superskills:obsidian-automation
/obsidian-superskills:obsidian-note-builder
/obsidian-superskills:obsidian-canvas
```

## ✨ Features

- **6 Obsidian-Specific Skills** - Deep vault integration
- **Zero-Config Install** - Run once, works everywhere
- **8 Platform Support** - GitHub Copilot, Claude Code, Codex, OpenCode, Gemini, Antigravity, Cursor, AdaL
- **No API Keys Required** - All skills run natively in your AI tool

## 📦 Available Skills

| Skill | Version | Purpose |
|-------|---------|---------|
| **obsidian-markdown** | v1.0.1 | Create and edit notes using Obsidian Flavored Markdown — wikilinks, callouts, embeds, block references, and all Obsidian-specific syntax |
| **obsidian-links** | v1.0.1 | Create, validate, repair, and analyze wikilinks inside an Obsidian vault — broken link detection, orphan discovery, auto-linking, and MOC builder |
| **obsidian-frontmatter** | v1.0.1 | Create, validate, standardize, and repair YAML frontmatter — tags, aliases, dates, custom fields — for Dataview-compatible notes |
| **obsidian-automation** | v1.0.1 | Automate vault tasks using the CLI, shell scripts, and Local REST API — batch note creation, bulk frontmatter updates, and vault maintenance |
| **obsidian-note-builder** | v1.0.1 | Build complete, knowledge-graph-ready notes from raw content with entity extraction, auto-wikilinks, and Zettelkasten atomicity |
| **obsidian-canvas** | v1.0.1 | Create freeform visual workspaces using Obsidian Canvas — hub-and-spoke, Kanban, and dashboard layouts as ready-to-save `.canvas` files |

## 🎯 Bundles

```bash
# All Obsidian Skills (complete collection)
npx obsidian-superskills --bundle all -y
```

## 🚀 Quick Start Examples

```bash
# Build a knowledge-graph-ready note from raw content
claude -p "build an obsidian note from these meeting notes: ..."

# Find and repair broken wikilinks in the vault
claude -p "find broken links in my vault and fix them"

# Create a Canvas dashboard for a project
claude -p "create an obsidian canvas for my Q2 planning project"

# Batch-update frontmatter across multiple notes
claude -p "add tag: project-x to all notes in the 03-projects/ folder"
```

## 💻 Supported Platforms

- **GitHub Copilot CLI** - Terminal AI assistant (`~/.github/skills/`)
- **Claude Code** - Anthropic's Claude in development (`~/.claude/skills/`)
- **OpenAI Codex** - GPT-powered coding assistant (`~/.codex/skills/`)
- **OpenCode** - Open source AI coding assistant (`~/.agent/skills/`)
- **Gemini CLI** - Google's Gemini in terminal (`~/.gemini/skills/`)
- **Antigravity** - AI coding assistant (`~/.gemini/antigravity/skills/`)
- **Cursor IDE** - AI-powered code editor (`~/.cursor/skills/`)
- **AdaL CLI** - AI development assistant (`~/.adal/skills/`)

## ⌨️ Compatibility & Invocation

| Tool | Type | Invocation Example | Path |
|------|------|--------------------|------|
| **Claude Code** | CLI | `/obsidian-markdown help me...` | `~/.claude/skills/` |
| **Gemini CLI** | CLI | `Use obsidian-links to...` | `~/.gemini/skills/` |
| **Codex CLI** | CLI | `Use obsidian-frontmatter to...` | `~/.codex/skills/` |
| **Antigravity** | IDE | *(Agent Mode)* `Use skill...` | `~/.gemini/antigravity/skills/` |
| **Cursor** | IDE | `@obsidian-note-builder` in Chat | `~/.cursor/skills/` |
| **Copilot** | Ext | *(Paste skill content manually)* | N/A |
| **OpenCode** | CLI | `opencode run @obsidian-canvas` | `~/.agent/skills/` |
| **AdaL CLI** | CLI | *(Auto)* Skills load on-demand | `~/.adal/skills/` |

## ⚡ CLI Commands & Shortcuts

| Command | Shortcut | Purpose |
|---------|----------|---------|
| `install` | `i` | Install skills |
| `list` | `ls` | List installed skills |
| `status` | `st` | Show global install status + version differences |
| `update` | `up` | Smart update (outdated + missing skills) |
| `uninstall` | `rm` | Remove skills |
| `doctor` | `doc` | Check installation |

```bash
npx obsidian-superskills i -a -y -q    # Install all, skip prompts, quiet mode
npx obsidian-superskills status         # Show global status + skill version differences
npx obsidian-superskills up -y          # Update outdated + install missing skills
npx obsidian-superskills ls -q          # List with minimal output
npx obsidian-superskills --list-bundles # Show available bundles
```

## 📋 System Requirements

- Node.js 14+ (for installer)
- One or more supported platforms installed
- Obsidian installed (for vault-specific features)

## 🔒 Privacy

obsidian-superskills does not collect, store, transmit, or share any user data.

- **No external servers** — no backend, no telemetry, no network requests of its own
- **No API keys required** — all skills run within your AI tool using native tools
- **No logging** — nothing is recorded outside of your local session
- **Open source** — all skill logic is fully auditable

## 📄 License

MIT - See [LICENSE](./LICENSE) for details.

## 🔗 Quick Links

- 📝 [Changelog](CHANGELOG.md) - Release history
- 🐛 [Issues](https://github.com/ericgandrade/obsidian-superskills/issues) - Report problems

## Part of the Superskills Family

| Package | Skills | Focus | Install |
|---------|--------|-------|---------|
| [claude-superskills](https://github.com/ericgandrade/claude-superskills) | 18 | Core: orchestration, planning, research & content | `npx claude-superskills` |
| **obsidian-superskills** | 6 | Obsidian knowledge management | `npx obsidian-superskills` |
| [career-superskills](https://github.com/ericgandrade/career-superskills) | 20 | Job search & career development | `npx career-superskills` |
| [product-superskills](https://github.com/ericgandrade/product-superskills) | 8 | Product management & GTM strategy | `npx product-superskills` |
| [design-superskills](https://github.com/ericgandrade/design-superskills) | 9 | UI/UX design, brand & diagrams | `npx design-superskills` |
| [avanade-superskills](https://github.com/ericgandrade/avanade-superskills) | 3 | Avanade-branded content (private) | `git clone git@github.com:ericgandrade/avanade-superskills.git` |

---

**Built with ❤️ by [Eric Andrade](https://github.com/ericgandrade)**

*Version 1.0.1 | May 2026*
