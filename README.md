# IDEA Notes

Personal knowledge management using the IDEA method, powered by [OpenCode](https://opencode.ai).

## What is this?

An AI-augmented personal knowledge management system. Notes are stored as plain markdown files (compatible with Obsidian) and managed through natural language commands via OpenCode.

## The IDEA Method

| Folder | Purpose |
|--------|---------|
| **I**nitiatives | Projects with a defined end goal |
| **D**omains | Recurring areas of responsibility |
| **E**xpertise | Notes about things you learn |
| **A**rchive | Completed or inactive items |
| **inbox** | Quick capture for notes to classify later |

## Getting Started

1. Clone this repo
2. Open with [OpenCode](https://opencode.ai)
3. Start taking notes!

## Commands

### Create Tracking Areas (Meta Commands)

These create dedicated slash commands for tracking specific topics:

| Command | Creates |
|---------|---------|
| `/meta-person {name}` | `/person-{name}` command + folder |
| `/meta-domain {name}` | `/domain-{name}` command + folder |
| `/meta-initiative {name}` | `/initiative-{name}` command + folder |
| `/meta-expertise {name}` | `/expertise-{name}` command + folder |

**Example:** `/meta-person jane-doe` creates:
- Folder: `domains/people/jane-doe/`
- Command: `/person-jane-doe`

### Quick Capture

```
/note {target} {content}
```

Auto-routes notes to matching folders or inbox:
- `/note jane-doe Met for coffee, discussed timeline` → goes to person folder
- `/note mobile-app Decided to use React Native` → goes to initiative folder
- `/note rust Learned about lifetimes` → goes to expertise folder
- `/note Remember to review budget` → goes to inbox (no target match)

### Triage

| Command | Description |
|---------|-------------|
| `/inbox` | List all notes waiting to be classified |
| `/classify {file} {type} {name}` | Move inbox note to proper location |

**Types for classify:** `person`, `domain`, `initiative`, `expertise`

### Discovery

| Command | Description |
|---------|-------------|
| `/search {query}` | Search across all notes |
| `/recent` | Show 10 most recently modified notes |
| `/recent {n}` | Show last N modified notes |

### Lifecycle

| Command | Description |
|---------|-------------|
| `/archive {type} {name}` | Move folder and command to archive |
| `/ship` | Git add, commit, and push all changes |

## File Naming Convention

Notes are created with timestamp-based filenames:
- **Format:** `YYYYMMDD-HHMM.md` (e.g., `20260120-1430.md`)
- **Inbox notes:** `YYYYMMDD-HHMM-{slug}.md` where slug is derived from content

## Quick Start Workflow

1. **Create a tracking area:** `/meta-person jane-doe`
2. **Take notes:** `/person-jane-doe` or `/note jane-doe discussed project timeline`
3. **Quick capture:** `/note need to review budget proposal` (goes to inbox)
4. **Triage inbox:** `/inbox` then `/classify 20260120-1755-budget.md domain finances`
5. **Find notes:** `/search budget` or `/recent`
6. **Archive when done:** `/archive initiative old-project`
7. **Save to git:** `/ship`

## Sample Content

This repo includes sample notes demonstrating the system:

- **Initiatives:** `mobile-app` - A sample project
- **Domains:** `people/jane-doe` - A sample person, `finances` - A sample domain
- **Expertise:** `rust` - A sample learning topic
- **Inbox:** Sample notes waiting to be classified
