# Cheat Sheet: Prompt Engineering

Full guide: [docs/07-prompt-engineering](../docs/07-prompt-engineering/README.md)

## The 5-part structure

```
Role        → who/what expertise the model should apply
Context     → real code, real errors, stack/version, conventions
Task        → one clear, scoped request
Constraints → what must NOT change, dependencies allowed/disallowed
Output      → diff only? explanation? tests? format?
```

## Quick do / don't

| Do | Don't |
|---|---|
| Paste real code and real errors | Describe/paraphrase them |
| Scope one prompt to one task | Ask for a whole feature/app at once |
| State what must not change | Assume the model will infer it |
| Ask for reasoning before code on hard logic | Accept the first draft blind |
| Give explicit output format | Leave format to guesswork if you need to parse it |

## Fast templates

**Feature request:**
```
Context: [stack, relevant files, conventions]
Task: [one scoped ask]
Constraints: [what not to touch/add]
Output: diff only, note assumptions
```

**Bug report:**
```
Code: [paste]
Error: [paste full trace]
Diagnose root cause first, don't fix yet.
```

**Refactor:**
```
Refactor [target] to [goal]. Keep [X] identical. Do not change [Y].
Show diff, not full file.
```

## Escalation checklist (when output is wrong)

1. Did you paste the *actual* error, not a paraphrase?
2. Did you state constraints explicitly, or let the model guess?
3. Is the task actually one unit of work, or several bundled together?
4. Would asking for step-by-step reasoning first help on this task?
5. Are you on the right [model tier](../docs/03-ai-models/README.md) for
   this task's difficulty?

## Related

- [Prompt Engineering (full guide)](../docs/07-prompt-engineering/README.md)
- [Prompt Library](../prompts/)
