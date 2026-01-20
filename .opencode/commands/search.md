# Search

Search across all notes.

## Usage

```
/search {query}
```

Examples:
- `/search API design`
- `/search project timeline`
- `/search rust lifetimes`

## Instructions

When this command is run:

1. Search for `{query}` across all markdown files in:
   - `domains/`
   - `initiatives/`
   - `expertise/`
   - `inbox/`
   - `archive/`
2. Show results grouped by location with:
   - File path
   - Matching line(s) with context
3. If no results found, say "No notes found matching '{query}'"
