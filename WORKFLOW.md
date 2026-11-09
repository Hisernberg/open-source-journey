# WORKFLOW — The Daily Operating System

This is the standard operating procedure for every contribution day. The goal is not "10 open PRs a day" — it is **10 high-quality touchpoints** with target projects: merged PRs, reviews, reproductions, well-scoped issues. Volume only counts when it survives maintainer review.

---

## 1. Daily rhythm (Dhaka time)

| Time | Block | What happens |
|---|---|---|
| 07:30 | Triage | Open the daily checklist issue. Read the morning sprint plan. Pick 4 S / 4 M / 2 L. Check the state of every open PR (new review comments?). |
| 08:00–09:30 | Small block 1 | 2 smalls, landed end-to-end (branch → commit → PR). |
| 10:00–10:45 | Small block 2 | 2 more smalls. |
| 11:30–13:00 | Medium block 1 | Reproduce the bug, write the failing test, implement the fix. |
| 15:00–16:30 | Medium block 2 | Same. Or push a medium forward from yesterday. |
| 17:30–19:30 | Large block | Deep work on the 2 rolling large arcs (feature, optimization with benchmark, new model support). |
| 20:30–21:00 | Close | Reply to every review comment. Update `tracker/contributions.csv`. Write `logs/YYYY-MM-DD.md`. Commit + push. Close the daily issue. |

Anything unfinished rolls over to the next day — **rolling is fine, rushing is not**.

---

## 2. Contribution size definitions

### Small (≤ 1 hour, land same day)
- Docs: fix an incorrect example, translate a missing section note, clarify an ambiguous docstring.
- Tests: add a missing test case, reproduce a reported edge case.
- Tiny fixes: typo clusters in one file, broken links, deprecated flag removal.
- Triage: reproduce a bug comment with a minimal snippet, confirm version ranges, label requests.

### Medium (a few hours – 2 days)
- Bug fix with reproduction: failing test first, then the fix, then the regression note.
- Single-module feature: a new transform, a CLI flag, a config option.
- Benchmarks: add a missing benchmark entry, compare two implementations, record results in the project's format.
- Error messages: turn a cryptic traceback into an actionable one (with docs).

### Large (5–10 day arcs, max 2 concurrent)
- New model / new backend support in a framework (transformers, sherpa-onnx, OpenCV).
- Performance optimization with before/after benchmarks and a reproducible script.
- Multi-file feature: new pipeline stage, new eval task, new dataset loader.
- A well-researched design proposal or RFC when maintainers invite one.

---

## 3. Quality gates — every PR, no exceptions

1. **Read `CONTRIBUTING.md` and the PR template first.** Many projects require issue linkage, DCO sign-off, or specific commit formats.
2. **Search open/closed PRs** for the same fix. Duplicate PRs are the fastest way to look bad.
3. **Link the issue** (`Fixes #1234`) or, if none exists, comment on the related issue first.
4. **One logical change per PR.** Never mix a typo fix with a feature.
5. **Tests pass locally** before pushing; run the project's linter (`pre-commit`, `ruff`, `clang-format` — whatever they use).
6. **Description follows the template** in [`templates/pr-description.md`](templates/pr-description.md).
7. **Draft PR early** for anything > 1 day so maintainers can course-correct.
8. **Never mass-open PRs across unrelated repos in one day** — sustained, focused work in the portfolio reads as genuine; spray-and-pray reads as spam and gets accounts flagged.

---

## 4. PR lifecycle management

| State | Rule |
|---|---|
| Review comment received | Respond within **24 hours**, even if just "working on it". |
| No review after 7 days | Polite ping: one comment, @-mention a reviewer who usually reviews this area. |
| No review after 14 days | Move on; note it in the daily log; re-ping in the next Sunday session. |
| Changes requested | Same-day turnaround if small; otherwise top priority the next day. |
| Closed (not merged) | Read the reason, extract the lesson into the daily log, never argue. |
| Merged | Update CSV status, add the repo to the "wins" section of the weekly review. |

**Sunday is review-and-ping day:** no new PRs. Clear the review backlog, close finished business, plan next week's larges, write the weekly review from [`templates/weekly-review.md`](templates/weekly-review.md).

---

## 5. Logging (the non-negotiable 20 minutes)

Every contribution gets a row in `tracker/contributions.csv`:

```csv
date,org_repo,url,type,size,title,status,merged_at,notes
2026-11-10,huggingface/transformers,https://github.com/huggingface/transformers/pull/0000,PR,small,Fix wrong arg name in BertGeneration docs,open,,
```

- `type`: `PR` | `issue` | `review` | `triage`
- `size`: `small` | `medium` | `large`
- `status`: `open` | `changes-requested` | `merged` | `closed` | `parked`

Weekly KPIs are computed from this file — no log, no credit. The daily log (`logs/YYYY-MM-DD.md`, from [`templates/daily-log.md`](templates/daily-log.md)) records the *why*: what worked, what blocked, what to do tomorrow.

---

## 6. Communication rules

- Ask sharp questions with evidence (minimal repro, versions, logs) — never "it doesn't work".
- Never argue a close; ask what would make the change acceptable instead.
- Credit others: mention the issue reporter, co-commenters, prior PR attempts.
- In GSoC org channels (Discord/Slack/Zulip/mailing lists): introduce yourself once, then be useful in public threads — mentors notice who answers other newcomers.
