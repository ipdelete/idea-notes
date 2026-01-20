# Archive

Move a domain, initiative, or person to the archive folder.

## Usage

```
/archive {type} {name}
```

Where:
- `{type}` is one of: `person`, `domain`, `initiative`
- `{name}` is the name used when creating it (lowercase, hyphens)

Examples:
- `/archive person jane-doe`
- `/archive domain finances`
- `/archive initiative mobile-app`

## Instructions

When this command is run:

1. Identify the source locations based on type:
   - `person`: folder at `domains/people/{name}/`, command at `.opencode/commands/person-{name}.md`
   - `domain`: folder at `domains/{name}/`, command at `.opencode/commands/domain-{name}.md`
   - `initiative`: folder at `initiatives/{name}/`, command at `.opencode/commands/initiative-{name}.md`

2. Move the folder to `archive/{type}/{name}/`

3. Delete the associated command file from `.opencode/commands/`

4. Confirm what was archived and removed
