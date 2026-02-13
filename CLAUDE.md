# CLAUDE.md

## Project Overview

**ai-logs** is a personal knowledge management repository for collecting, organizing, and archiving AI conversation transcripts from multiple platforms (Claude, ChatGPT, Gemini, etc.). The content is primarily in Japanese. The long-term goal is fully automated, "button-less" log harvesting and organization integrated with Obsidian.

This is a **documentation/logs repository**, not a software project. There is no source code, build system, or test suite.

## Repository Structure

```
/
├── CLAUDE.md                    # This file — guidance for AI assistants
├── README.md                    # Project stub
├── YYYY-MM-DD_Platform_Title.md # AI conversation logs (primary content)
└── platform_log_YYYY-MM-DD.md  # Alternate naming for some logs
```

All log files live at the root level. There are no subdirectories for content.

## File Naming Conventions

Two patterns are used for log files:

| Pattern | Example |
|---|---|
| `YYYY-MM-DD_Platform_Description.md` | `2026-01-19_Gemini_AIログ整理システム構築ガイド.md` |
| `platform_log_YYYY-MM-DD.md` | `gemini_log_2026-01-29.md` |

The **preferred** convention is `YYYY-MM-DD_Platform_Description.md`. Platform names should match one of: `ChatGPT`, `Claude`, `Gemini`.

## Content Conventions

- **Language:** Japanese (all content is written in Japanese)
- **Format:** Markdown with optional YAML front-matter metadata
- **Front-matter fields (when present):** `date`, `AI platform`, `tags`, `URL`
- **Conversation format:** `User: ...` / `AI: ...` style, or summarized notes

## External Tools & Ecosystem

This repository is part of a broader automation pipeline:

| Tool | Role |
|---|---|
| **Obsidian** | Central knowledge base where logs are ultimately stored and browsed |
| **Obsidian Web Clipper** | Browser extension for template-based saving of AI conversations |
| **Python scripts** | Organization/sorting automation (`~/Scripts/ObsidianOrganizer/organize.py`) |
| **Manus AI agent** | Fully automated conversation harvesting from AI platforms |
| **Cron jobs** | Scheduled execution of collection/organization scripts |

## Development Workflow

Since this is a documentation repository, "development" means adding or organizing log files:

1. AI conversations are captured (manually or via automation)
2. Logs are formatted as Markdown following the naming conventions above
3. Files are committed to this repository
4. Obsidian or scripts may further organize the content

## Guidelines for AI Assistants

- **Preserve Japanese content.** All existing documentation is in Japanese — do not translate or alter it unless asked.
- **Follow naming conventions.** When creating new log files, use the `YYYY-MM-DD_Platform_Description.md` pattern.
- **Keep files at root level.** Do not create subdirectories for content unless explicitly requested.
- **Include front-matter when appropriate.** New log files should include YAML front-matter with `date`, `AI platform`, and `tags` fields.
- **Minimal README.** The README.md is intentionally minimal; do not expand it without being asked.
- **No build/test/lint tooling exists.** There are no commands to run for validation. Changes are purely content-based.

## Git Practices

- Commit messages should be concise and descriptive
- The repository uses SSH-based commit signing
- Historical commit authors include `array0224-cloud` and `Manus AI`
