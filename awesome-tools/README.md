# Tool Directory

Structured, opinionated comparisons — not a link dump. Each entry
includes strengths, weaknesses, and best-fit use cases so you can choose
deliberately. **Pricing and feature details change quickly; verify on
the vendor's site before deciding — "last verified" dates are noted.**

> Full guides: [AI IDEs](../docs/04-ai-ides/README.md) ·
> [Coding Assistants](../docs/05-coding-assistants/README.md) ·
> [CLI Agents](../docs/06-cli-agents/README.md)
> *(some linked pages are still in progress — see [ROADMAP.md](../ROADMAP.md))*

## Category: AI-Native IDEs

IDEs built around AI-assisted, multi-file editing as a core workflow
rather than a bolt-on.

### Cursor

| | |
|---|---|
| **Category** | AI-native IDE (VS Code fork) |
| **Strengths** | Deep codebase-aware editing, fast inline diffs, strong multi-file refactor support, familiar VS Code extension ecosystem |
| **Weaknesses** | Pricing scales with usage on heavier workloads; being a fork means occasional lag adopting upstream VS Code features |
| **Platform** | macOS, Windows, Linux |
| **Best use cases** | Day-to-day feature development in an existing codebase; developers who want AI tightly integrated into normal editing, not a separate chat window |
| **Alternatives** | Windsurf, VS Code + Copilot |

### Windsurf

| | |
|---|---|
| **Category** | AI-native IDE |
| **Strengths** | Strong agentic "flow" mode for multi-step tasks, good at maintaining context across a session |
| **Weaknesses** | Smaller extension ecosystem than VS Code-based competitors |
| **Platform** | macOS, Windows, Linux |
| **Best use cases** | Longer, more autonomous multi-file tasks where you want the editor to drive more of the process |
| **Alternatives** | Cursor, VS Code + Copilot |

## Category: CLI / Agentic Coding Tools

Tools that operate from the terminal, can read/write files and run
commands directly, and are suited to more autonomous, multi-step work.

### Claude Code

| | |
|---|---|
| **Category** | CLI coding agent |
| **Strengths** | Strong multi-step task execution, direct file system and shell access, good at large refactors and codebase-wide tasks with appropriate review checkpoints |
| **Weaknesses** | Terminal-based workflow has a learning curve for developers used to GUI-first tools; autonomy requires disciplined review habits |
| **Platform** | macOS, Windows, Linux (terminal); also available via desktop app |
| **Best use cases** | Large refactors, multi-file features, repository-wide tasks, automation scripts |
| **Alternatives** | Other CLI-based coding agents in this fast-moving category |

> For current, authoritative details on any Anthropic product
> (capabilities, pricing, availability), check
> [docs.claude.com](https://docs.claude.com) directly — this repository
> avoids restating fast-changing product specifics that go stale.

## Category: Inline Coding Assistants

Tools focused on in-editor autocomplete/suggestion rather than
full agentic workflows.

### GitHub Copilot

| | |
|---|---|
| **Category** | Inline coding assistant / chat |
| **Strengths** | Broad IDE support (VS Code, JetBrains, Neovim, etc.), mature autocomplete, integrated chat and PR-review features |
| **Weaknesses** | Historically weaker at large, autonomous multi-file tasks compared to dedicated agentic tools |
| **Platform** | Most major IDEs via extension |
| **Best use cases** | Autocomplete-heavy workflows, teams standardized on GitHub's ecosystem |
| **Alternatives** | Cursor, Windsurf, model-specific IDE extensions |

## How to Use This Directory

1. Identify your workflow type first (autocomplete vs. IDE-integrated
   vs. agentic/CLI) — see
   [AI Coding Fundamentals](../docs/02-fundamentals/README.md#autocomplete-vs-chat-vs-agentic-coding).
2. Compare 2-3 candidates within that category on your actual tasks, not
   just the table above.
3. Re-check pricing directly with the vendor — this space changes
   monthly.

## Contributing a Tool Entry

Use this template and see [CONTRIBUTING.md](../CONTRIBUTING.md):

```markdown
### Tool Name

| | |
|---|---|
| **Category** | |
| **Strengths** | |
| **Weaknesses** | |
| **Pricing** | (with "last verified" date) |
| **Platform** | |
| **Best use cases** | |
| **Alternatives** | |
```

Last reviewed: 2026-07-29.
