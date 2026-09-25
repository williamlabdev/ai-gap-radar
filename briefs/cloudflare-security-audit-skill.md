## Repo

- Name: cloudflare/security-audit-skill
- URL: https://github.com/cloudflare/security-audit-skill
- Stars (as of 2026-09-25): ~0.5k (new, June 2026)
- Weekly growth: new-repo velocity
- Language / License: JavaScript / —
- Category: skill (security audit)

## What (2-3 sentences)

Cloudflare's official multi-stage security-audit skill for coding agents. Encodes the vendor's audit playbook as an installable skill rather than a SaaS product.

## Why it blew up

- Distribution path: Cloudflare official + "vendor playbook as skill" novelty + new-repo Trending slot.
- Data point: top-15 new repo in its launch week despite <1k stars.
- Timing: same governance week as SkillSpector and Anthropic's managed-agent onboarding — platforms claiming the trust layer.

## License & risk

Vendor-owned; portability risk if the skill assumes Cloudflare infra. But the pattern (playbook-as-skill) is clonable for any domain.

## Gap (what it leaves open — the part that matters for this repo)

Single-vendor, single-playbook. No cross-vendor baseline, no comparison scoring, no "which audit skill should I trust?" layer. A neutral linter/scoreboard that rates audit skills themselves is missing.

## Links

- Repo: https://github.com/cloudflare/security-audit-skill

## 給自己的判斷（3 行中文）

- 大廠下場寫 skill = skill 已成官方通路，值得重押。
- 但大廠只會寫自家的，中立評測永遠是第三方機會。
- 抄它的結構，評它的分數。
