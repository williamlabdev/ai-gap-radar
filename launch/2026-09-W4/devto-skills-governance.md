---
title: "Agent Skills Solved Distribution. Trust Is the Missing Layer."
published: false
tags: ai, opensource, github, llm
---

Agent skills had their explosion. `mattpocock/skills` sits at ~269k stars, `obra/superpowers` at ~291k. Every coding agent — Claude Code, Cursor, Codex, OpenCode — now consumes `SKILL.md` files. Distribution is solved.

But here's what happened over the summer of 2026: the skills boom entered its **governance phase**. Three signals landed within weeks of each other, and together they point at the same missing layer.

## Signal 1: NVIDIA put a number on the fear

[NVIDIA/SkillSpector](https://github.com/NVIDIA/SkillSpector) (~18k stars) is a scanner for agent skills, and it came with a quotable finding: **~26% of sampled skills contain vulnerabilities**. Every `SKILL.md` install is unsigned code execution on a machine that holds real credentials — and until now, nobody had measured how bad it was.

## Signal 2: Cloudflare shipped a playbook as a skill

[cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill) went from ~0.5k stars at its June launch to **~21.4k by late September — roughly 40x in three months**. A vendor's security audit playbook, distributed not as SaaS but as an installable skill. "Playbook-as-skill" is now an official distribution channel.

## Signal 3: Anthropic owns the onboarding path

[anthropics/launch-your-agent](https://github.com/anthropics/launch-your-agent) guides you from an agent idea to a live managed agent. Read it alongside Vercel's Eve ("Next.js for agents") and the pattern is clear: **platforms are splitting the agent stack into layers** — framework, hosting, security. Each vendor claims one layer.

## The gap: detection without a trust gate

Scanners tell you something is wrong. Nobody tells you:

- Should I install this skill? (score)
- Can it prove it's safe? (badge)
- Can my team require that proof in PRs? (CI gate)
- Can the obvious issues fix themselves? (minimal-permission rewrites)

That's the missing loop: **lint → sandbox trial-run → permission manifest → 0–100 score + badge → CI gate**. The "eslint moment" for skills. Neutral, single-binary, vendor-independent.

## What I'm doing about it

I started [ai-gap-radar](https://github.com/williamlabdev/ai-gap-radar), a public biweekly research repo with a simple rule: *hot repos are evidence, buildable gaps are conclusions.* Each issue has a star-velocity radar, one-page briefs with verdicts, and `opportunities/` — gaps concrete enough to ship, with competitor tables and 2-week MVP scopes.

The first issue tracks skills governance, and its first opportunity is a [skill security linter](https://github.com/williamlabdev/ai-gap-radar/blob/dev/opportunities/skill-security-linter.md). My validation rule is public: if 5+ teams say "run this on my skills repo," I build it. Otherwise it stays a proposal.

Corrections welcome — that's what a radar is for.
