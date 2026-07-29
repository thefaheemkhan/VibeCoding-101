# Debugging Prompts

See [Debugging](../../docs/16-debugging/README.md) for concepts (once
published — tracked in [ROADMAP.md](../../ROADMAP.md)).

## 1. Root Cause Diagnosis (diagnose before fixing)

```text
Here is the relevant code (unmodified) and the exact error I'm seeing:

--- file: [path] ---
[paste code]

--- error ---
[paste full stack trace / error output]

Diagnose the root cause first — don't propose a fix yet. If you need
another file to be sure, ask for it instead of guessing.
```

## 2. Reproduce-then-Fix

```text
Bug report: [describe observed behavior vs expected behavior]

Relevant code: [paste]

1. Restate the expected vs actual behavior in your own words to confirm
   you understand the bug.
2. Identify the minimal steps/inputs that reproduce it.
3. Only then propose a fix, and explain why it addresses the root cause
   (not just the symptom).
```

## 3. Regression Hunt

```text
This used to work and broke sometime after [reference point, e.g. a
commit range or date]. Here's the current code: [paste]. Here's what
changed recently: [paste diff/commit log if available].

Identify which change is most likely responsible and why, before
suggesting a fix.
```

## 4. "Explain Like I'm Debugging at 2am"

```text
I'm stuck on this bug and my usual approaches haven't worked:
[describe what you've already tried]

Code: [paste]
Error: [paste]

Suggest 3 hypotheses for the root cause, ranked by likelihood, each with
one concrete way to test whether it's correct.
```

## Related

- [AI Coding Fundamentals](../../docs/02-fundamentals/README.md)
- [Testing](../../docs/15-testing/README.md)
- [Prompt Library home](../README.md)
