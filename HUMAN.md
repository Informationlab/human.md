# HUMAN.md

> Portable context for working with a human in AI-assisted teams.

## The idea

AI agents increasingly work as members of teams. They have `AGENTS.md`,
skills, tools, memory, project documentation, and other context that tells
them how to operate.

But what about the human?

**HUMAN.md** is a simple, human-readable file that tells AI agents how to
work effectively with a particular human.

It is not intended to be a biography. Its primary purpose is collaboration.

---

## Why HUMAN.md?

Human context is often scattered across:

- conversations
- project management tools
- chat messages
- documents
- AI memory systems
- previous projects
- personal notes

Every new agent or team can otherwise start with little context.

A HUMAN.md gives an agent a portable starting point.

Instead of repeatedly explaining:

> "This is how I like to work."

the human can provide a structured context file.

---

# Example HUMAN.md

## 1. Identity

**Name:** Example Human

**Role:** Founder / Product Lead

**Location:** Europe

**Primary languages:** English, Dutch

---

## 2. How to communicate with me

Be direct and concise.

Start with the most important conclusion rather than a long introduction.

If something is uncertain, say so.

I prefer useful disagreement over polite agreement.

Do not hide problems in order to make an answer sound positive.

When there are several reasonable options, explain the trade-offs and
recommend one.

---

## 3. How I make decisions

I prefer:

1. Understand the objective.
2. Identify the important constraints.
3. Generate a small number of options.
4. Recommend the best option.
5. Act.

Do not turn every small decision into a question.

For reversible decisions, use reasonable judgement and proceed.

For expensive, irreversible, legal, security, or major strategic decisions,
stop and ask for approval.

---

## 4. Autonomy

I prefer AI agents to be proactive.

If you can safely complete a task without waiting for permission, do it.

If you discover a problem, investigate it before reporting it when possible.

Do not simply tell me that something cannot be done.

Try to find an alternative first.

---

## 5. Challenge me

You are expected to challenge my assumptions.

If my idea has a significant weakness:

1. Tell me clearly.
2. Explain why.
3. Suggest a better alternative.

Do not agree with an idea simply because I proposed it.

---

## 6. Working style

I tend to explore ideas conversationally.

An early idea may be incomplete or intentionally rough.

Do not interpret every exploratory statement as a final decision.

When an idea becomes a decision, make that distinction explicit.

I value:

- speed
- clarity
- experimentation
- practical results
- simple systems
- good UX

I generally prefer a simple working solution over an elaborate system that
has not yet been validated.

---

## 7. Working with multiple agents

Agents should communicate relevant discoveries to the team.

Avoid duplicating work already completed by another agent.

When handing work to another agent, provide:

- objective
- relevant context
- what has already been done
- decisions already made
- unresolved questions
- recommended next step

---

## 8. Context and memory

Do not assume that everything in previous conversations is a permanent
preference.

Distinguish between:

- temporary context
- current project decisions
- persistent preferences
- historical information

When uncertain, treat old information as context rather than truth.

---

## 9. Feedback

I prefer feedback that is:

- specific
- actionable
- honest
- proportional to the problem

Do not spend significant effort polishing something that has not yet been
validated.

---

## 10. What success looks like

The objective is not to maximise activity.

The objective is to make meaningful progress toward the goal.

An agent should ask itself:

> "What is the most useful thing I can do next?"

rather than:

> "What task can I complete?"

---

# HUMAN.md as part of a hybrid team

The larger idea is not just a file.

It is a possible model for teams where humans and AI agents work together.

For example:

```text
                    ┌──────────────┐
                    │    HUMAN     │
                    │  HUMAN.md    │
                    └──────┬───────┘
                           │
              ┌────────────┼────────────┐
              │            │            │
              ▼            ▼            ▼
          Researcher   Designer      Engineer
            Agent        Agent         Agent
              │            │            │
              └────────────┼────────────┘
                           ▼
                         PROJECT
```

The human is not simply a user of the agents.

The human is a member of the team.

---

# HUMAN.md vs AGENTS.md

They serve different purposes.

### AGENTS.md

Describes how an AI agent should operate within a repository or project.

Examples:

- coding conventions
- architecture
- commands
- tests
- deployment procedures
- repository rules

### HUMAN.md

Describes how to work with a particular human.

Examples:

- communication preferences
- decision-making style
- autonomy
- collaboration preferences
- approval boundaries
- feedback style
- relevant expertise

In a hybrid organisation, they complement each other.

```text
AGENTS.md
    ↓
How the agent works in this environment

HUMAN.md
    ↓
How the agent works with this human
```

---

# Portable human context

A human may participate in several teams:

```text
                    HUMAN.md
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
     Team A          Team B          Team C
        │              │              │
      agents         agents         agents
```

The human's core working preferences can remain stable while
team-specific context changes.

