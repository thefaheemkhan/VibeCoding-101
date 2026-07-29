# Pull Request Checklist (AI-Assisted Code)

Use this before merging any AI-generated or AI-assisted change.

## Understanding
- [ ] I have read the full diff, not just the summary.
- [ ] I understand every change well enough to explain it to someone
      else.

## Correctness
- [ ] The change was actually run/tested, not just reviewed visually.
- [ ] Edge cases were considered (empty input, large input, concurrent
      access, etc.).
- [ ] Tests were added or updated for new/changed behavior.

## Security (see [Security](../docs/18-security/README.md))
- [ ] No hardcoded secrets or credentials.
- [ ] All queries are parameterized (no string-concatenated SQL/commands).
- [ ] Input validation exists for all new external inputs.
- [ ] Authorization checks are correct for any new/changed endpoints.

## Scope & Architecture
- [ ] The change stays within its intended scope (no unrelated
      refactors bundled in).
- [ ] It's consistent with existing project conventions and patterns.
- [ ] No unfamiliar library/API calls were used without verifying they
      exist and behave as expected.

## Documentation
- [ ] Any new public function/endpoint is documented.
- [ ] README/docs updated if behavior visible to users changed.

Related: [Common Mistakes](../docs/25-common-mistakes/README.md)
