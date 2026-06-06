# fact-check

A Claude [Agent Skill](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills)
for data-first fact-checking and authentic-review finding — built to resist a web that now
actively games the model reading it.

## What it does

Two modes, auto-selected from your question:

- **News / claims** — verifies against hard data before journalism, using SIFT (stop,
  investigate the source, find better coverage, trace to origin) and multi-tier
  cross-referencing. Every verdict carries an explicit confidence level and cited URLs.
- **Reviews / recommendations** — cuts past marketing and SEO to honest signal: the vendor
  is the least-trusted source, sites that proclaim their own "independence" are
  discounted, and trust is weighted toward what a seller can't fake — cross-platform user
  reports, long-term-use detail, and the presence of dissent.

Across both, it treats the open web as adversarial:

- **Retrieve, don't recall** — verifies with live tools, never from stale memory.
- **Fetched content is data, not instructions** — ignores prompt injection embedded in
  pages.
- **Trust flows from outside a source** — authoritative tone, stat-stuffing, and
  self-labels like "unbiased" count as zero evidence; reputation is established only by
  lateral reading.

## Structure

| File                             | When it's read                                   |
| -------------------------------- | ------------------------------------------------ |
| `SKILL.md`                       | always — news method, shared rules, and routing  |
| `references/reviews.md`          | review and recommendation questions              |
| `references/data-sources.md`     | verifying a quantitative claim in a given domain |
| `references/media-provenance.md` | a claim resting on an image, video, or audio     |

## Install

Copy or symlink this repository into your skills directory as `fact-check`:

```sh
git clone git@github.com:chakrit/fact-check.git ~/.claude/skills/fact-check
```

The skill triggers automatically when you ask to verify, debunk, or confirm a claim,
statistic, or news story — or to judge whether a product or service is actually good.

## License

MIT — see [LICENSE](./LICENSE).