This means the human does not need to start from zero every time they join
a new AI team.

A repository can therefore contain team-specific context such as:

```text
HUMAN.md

teams/
├── product.md
├── engineering.md
└── research.md
```

---

# Human context and history

Long-term information should not necessarily live in HUMAN.md.

A possible structure is:

```text
HUMAN.md
    │
    ├── identity
    ├── role
    ├── communication
    ├── decision making
    ├── collaboration
    └── boundaries
          │
          ├── history/
          └── teams/
```

For example:

```text
history/
├── work-history.md
├── decisions.md
└── lessons-learned.md
```

The distinction is important:

**HUMAN.md = how to work with me now**

**history/ = what happened before**

Historical information should not automatically override current
instructions.

---

# Suggested repository structure

```text
human-md/
├── README.md
├── HUMAN.md
├── SPEC.md
├── teams/
│   └── example-team.md
└── history/
    └── work-history.md
```

---

# Minimal HUMAN.md

A HUMAN.md does not need to be large.

A minimal version could simply be:

```markdown
# Human

## Role

Founder and product lead.

## Communication

Be direct.
Start with the conclusion.
Challenge weak assumptions.

## Decision making

For reversible decisions, proceed without asking.

For expensive, irreversible, or strategic decisions,
present options and ask for approval.

## Collaboration

Take initiative rather than waiting for instructions.

If something is unclear, make a reasonable assumption
and state it explicitly.

## What to avoid

Do not create unnecessary process.
Do not repeat information already established.
Do not optimise something before understanding the goal.
```

---

# Specification — v0.1

## Status

**Version:** 0.1

**Status:** Experimental

HUMAN.md is currently a convention, not a formal standard.

The goal is to explore whether portable human context is useful for
human-AI collaboration.

---

## Design principles

HUMAN.md should be:

- human-readable
- AI-readable
- portable
- concise
- editable
- version-controlled
- understandable without proprietary software

It should not require a particular AI model, platform, agent framework,
or vendor.

---

## Recommended sections

A HUMAN.md may contain:

```text
Identity
Role
Communication
Decision Making
Autonomy
Collaboration
Expertise
Preferences
Boundaries
Approval Rules
Feedback
Goals
Current Context
```

None of these sections are mandatory in version 0.1.

---

## HUMAN.md is not a biography

Information should be included when it changes how an AI agent should work
with the human.

Good:

```markdown
I prefer agents to make reversible decisions without asking.
```

Less useful:

```markdown
I was born in...
```

unless that information is directly relevant to the team's work.

The guiding principle is:

> **How to work with me, not everything about me.**

---

## Team-specific context

Human context should be separated from team context.

For example:

```text
HUMAN.md

teams/
    product.md
    engineering.md
    research.md
```

`HUMAN.md` describes the person.

`teams/*.md` describes how that person works within a particular team.

---

## Historical context

Historical information may be stored separately:

```text
history/
    work-history.md
    decisions.md
    lessons-learned.md
```

History should provide context, not silently become current instruction.

---

## Precedence

When multiple sources of information exist, the recommended principle is:

```text
Current explicit instruction
        ↓
Current team context
        ↓
Current HUMAN.md
        ↓
Historical context
        ↓
Agent assumptions
```

An agent should not use historical information to override an explicit
current instruction.

---

## Privacy

HUMAN.md may contain personal or sensitive information.

Only publish information appropriate for the intended audience.

A public HUMAN.md should contain only information the human is comfortable
making public.

Private human context should remain private.

---

## Versioning

Because HUMAN.md is plain text, it can be version-controlled with Git.

For example:

```text
git log HUMAN.md
```

This creates an interesting possibility: the history of a human's
collaboration preferences can evolve alongside the history of the teams
they work with.

---

## Agents should not silently rewrite human preferences

Agents may observe repeated behaviour and propose changes to HUMAN.md.

They should not silently modify persistent human preferences unless
explicitly authorised.

A useful workflow is:

```text
Agent observes repeated preference
            ↓
Agent proposes HUMAN.md update
            ↓
Human approves
            ↓
HUMAN.md updated
```

---

# Future possibilities

Future versions could explore:

- machine-readable metadata
- standard schemas
- permissions
- multiple human profiles
- team membership
- agent-to-human compatibility
- human-to-agent preferences
- change proposals
- consent mechanisms
- identity verification
- privacy levels
- inheritance between teams
- organisational structures
- persistent human work history
- interoperability between agent platforms

These should not be standardised prematurely.

The first question is whether the basic concept is useful.

---

# Open questions

This project deliberately leaves several questions unanswered:

1. What information is genuinely useful to agents?
2. What belongs in HUMAN.md versus memory?
3. How much should be standardised?
4. Should humans have one global HUMAN.md or several?
5. How should private and public human context differ?
6. How should team-specific context override or extend personal context?
7. Can HUMAN.md become portable across different AI platforms?
8. Should agents be able to propose updates based on observed behaviour?
9. How should consent and privacy work?
10. What happens when a human's preferences change?

