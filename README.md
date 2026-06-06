# fact-check

A Claude [Agent Skill](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills)
for rigorous, data-first fact-checking and source verification.

## What it does

- **Data before journalism** — verifies claims against hard data (exchanges, central
  bank and regulatory filings, vessel tracking, trade-flow databases, official
  statistics) before treating news reports as evidence.
- **Multi-tier cross-referencing** — requires corroboration across at least 3 sources
  spanning 2+ tiers (wire, local/trade, official, social, OSINT, expert), searched in
  both the source language and English.
- **Government skepticism** — treats official statements as claims, not facts, and flags
  amplification, circular sourcing, and shifting baselines.
- **Calibrated verdicts** — every result carries an explicit confidence level, verdict,
  data check, and the corroboration/discrepancies behind it.
- **Review mode** — for "is X good / should I buy X" questions, trust inverts: the vendor
  becomes the least-trusted source, and user-supported evidence (forums, long-term-use
  reports, independent benchmarks) is prioritized while astroturfing is flagged.

## Install

Copy or symlink this repository into your skills directory as `fact-check`:

```sh
git clone git@github.com:chakrit/fact-check.git ~/.claude/skills/fact-check
```

The skill triggers automatically when you ask Claude to verify, debunk, or confirm a
claim, statistic, or news story — or to assess whether a product or service is actually
good.

## License

See [LICENSE](./LICENSE).
