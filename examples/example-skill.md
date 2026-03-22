# Example Skill

A tiny reference skill showing a clean, low-bloat structure.

```text
example-skill/
└── SKILL.md
```

```markdown
---
name: example-skill
description: Summarize a plain text report and extract the top three action items.
metadata: { "openclaw": { "requires": { "bins": ["sed"] } } }
---

# Example Skill

## When to use

- User asks to summarize a plain text report
- User wants action items extracted

## When not to use

- Binary files
- PDFs that need OCR
- Spreadsheets or slide decks

## Workflow

1. Read the file.
2. Identify the main objective.
3. Extract the top three action items.
4. Return a short summary first, then bullets.
5. If the file is not plain text, stop and say why.
```
