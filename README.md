# claude-summary-obsidian

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that turns any conversation into a structured Obsidian-compatible markdown note. Invoke it with `/summary` at the end of a session to generate a note with YAML frontmatter, tags, and sections for key points, code outputs, and next steps — saved directly to your vault.

Built to leverage [obsidian-skills](https://github.com/kepano/obsidian-skills/tree/main) and [Obsidian CLI](https://help.obsidian.md/cli) but can also simply write the file in your vault as pure markdown.

## Features

- Proposes a title, summary, and keywords for approval before writing
- Outputs Obsidian-flavored markdown with `Topic` and `Type` frontmatter - which will be useful to build an Obsidian base
- Consistent template: Summary, Initial Prompt, Key Points, Code/Outputs, Next Steps, Context
- Saves notes to your vault's `claude/notes` folder

## Installation

```
# Project-level command (shared via git)
mkdir -p .claude/commands

# Or user-level (available across all projects)
mkdir -p ~/.claude/commands
```
Copy `summary.md` into your Claude Code commands directory.

## Usage

At the end of any Claude Code session, run:

```
/summary
```

Claude will propose a title, a short summary, and three keywords. Once approved, it writes the note to your Obsidian vault.

## Note Template

```markdown
---
Topic: "<10 word summary>"
Type: "<Analysis | Literature | Exploration>"
---

Tags: #Keyword1 #Keyword2 #Keyword3

# Title

## Summary
## Initial prompt
## Key Points
## Code/Outputs
## Next Steps
## Context
```
