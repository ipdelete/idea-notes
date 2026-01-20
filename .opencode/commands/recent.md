# Recent

Show recently modified notes.

## Usage

```
/recent
```

Or with a limit:
```
/recent {n}
```

Examples:
- `/recent` - shows last 10 notes
- `/recent 20` - shows last 20 notes

## Instructions

When this command is run:

1. Find all markdown files across:
   - `domains/`
   - `initiatives/`
   - `expertise/`
   - `inbox/`
2. Sort by modification time (most recent first)
3. Show the top N results (default 10) with:
   - File path
   - Title (first heading or first line)
   - Last modified date/time
4. Exclude archive from results (those are intentionally inactive)
