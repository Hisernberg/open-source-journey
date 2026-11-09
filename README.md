# 🚀 Open Source Journey — AI/ML Daily Contribution System

[![Daily Sprint](https://github.com/Hisernberg/open-source-journey/actions/workflows/daily-plan.yml/badge.svg)](https://github.com/Hisernberg/open-source-journey/actions/workflows/daily-plan.yml)

> **Mission:** land **10 meaningful contributions every day — 4 small · 4 medium · 2 large** — across LLM, Computer Vision, NLP and Audio/Speech. Strategic targets: **Google Summer of Code 2027**, the **Claude for Open Source program**, and long-term ecosystem reputation.
>
> **Window:** November 10, 2026 → January 31, 2027 (GSoC pre-season) → applications Mar 18 – Apr 2, 2027.

**Owner:** [@Hisernberg](https://github.com/Hisernberg) · **Fields:** LLM · CV · NLP · Audio · full AI/ML

---

## 📂 Repo map

| Path | What it is |
|---|---|
| [`WORKFLOW.md`](WORKFLOW.md) | The daily operating system: 4-4-2 rule, time blocks, quality gates, PR lifecycle |
| [`ROADMAP.md`](ROADMAP.md) | 12-week master plan (W1–W12), GSoC 2027 timeline, Claude OSS qualification path |
| [`targets/`](targets/) | The curated portfolio: GSoC orgs + ~80 repos by domain (LLM / CV / NLP / Audio / top labs) |
| [`tracker/contributions.csv`](tracker/contributions.csv) | One row per contribution — the single source of truth for KPIs |
| [`templates/`](templates/) | Daily log, PR description, weekly review templates |
| [`logs/`](logs/) | One dated log per day (what was planned, what landed, lessons) |
| [`.github/workflows/daily-plan.yml`](.github/workflows/daily-plan.yml) | GitHub Action that opens a **daily checklist issue at 07:30 (Asia/Dhaka)** |

---

## ⚡ The daily loop

| Slot | Size | Definition | When |
|---|---|---|---|
| Morning triage | — | Read the daily issue, pick 10 targets, check PR states | 20 min |
| Block 1 | 4 × Small | docs, typo clusters, test cases, one-line fixes — **land same day** | 2 × 45 min |
| Block 2 | 4 × Medium | bug + repro + fix, single-module feature, benchmark — 1–3 day arcs | 2 × 90 min |
| Block 3 | 2 × Large | multi-file features, optimizations with benchmarks, new model support — 5–10 day rolling arcs | deep work |
| Evening close | — | Respond to every review <24h, log CSV, commit daily log, push | 20 min |

**Quality gates (non-negotiable):** read CONTRIBUTING first · search for duplicate PRs · link the issue · tests pass · one logical change per PR · mediums/larges roll over rather than get rushed · Sunday = review-and-ping day, no new PRs.

---

## 🎯 Portfolio rule

**3 primary orgs** (5+ merged PRs each by January) + 3 secondaries + satellites.

Recommended primaries to start: **huggingface/transformers**, **opencv/opencv**, **k2-fsa/sherpa-onnx**.

Start points: each repo's `/contribute` page (e.g. [github.com/huggingface/transformers/contribute](https://github.com/huggingface/transformers/contribute)) lists `good first issue`s automatically.

---

## 📊 KPIs by Jan 31, 2027

| KPI | Target |
|---|---|
| Total contributions opened | ≥ 400 |
| Merged PRs | ≥ 100 |
| Orgs with 5+ merged PRs | ≥ 3 |
| Large PRs merged | ≥ 2 |
| Repo stars / external contributors (this repo) | ≥ 5 |

---

## 🤖 Automation

1. **Daily issue** — the Action opens "Daily Sprint — YYYY-MM-DD" at 07:30 Dhaka time with the 4-4-2 checklist. Fill it in as you go, close it when done.
2. **Daily sprint plan** — a scheduled assistant session every morning researches live, open issues across the portfolio and posts 10 verified targets.
3. **Keep the Action alive** — GitHub disables scheduled workflows after 60 days without repo activity; the daily log commit resets that clock.

---

## 🔐 Security

No secrets live in this repo, ever. See [`SECURITY.md`](SECURITY.md) for token hygiene rules and the rotation checklist.