These questions are part of the experiment.

---

# Contributing

The best contribution is not necessarily more specification.

Try HUMAN.md with an AI agent.

Then report:

- What information was useful?
- What information was unnecessary?
- What did the agent misunderstand?
- What should be standardised?
- What should remain personal?
- What belongs in HUMAN.md versus team/project context?
- Did it actually improve collaboration?

---

# Core principle

The simplest definition of HUMAN.md is:

> **A portable, human-readable description of how to work effectively with
> a particular human.**

The larger hypothesis is:

> **If AI agents can have persistent identities, instructions, skills,
> memory, and histories, humans may also benefit from a portable interface
> describing how AI systems should collaborate with them.**

---


---

# Related projects

HUMAN.md is not a completely new idea. Several projects are already
exploring related territory, but they approach it from different
directions.

## 1. thellmwhisperer/human.md

A particularly close project is
**thellmwhisperer/human.md** on GitHub:

https://github.com/thellmwhisperer/human.md

It describes `human.md` as a framework for healthy human-agent
collaboration. Its central idea is that, just as `CLAUDE.md` tells an
agent how to work on a project, `human.md` tells an agent how to work
with the human.

Its current focus is quite specific: protecting humans from excessive
AI-agent usage. It can define working hours, blocked periods, session
limits, breaks, wind-down periods, and enforcement through a shell
wrapper and Claude Code `PreToolUse` hooks.

The project has also evolved beyond a simple Markdown convention and
includes an installer, enforcement mechanisms, session logging, and
support for multiple runtimes. Its releases include v1.4.1 as of March
2026.

### What it gets right

It demonstrates that the human can be treated as part of the agent's
operating context rather than merely as the person issuing commands.

It also makes an important distinction:

```text
CLAUDE.md / AGENTS.md
        ↓
How the agent works on the project

human.md
        ↓
How the agent works with the human
```

That distinction is very close to the core idea explored by this
repository.

### Where this proposal differs

Thellmwhisperer's project is primarily about **healthy usage and
guardrails for AI coding agents**.

This project proposes a broader concept:

> **HUMAN.md as a portable interface between a human and AI teams.**

The emphasis here is not primarily:

```text
"Don't let me work with the agent too long."
```

but:

```text
"Understand how to work with me wherever we work together."
```

That includes communication, decision-making, autonomy, expertise,
approval boundaries, collaboration style, and potentially persistent
working history.

### Potential shortcomings for the broader idea

The existing project is strongly tied to the Claude Code environment and
to session/usage controls. That makes it useful as a practical tool, but
it does not by itself solve the larger portability problem:

- How does a human carry their context between teams?
- How does the same human context work with different agent frameworks?
- How does team-specific context extend the human's global context?
- How should long-term history be separated from stable preferences?
- How can multiple agents share the same understanding of a human?
- How should an agent distinguish a current preference from an old one?

Those are the areas this project explores.

---

## 2. Intuition-Lab/personal-model

Another closely related project is
**Intuition-Lab/personal-model**:

https://github.com/Intuition-Lab/personal-model

This project takes a different approach. Rather than asking the human to
manually maintain a `HUMAN.md`, it builds a local-first Personal Model
from activity and makes that context available to multiple AI clients.

Its stated goal is effectively a living model of the person: what matters
now, how they tend to decide, and where their attention is moving.

This is particularly interesting because it addresses one of the major
weaknesses of a manually maintained HUMAN.md:

> **People are bad at continuously documenting themselves.**

### What it gets right

It explores:

- one personal context shared across agents
- evidence-linked memory
- evolving rather than static context
- user ownership
- local-first storage
- interoperability through MCP

### Difference

Personal Model is closer to a **personal memory/context runtime**.

This proposal is primarily about a **portable human-facing convention and
interface**.

They could eventually complement each other:

```text
                 HUMAN.md
              stable authored context
                       │
                       ▼
              Personal Model
          evolving contextual memory
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
       Agent A      Agent B       Agent C
```

A future HUMAN.md ecosystem could therefore use a Personal Model or
another memory system underneath it without making that implementation
mandatory.

---

## 3. Spacebot HUMAN.md

Spacebot also uses `HUMAN.md`. Its documentation describes a long-form
profile at:

```text
humans/{id}/HUMAN.md
```

The profile is rendered into the organisation context of agents connected
to that human.

Spacebot makes an especially useful distinction between stable human
profile information and changing memory.

It recommends putting things that remain true for years into HUMAN.md,
such as:

- identity
- how to work with the person
- tone
- escalation preferences
- standing rules
- sensitivities

while putting volatile information such as current projects, goals,
travel, or changing circumstances into a memory system.

