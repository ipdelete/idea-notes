# Note

Quick capture for notes, routed to the right location.

## Usage

```
/note {target} {content}
```

Examples:
- `/note jane-doe Met for coffee, discussed the project timeline`
- `/note mobile-app Decided to use React Native instead of Flutter`
- `/note rust Learned about lifetimes today`
- `/note Remember to review the quarterly report`

## Instructions

When this command is run:

1. Parse the input to identify a potential target and content
2. Search for a matching location:
   - `domains/people/{target}/` - for people
   - `initiatives/{target}/` - for projects
   - `expertise/{target}/` - for learning topics
3. If a match is found:
   - Create a new file `YYYYMMDD-HHMM.md` in that location
   - Use the appropriate template for that category
4. If no match is found and target seems like a category (person name, project name, topic):
   - Ask: "I don't see {target} yet. Should I create it in domains/people/, initiatives/, or expertise/?"
   - Create the folder and note based on response
5. If no clear target can be inferred:
   - Put the note in `inbox/YYYYMMDD-HHMM-{slug}.md` where `{slug}` is the first few words of the content, lowercased and hyphenated
   - Use a simple template with just the content

## Templates

### People (domains/people/)
```
# {Name} - {Date} {Time}

## Notes

{content}

## Decisions



## Next Steps


```

### Initiatives
```
# {Project} - {Date} {Time}

## Notes

{content}

## Decisions



## Next Steps


```

### Expertise
```
# {Topic} - {Date} {Time}

## Notes

{content}

## Resources


```

### Inbox
```
# {Date} {Time}

{content}
```
