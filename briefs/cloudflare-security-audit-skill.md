## Repo

- Name: cloudflare/security-audit-skill
- URL: https://github.com/cloudflare/security-audit-skill
- Stars (as of 2026-09-25, verified via GitHub API): ~21.4k
- Weekly growth: launched ~0.5k (June) → 21.4k by late Sept; last push 2026-09-14
- Language / License: JavaScript / MIT
- Category: skill (security audit)

## What (2-3 sentences)

Cloudflare's official multi-stage security-audit skill for coding agents. Encodes the vendor's audit playbook as an installable skill rather than a SaaS product.

## Why it blew up

- Distribution path: Cloudflare official + "vendor playbook as skill" novelty + new-repo Trending slot.
- Data point: from ~0.5k at June launch to 21.4k by late Sept (~40x) — the strongest governance-demand signal in this issue.
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
