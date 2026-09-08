# HUMAN.md Specification

**Version:** 0.1  
**Status:** Experimental

## Purpose

HUMAN.md provides portable context describing how an AI agent should work with a particular human.

## Design principles

HUMAN.md should be human-readable, AI-readable, portable, concise, editable, version-controlled, and vendor-neutral.

## Recommended sections

Identity, Role, Communication, Decision Making, Autonomy, Collaboration, Expertise, Preferences, Boundaries, Approval Rules, Feedback, Goals, and Current Context.

None are mandatory in v0.1.

## Core distinction

**HUMAN.md = how to work with me now**

**history/ = what happened before**

Team-specific context can live under `teams/`.

## Precedence

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

Historical information must not override an explicit current instruction.

## Privacy

Public HUMAN.md files should contain only information the human is comfortable making public.

## Agent changes

Agents may propose updates based on observed preferences, but should not silently rewrite persistent human preferences.

## Open questions

- What information is genuinely useful to agents?
- What belongs in HUMAN.md versus memory?
- How much should be standardised?
- How should team context extend global context?
- How should privacy and consent work?
- Can HUMAN.md become portable across agent platforms?
