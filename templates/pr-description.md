# PR Description Template

Copy into every pull request; delete sections that do not apply.

```markdown
## What does this PR do?
<!-- One sentence. -->

## Why? / Linked issue
<!-- Fixes #1234  (or: addresses part of #5678) -->

## Changes
- <!-- bullet list of concrete changes, one logical change per PR -->

## How was this tested?
<!-- commands run, tests added, before/after outputs -->

## Checklist
- [ ] Read CONTRIBUTING.md and the PR template
- [ ] Searched for duplicate PRs
- [ ] Tests added/updated and passing locally
- [ ] Linter / formatter run (`pre-commit run -a` or project equivalent)
- [ ] Docs updated where behavior changed
```

**Subject line format (most projects):** `area: imperative summary (#issue)`
Examples: `docs: fix wrong argument name in BertGeneration`, `fix(tokenizer): handle empty prefix in fast tokenizer (#1234)`.

**DCO/CLA:** if the project requires `Signed-off-by`, commit with `git commit -s`.
