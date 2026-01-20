# Meta Initiative Command

Create a new initiative command for tracking notes about a specific project.

## Usage

```
/meta-initiative {name}
```

Where `{name}` is the project name (lowercase, no spaces - use hyphens if needed).

## Instructions

When this command is run with a project name:

1. Create a new command file at `.opencode/commands/initiative-{name}.md` with the following content:

```markdown
# Initiative: {Name}

Take notes about {Name}.

## Instructions

When this command is run:

1. Create the folder `initiatives/{name}/` if it doesn't exist
2. Create a new markdown file with the current date and time as the filename in format `YYYYMMDD-HHMM.md` (e.g., `20260120-1430.md`)
3. Add the following template to the file:

```
# {Name} - {Date} {Time}

## Notes



## Decisions



## Next Steps


```

4. Ask me what I'd like to note about {Name} and add my response to the Notes section
```

2. Confirm the command was created and show how to use it: `/initiative-{name}`
