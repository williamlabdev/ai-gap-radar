## Repo

- Name: anthropics/launch-your-agent
- URL: https://github.com/anthropics/launch-your-agent
- Stars (as of 2026-09-25): ~0.5k (new, June 2026)
- Weekly growth: new-repo velocity
- Language / License: HTML (docs/skills) / —
- Category: skill (onboarding)

## What (2-3 sentences)

End-to-end guide + skills for going from an agent idea to a live managed agent. Onboarding path into Anthropic's agent hosting rather than a standalone tool.

## Why it blew up

- Distribution path: Anthropic official + new-repo Trending + platform-strategy commentary (Vercel Eve for framework, Anthropic for hosting, Cloudflare for security — same week).
- Data point: top-15 new repo in launch week.
- Timing: marks the shift from "personal-agent experiments" to "platform-owned agent infra."

## License & risk

Docs-led repo; platform-coupling risk (happy path ends on Anthropic infra). Low direct reuse risk, high strategic signal value.

## Gap (what it leaves open — the part that matters for this repo)

Onboarding without trust evidence. It tells you how to ship, not how to prove your agent/skills are safe. A pre-launch gate (lint + vuln scan + permission manifest + score badge) slots directly into this path as the missing step before "launch."

## Links

- Repo: https://github.com/anthropics/launch-your-agent

## 給自己的判斷（3 行中文）

- 平台只管讓你上線，不管讓你可信——可信層是獨立機會。
- 最好的發布策略是做它上線流程的外掛，而不是競品。
- 盯著它的下一步（審核？市集？），提前卡位。
