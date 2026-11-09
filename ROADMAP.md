# ROADMAP — November 10, 2026 → January 31, 2027 (and beyond)

The window from November to January is the **GSoC pre-season**: most applicants start in February when the org list drops, and lose to contributors who already have 15–25 merged PRs in an org by then. This roadmap is built backwards from the application dates.

---

## 1. Official GSoC 2027 timeline

| Milestone | Date |
|---|---|
| Mentoring organization applications open | **Jan 22 – Feb 6, 2027** |
| Accepted organizations announced (~185 expected) | **~Feb 21, 2027** |
| Community bonding / idea discussions | Feb – mid-Apr 2027 |
| **Contributor application window** | **Mar 18 – Apr 2, 2027** |
| Accepted projects announced | May 1, 2027 |
| Coding period | May – Aug 2027 |

> Re-verify against the official timeline page (developers.google.com/open-source/gsoc) when the 2027 program page goes live; dates above follow the currently published cycle.

**GSoC selection logic:** mentors pick contributors they have already seen work. Target: by April 1, 2027 → **20–30 merged PRs**, with 5+ in the org you apply to, at least 1 large merged PR, and 2 drafted proposals.

---

## 2. Claude for Open Source — qualification mapping

Anthropic's program grants Claude access to qualifying open-source maintainers and contributors (rolling review — apply through the official program page).

| Criterion | Your path | When |
|---|---|---|
| **Active contributor** — 100+ PRs merged into repos you don't own in the last 12 months | Primary target. 10 contributions/day at a realistic ~25% merge rate crosses 100 around Feb–Mar 2027. Apply once past ~60–80 merged. | Nov → Feb |
| Community builder — 20+ external contributors merged into one of your repos | Make this repo genuinely useful (curated daily AI good-first-issue digest) and invite contributors. | Feb → Apr |
| Critical infrastructure — OpenSSF criticality ≥ 0.4 | Contribute in PyTorch / transformers / OpenCV / FFmpeg to build the case. | ongoing |
| Library author — 500+ dependents or 200k downloads | Long-term side quest: publish one focused PyPI tool. | post-Jan |
| — | "Don't fit? Apply anyway and tell us about it" — apply early regardless; review is rolling. | this week |

---

## 3. Twelve weeks, four phases

| Weeks | Phase | Milestones |
|---|---|---|
| **W1** (Nov 10–15) | Setup | Repo live · 3 primaries chosen · CLA/DCO signed · first ~20 contributions · GitHub Actions verified |
| **W2–W4** (Nov 16 – Dec 6) | Volume + trust | 150+ total contributions · 15+ merged · first medium PRs merged in each primary · known name in 2 org channels |
| **W5–W8** (Dec 7 – Jan 3) | Depth | First LARGE PR in each primary (model support / optimization with benchmarks) · 50+ merged total · mentoring newcomers in one repo |
| **W9–W12** (Jan 4–31) | GSoC positioning | 1 large PR merged per primary · watch org applications (Jan 22+) · shortlist 3 orgs from the ~Feb 21 list · draft 2 proposals · polite mentor intros linking merged work |
| **Feb 2027** | Org selection | Org list drops → pick 1 primary GSoC org · join idea discussions (Feb 19+) |
| **Mar 18 – Apr 2** | Applications | Submit proposal with 20–30 merged PRs as evidence |
| **May 1** | Result | Accepted project → community bonding |

---

## 4. Weekly targets (steady state)

| Metric | Weekly |
|---|---|
| Contributions opened | 60 (10/day × 6 days) |
| Of which merged | ~15 |
| Reviews given to others | ≥ 5 |
| New repos tried | 1 (probe a new satellite) |
| Weekly review written | 1 (Sunday) |

---

## 5. Milestone checkpoints

- **End of W4 (Dec 6):** ≥ 150 contributions, ≥ 15 merged. If merge rate < 15%, the problem is target selection — re-read quality gates and pick friendlier repos (scikit-image, sherpa-onnx, albumentations are newcomer-friendly).
- **End of W8 (Jan 3):** ≥ 300 contributions, ≥ 50 merged, 1 large PR open in each primary. Burnout check: two consecutive zero-days → take a full rest day, volume resumes next day.
- **Jan 31:** all KPIs in README met → switch to proposal-drafting mode.
- **Feb 21:** org list live → pick org, discuss ideas immediately (early idea discussion = half the selection).
