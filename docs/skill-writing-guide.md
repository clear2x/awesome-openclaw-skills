# Skill Writing Guide

This guide is for writing **OpenClaw-compatible AgentSkills** that are useful, concise, and safe.

## 1. What a skill is

In OpenClaw, a skill is a folder containing a `SKILL.md` file and optional supporting resources.

Typical layout:

```text
my-skill/
├── SKILL.md
├── scripts/
├── references/
└── assets/
```

OpenClaw loads skills from:

1. bundled skills
2. `~/.openclaw/skills`
3. `<workspace>/skills`

Precedence is:

`<workspace>/skills` → `~/.openclaw/skills` → bundled

---

## 2. Minimal valid skill

```markdown
---
name: my-skill
description: One-sentence explanation of when this skill should be used.
---

# My Skill

Use this skill when the user asks for X.

## Workflow

1. Do A.
2. Check B.
3. Return C.
```

A good `description` is critical because OpenClaw uses the available skills list to decide what to load.

---

## 3. What makes a skill good

A good skill does four things well:

### a. Triggers clearly

The description should say **when to use it** and often **when not to use it**.

Bad:

```yaml
description: Helps with files.
```

Better:

```yaml
description: Read, organize, and summarize PDF invoices. Use when the user asks about invoice extraction, totals, due dates, or invoice classification.
```

### b. Stays concise

Do not waste context budget.

A skill should not explain basic concepts the model already knows. Put only the domain-specific or workflow-specific guidance in `SKILL.md`.

### c. Encodes workflow, not vibes

Bad skills say “be helpful and accurate.”
Good skills say what to do:

- inspect the file
- validate assumptions
- prefer a certain tool
- ask for approval before destructive actions
- use a deterministic script when correctness matters

### d. Handles safety explicitly

If a skill can trigger side effects, say so.

Examples:

- ask before deleting
- ask before sending external messages
- do not run shell commands built from raw user input
- prefer read-only checks first

---

## 4. Use progressive disclosure

Keep `SKILL.md` focused.

Use:

- `scripts/` for repeatable code
- `references/` for longer docs, schemas, or examples
- `assets/` for templates and output resources

The main file should teach the workflow and point to deeper materials only when needed.

---

## 5. Recommended shape of SKILL.md

A practical template:

```markdown
---
name: example-skill
description: Explain exactly when to use this skill.
metadata: { "openclaw": { "requires": { "bins": ["curl"] } } }
---

# Example Skill

## When to use

- case A
- case B

## When not to use

- case C
- case D

## Workflow

1. Inspect inputs.
2. Prefer tool X.
3. If condition Y, read `references/deeper-guide.md`.
4. Ask for confirmation before side effects.
5. Return concise results first, detail second.

## Notes

- limitation 1
- limitation 2
```

---

## 6. OpenClaw-specific details that matter

### Single-line frontmatter discipline

OpenClaw’s embedded parser expects frontmatter keys to remain simple.

Important notes from the docs:

- `SKILL.md` must include `name` and `description`
- `metadata` should be a **single-line JSON object**
- optional gating can live under `metadata.openclaw`

### Common OpenClaw metadata fields

Useful fields include:

- `requires.bins`
- `requires.anyBins`
- `requires.env`
- `requires.config`
- `primaryEnv`
- `install`
- `os`
- `emoji`
- `homepage`

These matter because skill eligibility is filtered at load time.

### Session snapshot behavior

OpenClaw snapshots eligible skills when a session starts.

That means if you change skill files or skill config, you may need:

- a new session
- or a skill refresh / watcher-triggered reload
- or a gateway restart, depending on what changed

---

## 7. When to use scripts instead of prose

If a skill repeatedly needs the same fragile logic, use a script.

Use `scripts/` when:

- correctness matters
- the same code keeps being rewritten
- the workflow is deterministic
- shell one-liners would be too brittle

Examples:

- PDF transforms
- document conversions
- structured parsing
- stable API wrappers

---

## 8. Good examples to imitate

From current OpenClaw-ready skills, good patterns include:

- `weather` — clear scope, simple commands, clear exclusions
- `github` — practical command inventory, concrete use cases
- `healthcheck` — explicit workflow, approvals, and safety guardrails
- `feishu-doc` — one-tool mental model with concrete action examples

These skills are useful because they tell the model **what to do in practice**.

---

## 9. Anti-patterns

Avoid these:

### Overbroad skills

If a skill claims to handle too many unrelated tasks, it becomes vague and low-value.

### Prompt-bloat essays

Huge SKILL.md files often waste context and perform worse than smaller focused ones.

### Hidden side effects

If a skill sends messages, mutates files, creates tickets, or runs commands, say so.

### No boundaries

A skill should say when **not** to trigger.

### Re-explaining the obvious

Do not fill the file with generic AI advice.

---

## 10. A practical writing checklist

Before publishing a skill, ask:

- Is the name clear?
- Is the description triggerable?
- Is the scope narrow enough?
- Are side effects explicit?
- Are limitations honest?
- Can I move details into `references/`?
- Should a script replace part of this prose?
- Would another agent understand when to use it in 10 seconds?

If not, it is not ready.

---

## 11. Testing workflow

Useful commands:

```bash
openclaw skills list
openclaw skills list --eligible
openclaw skills check
```

And for manual testing, create a real prompt that should trigger the skill.

Examples:

- “Summarize this video transcript.”
- “Check current weather in Hangzhou.”
- “Review PR #42 CI status.”

If the trigger sentence feels fuzzy, improve the description.

---

## 12. Bottom line

A good skill is not a giant prompt.

It is a **compact operating manual** for a recurring job:

- clear trigger
- clear workflow
- clear boundaries
- clear safety model
- minimal wasted tokens
