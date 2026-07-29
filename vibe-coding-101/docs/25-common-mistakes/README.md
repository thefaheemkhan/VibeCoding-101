# Common Mistakes in AI-Assisted Development

## Introduction

This page collects the failure patterns that show up repeatedly across
vibe-coded projects — not typos or one-off bugs, but structural habits
that reliably cause pain later. Each entry names the mistake, why it
happens, and the concrete fix.

## Why It Matters

Most of these mistakes are invisible in the moment — the code runs, the
demo works, everyone moves on. The cost shows up weeks later as a
security incident, an unmaintainable codebase, or a rewrite. Recognizing
the pattern early is far cheaper than fixing the consequence.

## First Principles

Nearly every mistake on this page traces back to one of three root
causes:

1. **Skipping review** because the output "looks right."
2. **Skipping planning** because prompting feels faster than designing.
3. **Trusting scale** — accepting large, unreviewed changes because
   reviewing them carefully feels slower than it apparently is.

## The Mistakes

### 1. Accepting large, unreviewed diffs

**Why it happens:** Reviewing a 500-line AI-generated diff feels
tedious, so it gets skimmed instead of read.
**Consequence:** Bugs, security issues, and unwanted architectural
decisions hide in the volume.
**Fix:** Keep changes small enough to review properly — see
[Introduction](../01-introduction/README.md). If a diff is too large to
review carefully, it's too large, regardless of whether it "works."

### 2. No plan before building

**Why it happens:** Prompting straight into "build me X" feels like
progress; planning feels like a delay.
**Consequence:** The AI makes dozens of unstated architecture and scope
decisions for you, many of which you'll want to undo once you see the
full picture.
**Fix:** See [Planning](../08-planning/README.md) — scope and sketch
architecture before generating code.

### 3. Treating first output as final

**Why it happens:** The first draft compiles and runs, so it feels done.
**Consequence:** Subtle logic errors, missed edge cases, and style
inconsistencies ship unnoticed.
**Fix:** Budget for iteration explicitly. Ask "what edge cases might
this miss?" as a standard follow-up.

### 4. No security review pass

**Why it happens:** Security issues don't break the demo, so they're
invisible without deliberate review.
**Consequence:** Injection vulnerabilities, broken auth, leaked secrets
ship to production.
**Fix:** See [Security](../18-security/README.md) — run an explicit
security-focused review on any code touching auth, payments, or user
data.

### 5. No tests to validate against

**Why it happens:** Writing tests feels like it slows down the "vibe."
**Consequence:** You can't distinguish "looks right" from "is right,"
and regressions go unnoticed as the AI makes further changes.
**Fix:** See [Testing](../15-testing/README.md) — generate tests
alongside features, not after.

### 6. Trusting hallucinated APIs/libraries

**Why it happens:** Confident, well-formatted code that references a
plausible-sounding method is easy to trust.
**Consequence:** Code fails at runtime or, worse, silently does the
wrong thing.
**Fix:** Verify unfamiliar API calls against real documentation before
relying on them. See [AI Coding Fundamentals](../02-fundamentals/README.md).

### 7. Letting scope creep back in mid-build

**Why it happens:** Each individual "just add this too" feels small.
**Consequence:** The project never converges; complexity compounds
faster than a vibe-coding loop can keep up with.
**Fix:** Write scope down explicitly and defer additions to a tracked
"later" list, per [Planning](../08-planning/README.md).

### 8. No architectural ownership

**Why it happens:** It's easy to let each prompt's output silently
define the architecture, one file at a time.
**Consequence:** Inconsistent patterns, duplicated logic, and a codebase
no single person (or model) fully understands.
**Fix:** Maintain your own mental model / lightweight design doc of the
system, and correct drift explicitly. See
[System Design](../09-system-design/README.md).

### 9. Copy-pasting instead of using grounded tools

**Why it happens:** Feels simpler than setting up an IDE-integrated or
agentic tool.
**Consequence:** Wastes context budget, loses relevant surrounding code,
and doesn't scale past small snippets.
**Fix:** Use tools that can read your actual files once your codebase
outgrows single-function snippets. See [AI IDEs](../04-ai-ides/README.md).

### 10. Ignoring dependency and license implications

**Why it happens:** Adding a suggested package is one line; checking its
license and maintenance status is extra effort.
**Consequence:** Legal exposure, abandoned dependencies, supply-chain
risk.
**Fix:** Review any new dependency's license, maintenance activity, and
known vulnerabilities before accepting it.

## Summary

Every mistake above is a shortcut around review, planning, or
verification — each of which feels like it saves time in the moment and
costs more later. The fix is nearly always the same shape: keep changes
small, plan before building, and verify deliberately rather than
trusting fluent output.

## Related Pages

- [Introduction to Vibe Coding](../01-introduction/README.md)
- [Best Practices](../24-best-practices/README.md)
- [Security](../18-security/README.md)
- [Testing](../15-testing/README.md)
