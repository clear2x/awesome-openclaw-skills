# Research Memo

## Objective

Create a public repo that:

1. curates valuable low-risk skills
2. teaches people how to write good skills
3. teaches people how to write good rules

## Ecosystem reality

### OpenClaw

OpenClaw has a meaningful built-in skill ecosystem already.

Local inspection shows ready skills like:

- feishu-doc / drive / perm / wiki
- github
- gh-issues
- healthcheck
- node-connect
- weather
- video-watcher
- self-improvement
- skill-creator

This means the strongest immediate source material is **OpenClaw’s bundled and extension skills**, not a huge public registry.

### ClawHub

ClawHub presents itself as a skill registry with install/update/publish flows.

Observed public state at the time of drafting:

- concept is promising
- install flow is clear
- public catalog appears sparse / early-stage
- highlighted/popular sections appear mostly empty

Implication:

- README should be honest
- repo should not pretend the public ecosystem is already mature
- curation should lean on quality examples and criteria, not volume claims

## Recommended categories

1. documentation / knowledge work
2. developer workflow
3. collaboration integrations
4. diagnostics / troubleshooting
5. lightweight utilities

These categories maximize usefulness while staying relatively low-risk.

## Recommended feature candidates

### Strong candidates

- `skill-creator`
- `weather`
- `github`
- `healthcheck`
- `node-connect`
- `feishu-doc`
- `feishu-drive`
- `feishu-perm`
- `feishu-wiki`
- `video-watcher`

### Why these work

- they have clear triggers
- they demonstrate workflow packaging
- several are low-risk and read-heavy
- the riskier ones generally include explicit process and boundaries

## Exclusion criteria

Do not prominently recommend skills that are:

- destructive by default
- vague about permissions or side effects
- built around secret extraction or surveillance
- mostly shell injection wrapped as “automation”
- stale and misleading

## Quality rubric

Use five filters:

1. utility
2. clarity
3. safety
4. portability
5. maintenance

## Recommendation for tutorial coverage

The project should include two first-class guides:

### Skill guide
Must explain:

- skill folder anatomy
- concise descriptions
- trigger quality
- progressive disclosure via scripts/references/assets
- OpenClaw gating metadata
- safety boundaries
- anti-patterns

### Rules guide
Must explain:

- different rule types
- where rules belong
- how to write concrete rules
- communication and group-chat rules
- safety and approval rules
- memory/documentation rules

## Positioning recommendation

This project should be framed as:

- a curated starting point
- a design-quality filter
- a practical writing guide

Not as:

- “the complete registry”
- “the biggest list”
- blind endorsement of every public skill
