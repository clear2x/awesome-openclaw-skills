# Awesome OpenClaw Skills

> Curated skills. Better skill-writing. Safer rules.

A curated, safety-conscious collection of high-value **OpenClaw / AgentSkills** resources.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-AgentSkills--compatible-blue)](https://docs.openclaw.ai/tools/skills)
[![ClawHub](https://img.shields.io/badge/Discover-ClawHub-orange)](https://clawhub.ai/)

This repo has three jobs:

1. **Curate useful skills** worth studying, installing, or adapting.
2. **Teach people how to write good skills** with real OpenClaw-compatible guidance.
3. **Teach people how to write rules** for agent behavior, routing, and safe operation.

> This is **not** a dump of every skill we can find.  
> The bar here is: **useful, understandable, maintainable, and low-risk**.

---

## Why this exists

The OpenClaw ecosystem is powerful, but skill discovery is still early.

- OpenClaw supports **AgentSkills-compatible** skill folders.
- Skills can come from bundled OpenClaw skills, workspace skills, managed local skills, plugins, and registries like **ClawHub**.
- But not every public skill is worth installing.
- Some are narrow, stale, badly scoped, or risky.

This project tries to create a cleaner path:

- a curated shortlist instead of noise
- a practical writing guide instead of vague theory
- clear safety standards instead of “just trust random skill folders”

---

## What you'll find here

- **Curated examples** of strong OpenClaw-compatible skills
- **A practical guide** to writing better `SKILL.md` files
- **A rules guide** for behavior, safety, routing, and workspace conventions
- **A curation policy** that explains what belongs here — and what doesn't

---

## Quick links

- [Awesome Skills List](lists/awesome-skills.md)
- [Skill Writing Guide](docs/skill-writing-guide.md)
- [Rules Guide](docs/rules-guide.md)
- [Curation Policy](docs/curation-policy.md)
- [Research Memo](docs/research-memo.md)

---

## What counts as a good skill

A skill is worth featuring here if it is:

- **Actually useful** in repeated real workflows
- **Clear about when it should trigger**
- **Concise** and not bloated
- **Safe by default**
- **OpenClaw-compatible** or easily adaptable
- **Honest about dependencies, limits, and side effects**

We especially like skills that:

- save repeated effort
- package domain knowledge cleanly
- improve reliability for recurring tasks
- teach correct tool usage without turning into prompt soup

---

## Repo structure

- `lists/awesome-skills.md` — curated skills and references
- `docs/skill-writing-guide.md` — how to write good OpenClaw/AgentSkills skills
- `docs/rules-guide.md` — how to write effective rules for behavior and routing
- `docs/curation-policy.md` — inclusion, exclusion, and safety criteria
- `docs/research-memo.md` — notes on ecosystem state and selection strategy
- `examples/` — starter examples for skills and rules

---

## Fast start

### Browse OpenClaw docs

- Skills: <https://docs.openclaw.ai/tools/skills>
- Creating skills: <https://docs.openclaw.ai/tools/creating-skills>
- Slash commands: <https://docs.openclaw.ai/tools/slash-commands>
- ClawHub: <https://clawhub.ai/>

### Install a skill locally

```bash
clawhub install <skill-slug>
```

Or create a workspace skill manually:

```bash
mkdir -p ~/.openclaw/workspace/skills/my-skill
$EDITOR ~/.openclaw/workspace/skills/my-skill/SKILL.md
```

### Inspect available skills

```bash
openclaw skills list
openclaw skills list --eligible
openclaw skills check
```

---

## Highlighted safe, high-value categories

These are the categories this repo prioritizes.

### 1. Documentation and knowledge work

Low-risk, high-utility skills that help read, summarize, organize, and transform information.

Examples:
- video transcript readers
- documentation summarizers
- wiki/doc readers
- note-system helpers

### 2. GitHub and developer workflow

Skills that help with issue triage, PR review support, CI inspection, and repo maintenance.

Examples:
- GitHub CLI workflow skills
- issue triage skills
- changelog/release note helpers

### 3. Local diagnostics and ops

Skills that help inspect systems, run health checks, or guide troubleshooting without creating hidden automation risk.

Examples:
- health checks
- node connectivity diagnosis
- environment inspection skills

### 4. Communication/workspace integrations

Skills that make agents useful inside real work environments.

Examples:
- Feishu docs/drive/wiki helpers
- Slack/Discord workflow helpers
- calendar/note integrations with clear boundaries

### 5. Retrieval and formatting helpers

Skills that package repeatable reference workflows well.

Examples:
- weather lookup
- transcript extraction
- summary formatting
- note normalization

---

## Things we explicitly avoid

We do **not** want to normalize risky skills just because they are flashy.

Examples of likely exclusions:

- stealthy surveillance skills
- credential-harvesting or secret-exfiltration helpers
- destructive automation with weak guardrails
- mass-messaging / spammy outreach skills
- “self-modifying” behavior with no review path
- vague shell-heavy skills that execute arbitrary user strings unsafely
- skills that imply safety claims they cannot enforce

See [`docs/curation-policy.md`](docs/curation-policy.md).

---

## Current reality of ClawHub

As of this repo’s initial draft, ClawHub looks promising, but the public ecosystem appears **early and sparse**.

That means this project does **not** pretend there are already hundreds of vetted gems. Instead, it does three things honestly:

1. feature strong bundled and public-reference examples
2. document what “good” looks like
3. create a place where better public skill curation can grow

---

## Contributing

Pull requests are welcome, but this is a **curated** list.

Please read:

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [docs/curation-policy.md](docs/curation-policy.md)

If you propose a skill, include:

- what it does
- why it matters
- why it is low-risk
- whether it is OpenClaw-ready or just conceptually relevant
- what dependencies or credentials it needs

---

## License

MIT
