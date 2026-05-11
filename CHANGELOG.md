# Changelog

All notable changes to obsidian-superskills are documented in this file.

## [1.0.1] - 2026-05-10

### Fixed
- Remove dangerous fallback in `uninstallManagedSkills()` that could delete skills from other packages
- Delete dead code `lib/commands/uninstall.js`

### Added
- Nuclear uninstall option (`--nuclear` flag and interactive menu choice) with type-to-confirm safety gate

---

## [1.0.2] - 2026-05-11

### Added
- New features...



## [1.0.0] - 2026-05-08

### Added
- Initial release — 6 Obsidian knowledge management skills carved out from claude-superskills v1.25.1
- obsidian-markdown: Creates well-structured Obsidian notes with proper formatting
- obsidian-links: Manages wikilinks and knowledge graph connections
- obsidian-frontmatter: Standardizes and validates frontmatter properties
- obsidian-automation: Automates vault tasks via CLI scripts
- obsidian-note-builder: Builds structured notes from raw content or templates
- obsidian-canvas: Creates visual workspaces with Obsidian Canvas
