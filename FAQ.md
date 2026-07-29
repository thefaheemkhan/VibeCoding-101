# Frequently Asked Questions

### What is "vibe coding," precisely?

Building software primarily through natural-language collaboration with
an AI model — describing intent, reviewing generated code, and
iterating — rather than writing every line manually. It does not mean
skipping review, testing, or architecture. See
[docs/01-introduction](docs/01-introduction/README.md).

### Is vibe coding only for beginners or small projects?

No. The techniques scale from a weekend prototype to production systems,
but the *practices* around it (planning, review, testing, security)
matter more, not less, as the stakes go up. This repository treats vibe
coding as a professional skill, not a shortcut.

### Do I need to know how to code to use AI coding tools well?

You'll get much further if you can read code, reason about
architecture, and evaluate correctness — even if you rarely type code by
hand. AI models make mistakes confidently. Understanding what "good"
looks like is what lets you catch them. Start with
[docs/02-fundamentals](docs/02-fundamentals/README.md).

### Which AI model or tool should I use?

There is no single right answer — it depends on task type, budget, and
workflow (chat vs. IDE-integrated vs. CLI agent). See
[docs/03-ai-models](docs/03-ai-models/README.md) and
[awesome-tools/](awesome-tools/) for structured comparisons instead of a
single recommendation.

### Why isn't this repository just a list of tools and links?

Because link lists go stale immediately and teach nothing about
judgment. This repository explains *why* a tool or technique works, when
to use it, and what the trade-offs are, so the reasoning stays useful
even after specific tools change. See the rationale in the root
[README](README.md#why-this-repository-exists).

### How current is the tool/pricing information?

Tools and pricing change fast. Every entry in `awesome-tools/` is dated
with a "last verified" note. Always double-check pricing on the vendor's
site before making a purchasing decision — see
[LEGAL_AND_FINANCIAL note in CONTRIBUTING.md](CONTRIBUTING.md#style-guide).

### Can I use these prompt templates commercially?

Yes. Everything in this repository is MIT licensed — see
[LICENSE](LICENSE). Attribution is appreciated but not legally required
beyond the license terms.

### How do I contribute a new page or fix an error?

See [CONTRIBUTING.md](CONTRIBUTING.md). Short version: no placeholders,
follow the page template, cross-link your addition, and open a PR.

### Is this repository affiliated with any AI company?

No. It is community-maintained and vendor-neutral. Tool comparisons
reflect strengths and weaknesses, not sponsorship.

### Something is outdated or wrong. What do I do?

Open a GitHub Issue with the page link and what's wrong. Outdated
tool/pricing info is one of the most valuable things you can report.
