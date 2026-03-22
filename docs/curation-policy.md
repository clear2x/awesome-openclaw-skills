# Curation Policy

This repo is curated for **signal, safety, and real-world usefulness**.

## Inclusion criteria

A skill should usually meet most of these:

1. **Clear purpose**
   - The trigger conditions are obvious.
   - The workflow is understandable.

2. **Real utility**
   - Solves a repeated task.
   - Saves user or agent time.
   - Teaches a capability worth reusing.

3. **Reasonable safety profile**
   - Does not hide risky side effects.
   - Does not normalize unsafe automation.
   - Does not require broad trust without disclosure.

4. **Good writing quality**
   - Concise, focused, and operational.
   - Avoids prompt bloat.
   - Includes boundaries and limitations.

5. **Maintainability**
   - Not obviously abandoned or broken.
   - Dependencies and setup are understandable.

---

## Strongly preferred traits

We especially like skills that are:

- read-heavy rather than write-heavy
- diagnostic rather than destructive
- transparent about permissions and dependencies
- specific in scope
- easy to audit quickly
- useful to many OpenClaw users

---

## Exclusion criteria

A skill is likely to be excluded if it is:

### 1. Dangerous by design

Examples:

- stealth surveillance
- secret extraction
- mass unsolicited outreach
- destructive shell automation with weak controls
- credential misuse or impersonation flows

### 2. Too vague to trust

Examples:

- “do anything with bash” skills
- giant prompts with unclear boundaries
- tools that claim safety without real mechanisms

### 3. Low-signal prompt clutter

Examples:

- mostly generic AI advice
- no specific workflow
- no concrete domain knowledge
- no repeatable operational value

### 4. Misleading or stale

Examples:

- broken setup instructions
- unsupported tools presented as working
- outdated dependency assumptions with no warning

---

## How we describe risky but educational skills

Some skills are interesting from a design perspective but not safe to recommend directly.

When useful, we may:

- mention them as anti-patterns
- discuss their design problems
- explain how to rewrite them safely

We do **not** have to list everything to be “complete.”

---

## Quality rubric

Each candidate can be scored informally across:

- **Utility** — does it solve a recurring problem?
- **Clarity** — is the trigger and workflow obvious?
- **Safety** — are permissions, side effects, and limits explicit?
- **Portability** — can others realistically use or adapt it?
- **Maintenance** — does it look current and supportable?

A skill with strong utility but weak safety usually does **not** make the list.

---

## How we treat ClawHub and public registries

Public registries are useful discovery layers, not trust guarantees.

That means:

- registry presence is **not** endorsement
- downloads are **not** proof of quality
- a public upload is still third-party code/instructions

Everything should be treated as reviewable and potentially untrusted.

---

## Scope of this repo

This repo is not only for ready-to-install skills.

It may also include:

- official bundled skills worth studying
- public examples worth adapting
- rule-writing guidance
- design notes on what makes a skill good or bad

That lets the repo stay useful even while the public ecosystem is still small.
