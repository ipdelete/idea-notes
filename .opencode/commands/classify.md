# Classify

Move an inbox note to the right location.

## Usage

```
/classify {filename} {type} {name}
```

Where:
- `{filename}` is the inbox file (e.g., `20260120-1755-buy-groceries.md`)
- `{type}` is one of: `person`, `domain`, `initiative`, `expertise`
- `{name}` is the target name (lowercase, hyphens)

Examples:
- `/classify 20260120-1755-meeting-notes.md person jane-doe`
- `/classify 20260120-1800-api-idea.md initiative mobile-app`
- `/classify 20260120-1805-rust-tip.md expertise rust`

## Instructions

When this command is run:

1. Verify the file exists in `inbox/`
2. Determine the destination based on type:
   - `person`: `domains/people/{name}/`
   - `domain`: `domains/{name}/`
   - `initiative`: `initiatives/{name}/`
   - `expertise`: `expertise/{name}/`
3. Create the destination folder if it doesn't exist
4. Move the file to the destination, renaming to `YYYYMMDD-HHMM.md` format (extract from original filename)
5. Confirm the move: "Moved {filename} to {destination}"
