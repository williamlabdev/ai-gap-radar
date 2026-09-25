## Repo

- Name: NVIDIA/SkillSpector
- URL: https://github.com/NVIDIA/SkillSpector
- Stars (as of 2026-09-25): ~9.8k
- Weekly growth: +3.3k (June)
- Language / License: Python / —
- Category: skill (security scanner)

## What (2-3 sentences)

Scanner for agent skills reporting that ~26% of sampled skills contain vulnerabilities. Flags risky patterns in skill instructions and bundled scripts before you install them into a coding agent.

## Why it blew up

- Distribution path: NVIDIA brand + a scary, quotable number (26%) + HN-grade security discourse.
- Data point: +3.3k stars in one week as a brand-new repo.
- Timing: landed exactly as enterprises started asking "can we allow skills on company machines?" — first credible answer.

## License & risk

Check license before vendoring. Risk: scanner-only, no fix, no policy enforcement, no CI gate.

## Gap (what it leaves open — the part that matters for this repo)

Detection without remediation or scoring-for-trust. Nobody mints a badge, nobody blocks `npx skills add` on failure, nobody auto-suggests minimal-permission rewrites. That full loop (lint → sandbox run → score → badge → CI gate) is the spin-off: `opportunities/skill-security-linter.md`.

## Links

- Repo: https://github.com/NVIDIA/SkillSpector

## 給自己的判斷（3 行中文）

- 它驗證了需求，但只做了一半（掃描），後半（修復+評分+閘門）是空的。
- 不要重做掃描器，做掃描器之後的那一層。
- 它的規則集是最好的冷啟動語料。
