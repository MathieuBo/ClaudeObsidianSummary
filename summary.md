Summarise our conversation as an Obsidian-compatible markdown note.

Before creating the note, propose a title (max 5 words), a 10-word (max) summary, and 3 keywords. Always upper-case the first letter of each keyword. Wait for user approval before writing.

## How to write the note

**Step 1: Discover the vault.** Run `obsidian vaults verbose` to get the vault name and path. Use the first vault listed. Parse the output as TSV: `<name>\t<path>`.

**Step 2: Create the note using the Obsidian CLI.**

```
obsidian create vault=<name> path="claude/notes/<Title>.md" content="<content>"
```

**Step 3 (fallback only):** If the content is too long for a single CLI argument (over ~4000 chars), write the file directly to `<vault_path>/claude/notes/<Title>.md` using the path obtained in Step 1.

## Note format

Use this exact template:

```
---
Topic: "<10 words summary>"
Type: "<Analysis | Literature | Exploration>"
---

Tags: #<Keyword1> #<Keyword2> #<Keyword3>

# <Title>

## Summary
<2-3 sentence high-level summary>

## Initial prompt
<initial prompt>

## Key Points
<bullet points of the main decisions, findings, or outputs>

## Code/Outputs
<any significant code snippets, file paths, or outputs produced>

## Next Steps
<actionable follow-ups if any>

## Context
<any important context for future reference>
```
