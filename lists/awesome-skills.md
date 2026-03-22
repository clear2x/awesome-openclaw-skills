# Awesome Skills List

A practical shortlist of OpenClaw / AgentSkills examples worth studying.

> This list mixes:
> - OpenClaw bundled skills
> - OpenClaw extension skills
> - workspace/public examples
> - ecosystem references
>
> It is intentionally curated, not exhaustive.

---

## Best reference skills to study first

### `skill-creator`
- **Why it matters:** strong meta-guidance on building good skills
- **Why it is safe:** instructional, not side-effect heavy
- **Best lesson:** skills should be concise, modular, and operational

### `weather`
- **Why it matters:** model trigger is obvious, scope is narrow, examples are concrete
- **Why it is safe:** mostly read-only and low-risk
- **Best lesson:** small skills can be excellent when the scope is crisp

### `github`
- **Why it matters:** practical real-world dev workflow skill
- **Why it is safe:** explicit dependency (`gh`), concrete command patterns
- **Best lesson:** a skill can package tool usage patterns without becoming bloated

### `healthcheck`
- **Why it matters:** great example of guardrails around risky system actions
- **Why it is safe:** approvals, rollback thinking, context gathering first
- **Best lesson:** higher-risk skills need process discipline, not just capability

### `feishu-doc`
- **Why it matters:** clean mental model for a one-tool integration with many actions
- **Why it is safe:** action-based structure is explicit and inspectable
- **Best lesson:** integrations improve when the workflow is concrete, not abstract

### `feishu-drive`, `feishu-perm`, `feishu-wiki`
- **Why they matter:** strong examples of workflow-specific collaboration skills
- **Why they are useful:** real workplace tasks, clear domain scope
- **Best lesson:** separate adjacent domains into multiple focused skills

### `video-watcher`
- **Why it matters:** useful retrieval/transcript workflow for public video content
- **Why it is useful:** high leverage for summarization and extraction tasks
- **Best lesson:** a skill can combine acquisition + reading + summarization cleanly

### `node-connect`
- **Why it matters:** good troubleshooting-oriented skill
- **Why it is safe:** focused on diagnosis and repair of a bounded system
- **Best lesson:** narrow diagnostic skills are often highly valuable

---

## Good categories to curate over time

### Documentation / knowledge skills
Examples:
- transcript readers
- doc/wiki readers
- note-system helpers
- PDF / summary helpers

### Dev workflow skills
Examples:
- GitHub / PR / CI helpers
- issue triage skills
- release-note skills

### Collaboration skills
Examples:
- Feishu / Slack / Discord integrations
- permission and doc workflow helpers

### Diagnostics / operations skills
Examples:
- health checks
- connectivity troubleshooting
- environment inspection

### Lightweight utility skills
Examples:
- weather
- summarization
- formatting helpers

---

## Public ecosystem notes

### ClawHub
- Useful as a discovery layer and eventual publishing surface
- Promising concept: versioned, searchable skill registry
- Current public surface appears early-stage and sparse
- Should be treated as a source of candidates, not trust

### OpenClaw bundled skills
- Best current source of high-signal examples
- Useful because they already reflect OpenClaw’s expectations and constraints

### Workspace / community examples
- Often valuable for niche workflows
- Need stronger review because quality varies a lot

---

## Skills we would be cautious about featuring

Be careful with skills that:

- shell out freely from untrusted user input
- automate outreach or messaging at scale
- touch secrets without strong boundary language
- change infrastructure without rollback guidance
- promise “agent autonomy” while hiding side effects

---

## What this list is optimizing for

This repo prefers:

- **high signal** over novelty
- **safety** over hype
- **transferable design lessons** over one-off gimmicks
