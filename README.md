# Lucy Voice Bot — QA Report Dashboard

**An interactive report that turns voice-bot test results into a clear view for leadership and the vendor: headline stats, per-tester scores, failure patterns, and prioritized action items.**

[Live demo](https://piperintech.github.io/lucy-test-dashboard/report.html) · Companion to the [QA test harness](https://github.com/piperintech/snap-lucy-test)

---

## What it shows

- **Headline stats:** calls completed, claims created, data loss rate, average ease-of-call and bot ratings, field-level capture rates
- **Gravity scale:** each tester's call scored by severity of what went wrong
- **Patterns:** failures that repeated across calls (systemic issues vs. one-offs)
- **Recommendations:** a prioritized action list for the vendor

## How it works

`report.html` loads `report.json` and renders everything client-side. To run a new round, swap in a new `report.json`; the layout doesn't change.

```
report.json
├── meta              round, dates, prepared by/for
├── summary           overview + stat cards
├── testers           per-tester results
├── patterns          recurring failures
└── recommendations   action items
```

## Why it matters

The test surfaced systemic data-capture gaps that a few spot-check calls would never have shown. The report gave the vendor a concrete, prioritized fix list before go-live.

## Stack

HTML, CSS, vanilla JavaScript (`fetch` + templating) · JSON data file · GitHub Pages

> Tester names are anonymized and claim details are fictional.

---

Built by **Manuela Gonzalez Piper** · Product & AI · [GitHub](https://github.com/piperintech)