### Why this matters

This strongly supports one of the principles in this project:

> If a statement needs an "as of" date to remain true, it probably
> belongs in memory rather than the stable HUMAN.md profile.

That separation should probably become an explicit part of any future
HUMAN.md specification.

---

## 4. Blank Collar / human.md

Another related effort is **Blank Collar**, which proposes an open
standard for a professional `human.md`:

https://www.blankcollar.me/

Its focus is different again. It treats `human.md` as a public,
agent-readable professional identity, potentially paired with an MCP
endpoint.

It is closer to:

```text
Human → professional identity → agents
```

whereas this project is interested in:

```text
Human → collaboration interface → AI team
```

There is useful overlap around portability, ownership, machine-readable
human context, and agent access.

The professional/public identity model could eventually be one possible
layer of a broader HUMAN.md ecosystem, rather than the whole concept.

---

# Comparison at a glance

| Project | Primary purpose | Stable human context | Memory/history | Team collaboration | Agent enforcement | Portable across agents |
|---|---|---:|---:|---:|---:|---:|
| thellmwhisperer/human.md | Healthy AI-agent usage | Yes | Limited | Limited | **Yes** | Partly |
| Personal Model | Living personal context | Yes | **Yes** | Potentially | No | **Yes** |
| Spacebot HUMAN.md | Agent organisation profile | **Yes** | **Yes, separately** | **Yes** | No | Within Spacebot |
| Blank Collar | Public professional identity | **Yes** | Limited | Limited | No | **Yes, by design** |
| This proposal | Human ↔ AI team interface | **Yes** | **Separate layer** | **Core goal** | Not required | **Core goal** |

---

# The opportunity

The important observation is that these projects are approaching different
parts of the same emerging problem.

```text
                     HUMAN
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      Identity      Memory      Collaboration
          │            │            │
     Blank Collar  Personal     HUMAN.md
                    Model       convention
                       │            │
                       └─────┬──────┘
                             ▼
                       AI AGENTS / TEAMS
```

Rather than competing with these projects, HUMAN.md could become a
**simple interoperability layer** between them.

For example:

- Blank Collar could provide public professional identity.
- Personal Model could provide evolving private memory.
- Spacebot could provide organisational implementation.
- thellmwhisperer/human.md could provide behavioural guardrails.
- A general HUMAN.md convention could define the portable collaboration
  layer.

That is potentially a stronger position than trying to build yet another
memory product.

---

# Current shortcomings of this proposal

This project should also be explicit about what it does **not** solve yet.

## 1. It is manually maintained

A static file becomes outdated.

A future system could allow agents to propose changes based on repeated
observations, while requiring human approval before changing persistent
preferences.

## 2. There is no machine-readable schema yet

Markdown is excellent for humans and LLMs, but different systems may
structure the information differently.

A future specification could define optional front matter or a standard
schema while keeping the human-readable Markdown.

## 3. There is no identity or authentication layer

A file saying "I am this person" does not prove that the person actually
authored it.

That becomes important if HUMAN.md is used for permissions, hiring,
financial actions, or other high-impact operations.

## 4. Privacy is unresolved

A detailed human profile can contain extremely sensitive information.

A future ecosystem needs clear distinctions between:

```text
public HUMAN.md
private HUMAN.md
team HUMAN.md
agent-specific context
private memory
```

## 5. Conflict resolution is unresolved

A human may have different preferences in different teams.

For example:

```text
Global preference:
Be concise.

Engineering team:
Provide detailed technical reasoning.

Board context:
Use executive summaries.
```

A future specification needs a principled way to resolve those layers.

## 6. There is no standard agent protocol

The file is useful only if agents actually read it.

The long-term opportunity is interoperability across agent platforms,
rather than depending on one particular coding agent.

---

# A possible future architecture

The eventual model could look like this:

```text
                         HUMAN
                           │
                           ▼
                     HUMAN.md
                 stable preferences
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
       Team Context                Personal Memory
       current role                evolving context
       current goals               evidence/history
              │                         │
              └────────────┬────────────┘
                           ▼
                    Collaboration Layer
                           │
          ┌────────────────┼────────────────┐
          ▼                ▼                ▼
       Researcher       Designer         Engineer
          Agent            Agent            Agent
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                         TEAM
```

The key idea is that the human becomes a persistent participant in the
AI organisation, rather than merely the person who happens to operate the
agents.

---

# Core hypothesis

The existing projects demonstrate that there is already real interest in
giving AI systems a structured understanding of the human.

The open question is whether we can turn that into a general,
vendor-neutral concept:

> **HUMAN.md is an interface between a human and the AI systems and teams
> they work with.**

Not a CV.

Not a biography.

Not merely a safety timer.

Not merely a memory database.

But a portable description of:

> **How should AI work with me?**

# License

CC0 1.0 Universal
