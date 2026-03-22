# Rules Guide

This guide is about **rules**, not just skills.

In practice, “rules” show up across OpenClaw in several places:

- workspace behavior files like `AGENTS.md`, `SOUL.md`, `TOOLS.md`, `USER.md`
- skill instructions in `SKILL.md`
- command and routing policy in `openclaw.json`
- approval and safety expectations around tools and external actions

A rule is any instruction that narrows behavior in a durable, reusable way.

---

## 1. Different kinds of rules

### Behavioral rules

These shape tone, judgment, and defaults.

Examples:

- be concise
- prefer Chinese in this workspace
- ask before external actions
- use `trash` instead of `rm`

### Operational rules

These shape workflow execution.

Examples:

- read local docs first
- run `openclaw status` yourself when possible
- use the browser tool for websites instead of vague descriptions
- prefer read-only inspection before mutation

### Routing and authorization rules

These determine where messages go and who can do what.

Examples:

- multi-agent channel bindings
- allowlists
- command authorization
- thread/session focus rules

### Tool-safety rules

These constrain higher-risk capabilities.

Examples:

- require approval for elevated exec
- do not expose plugin tools unnecessarily
- deny destructive commands by default

---

## 2. What a good rule looks like

A good rule is:

- **specific**
- **testable**
- **narrow enough to be followed consistently**
- **worth the context it costs**

Bad rule:

- “Always do the best thing.”

Better rule:

- “Before answering OpenClaw configuration questions, consult local docs first.”

Bad rule:

- “Be safe.”

Better rule:

- “Ask before sending emails, public posts, or other actions that leave the machine.”

---

## 3. Where to put rules

### Put stable workspace rules in workspace files

Good homes:

- `AGENTS.md` — workflow, guardrails, habits
- `SOUL.md` — tone/persona
- `USER.md` — user preferences and relationship context
- `TOOLS.md` — environment-specific notes

### Put task-specific rules in skills

If a rule only matters for a certain workflow, keep it in that skill.

Example:

- a document-editing skill can define how to handle tracked changes
- a security audit skill can require confirmation before firewall changes

### Put system policy in config

Examples:

- command authorization
- routing
- tool allow/deny
- channel settings

---

## 4. Rules should be concrete enough to survive pressure

When the system is busy, a vague rule collapses first.

Use rules like:

- “Number user choices so they can reply with a single digit.”
- “Ask for approval before destructive commands.”
- “In groups, only reply when directly mentioned or when adding clear value.”
- “Use local docs first for OpenClaw behavior.”

These are much stronger than abstract preferences.

---

## 5. Rules for group chat behavior

A lot of agents fail here by being too eager.

Good group rules often include:

- reply when directly asked
- stay quiet during normal human back-and-forth
- do not dominate a thread
- prefer a single thoughtful response over many fragments
- use reactions where supported instead of noisy text replies

This is one of the highest-leverage rule categories because it directly affects whether the agent feels human or annoying.

---

## 6. Rules for risky actions

Write these explicitly.

Good examples:

- ask before public posting
- ask before deleting or overwriting important files
- do not change firewall/SSH settings without confirming access path
- never claim a tool succeeded if the tool was unavailable
- do not leak private workspace context into group chats

---

## 7. Rules for documentation and memory

Strong agents write things down.

Useful rules include:

- if something should persist, write it to a file
- use daily notes for raw logs
- use `MEMORY.md` for curated long-term memory
- document learnings when workflows fail

These rules matter because model memory is not durable by itself.

---

## 8. A good rule-writing checklist

Before adding a rule, ask:

- What failure mode does this prevent?
- Is the rule concrete enough to test?
- Is this rule global, workspace-specific, or task-specific?
- Does it belong in config instead of prose?
- Will this still make sense in three months?
- Does it conflict with any existing rule?

If the answer is unclear, the rule probably needs rewriting.

---

## 9. Example transformations

### Example 1

Weak:

- “Be careful with commands.”

Strong:

- “Do not run destructive commands without asking.”

### Example 2

Weak:

- “Respect privacy.”

Strong:

- “Do not leak private workspace information into group chats.”

### Example 3

Weak:

- “Use tools wisely.”

Strong:

- “When a first-class tool exists, use it instead of asking the user to run an equivalent command.”

---

## 10. The best rules reduce ambiguity

The point of a rule is not decoration.

A good rule removes uncertainty in recurring situations.

If a rule does not change decisions, prevent errors, or improve consistency, it probably does not belong.

---

## 11. Rule templates

### Safety rule template

- Before doing **X**, confirm **Y**.
- Never do **Z** without explicit approval.

### Workflow rule template

- For tasks involving **domain A**, consult **source B** first.
- Prefer **method C** unless **condition D** applies.

### Communication rule template

- In **context A**, respond only when **condition B**.
- Prefer **style C** over **style D**.

---

## 12. Bottom line

Good rules make agents calmer, safer, and more predictable.

They are not slogans.
They are operating constraints that improve behavior under real pressure.
