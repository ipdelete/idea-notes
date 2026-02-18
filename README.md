# IDEA Notes

Personal knowledge management using the IDEA method, powered by [GitHub Copilot CLI](https://docs.github.com/en/copilot/github-copilot-in-the-cli).

## What is this?

An AI-powered personal knowledge management system. Notes are stored as plain markdown files and managed through natural language conversation with GitHub Copilot CLI. Fork this repo to get started.

For the full setup guide — including private/public publishing — see [Setting Up an AI-Powered Private/Public Note-Taking System](https://github.com/ianphil/public-notes/blob/main/expertise/IDEA-notes-setup.md).

## The IDEA Method

| Folder | Purpose |
|--------|---------|
| **I**nitiatives | Projects with a defined end goal |
| **D**omains | Recurring areas of responsibility |
| **E**xpertise | Notes about things you learn |
| **A**rchive | Completed or inactive items |
| **inbox** | Quick capture for notes to classify later |

## Getting Started

1. Fork this repo (make it **private**)
2. Install [GitHub Copilot CLI](https://docs.github.com/en/copilot/github-copilot-in-the-cli)
3. Start taking notes by talking to Copilot

## Skills

Skills are small instruction files in `.github/skills/` that teach Copilot your vault's workflows. This repo includes:

| Skill | What it does |
|-------|-------------|
| `capture-triage` | Quick capture notes, list inbox, classify into IDEA folders |
| `entity-notes` | Create new initiative/domain/expertise/person folders with templates |
| `next-actions` | Manage per-entity task lists with open/done sections |
| `discovery` | Search notes and list recently modified files |
| `links` | Suggest and add wiki-style links between notes |
| `lifecycle` | Archive completed entities, commit and push |
| `daily-report` | Generate a daily briefing from your notes |

### Example Conversations

**Quick capture:**
```
> note jane-doe Met for coffee, discussed timeline
  → creates entry in domains/people/jane-doe/

> note mobile-app Decided to use React Native
  → creates entry in initiatives/mobile-app/

> note Remember to review budget
  → lands in inbox/ (no match found)
```

**Triage inbox:**
```
> inbox
  3 notes waiting...

> classify 20260120-0915-budget.md domain finances
  → moved to domains/finances/
```

**Manage tasks:**
```
> next-action add initiative mobile-app Write the API spec
> next-action list initiative mobile-app
> next-action done initiative mobile-app 1
```

**Search and discover:**
```
> search React Native
> recent
```

## File Naming

- **Default:** `YYYYMMDD-HHMM.md` (e.g., `20260120-1430.md`)
- **Inbox:** `YYYYMMDD-HHMM-{slug}.md` where slug is derived from content

## Sample Content

This repo includes sample notes to demonstrate the system:

- **Initiatives:** `mobile-app` — a sample project with meeting notes
- **Domains:** `people/jane-doe` — a sample person, `finances` — a sample domain
- **Expertise:** `rust` — sample learning notes
- **Inbox:** Sample notes waiting to be classified

## Learn More

- [Full setup tutorial](https://github.com/ianphil/public-notes/blob/main/expertise/IDEA-notes-setup.md) — private repo, public publishing, skills, daily workflow
- [GitHub Copilot CLI docs](https://docs.github.com/en/copilot/github-copilot-in-the-cli)
