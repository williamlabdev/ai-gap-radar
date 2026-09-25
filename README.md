# ai-gap-radar

Builder's radar for AI repos: **what blew up, why, and what's missing.**

Most awesome-lists collect links. This repo collects **judgment** — every entry answers three questions: What does it do? Why did it blow up? What gap does it leave open?

- Cadence: biweekly (radar snapshot every 2 weeks)
- Language: English first; each brief ends with a 3-line 中文判斷 for the maintainer
- Scope: AI agent stack — skills, coding CLIs, MCP infra, gateways, vertical micro-agents
- Rule: implementation code lives in **separate** new repos. This repo only produces `opportunities/*.md` + a link back once a project spins off.

## Structure

```
README.md                  # purpose + method + latest conclusions
radar/YYYY-MM-Wn.md        # biweekly snapshot: stars / weekly growth / lang / license / category
briefs/_TEMPLATE.md        # one-page analysis template
briefs/*.md                # one page per hot repo (300-500 words, verdict first)
opportunities/_TEMPLATE.md # spin-off proposal template
opportunities/*.md         # buildable gaps (pain, competitors, differentiation, MVP, validation)
```

## Latest: 2026-09-W4 — Skills governance (first issue)

August–September 2026 data is unambiguous: the agent-skills explosion entered its **governance phase**. Three signals landed the same week:

1. `NVIDIA/SkillSpector` — scanner reporting ~26% of skills contain vulnerabilities
2. `cloudflare/security-audit-skill` — Cloudflare's official multi-stage security audit skill
3. `anthropics/launch-your-agent` — Anthropic's managed-agent onboarding skills

Meanwhile `mattpocock/skills` (+11.8k/week) and `obra/superpowers` keep growing, and users now pick skills by **author brand**, not feature lists. Distribution is solved; **trust is not**. That's the gap this issue tracks.

Top 5 to read first: `briefs/mattpocock-skills.md`, `briefs/obra-superpowers.md`, `briefs/nvidia-skillspector.md`, `briefs/cloudflare-security-audit-skill.md`, `briefs/anthropics-launch-your-agent.md`. Buildable gap: `opportunities/skill-security-linter.md`.

## Method

- Sources: GitHub Trending, Trendshift, OSSInsight, ShareuHack weekly, HN
- Columns per repo: total stars / weekly star growth / language / license / category
- Star counts are point-in-time (see snapshot date). Growth figures are lower bounds (GitHub public events feed has been incomplete since 2026-05-01).
- Verdicts are builder-biased: we care about what is clonable, embeddable, or monetizable.

## Contributing

PRs welcome for: corrections to snapshots, new briefs following `_TEMPLATE.md`, new opportunities with evidence (competitor README links + issue pain). Keep briefs under 500 words.

## License

CC0-1.0 — fork it, republish it, build on it.
