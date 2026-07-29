# Planning Prompts

See [Planning](../../docs/08-planning/README.md) for the concepts behind
these templates.

## 1. Idea → Build Plan

Use when you have a rough idea and need it turned into a scoped,
buildable plan.

```text
I want to build: [one-sentence idea].

Help me turn this into a build plan:
1. Ask me clarifying questions about goal, audience, and constraints.
2. Propose a minimal v1 scope and a "later" list — push back if
   something I want in v1 isn't essential.
3. Sketch a simple architecture (components + data model).
4. Break v1 into an ordered list of small, independently reviewable
   tasks (each with a one-sentence "done" condition).
```

## 2. Scope Stress Test

Use when you already have a feature list and want to pressure-test it.

```text
Here's my planned feature list for v1: [list].

For each item, tell me:
- Is this actually necessary for v1 to be useful, or can it wait?
- What's the smallest version of this feature that still delivers value?
- What am I likely missing that v1 needs but I haven't listed?
```

## 3. Task Breakdown

Use when you have an approved scope and need it split into
prompt-sized units of work.

```text
Here's my approved v1 scope: [paste scope/spec].

Break this into an ordered list of implementation tasks. Rules:
- Each task should be completable and reviewable independently.
- Each task should leave the project in a working state when done.
- Note dependencies between tasks explicitly.
- Flag any task that seems too large to review in one pass, and split
  it further.
```

## 4. Requirements Clarification

Use at the very start, before any scoping, when the idea itself is
still fuzzy.

```text
I have a rough idea I want to build: [idea].

Ask me one question at a time (not a list) to clarify:
- Who this is for and what problem it solves for them
- What "done" looks like for a first version
- Any hard constraints (budget, timeline, must-use tech, must-avoid tech)

Don't propose solutions yet — just help me clarify the problem first.
```

## Related

- [Planning](../../docs/08-planning/README.md)
- [System Design](../../docs/09-system-design/README.md)
- [Prompt Library home](../README.md)
