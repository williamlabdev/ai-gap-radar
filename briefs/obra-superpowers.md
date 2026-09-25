## Repo

- Name: obra/superpowers
- URL: https://github.com/obra/superpowers
- Stars (as of 2026-09-25): ~276k
- Weekly growth: +~0.6k/day on Trending
- Language / License: Shell / MIT-ish
- Category: skill

## What (2-3 sentences)

Agentic skills framework plus a software-development methodology that claims to actually work with coding agents. Skills + conventions for planning, executing, and reviewing agent-driven development.

## Why it blew up

- Distribution path: GitHub Trending #1-row regular, strong word-of-mouth among Claude Code users.
- Data point: 276k stars, 24.7k forks — one of the highest-starred agent repos ever.
- Timing: same skills wave as mattpocock/skills, but positioned as methodology (system) rather than collection (parts).

## License & risk

Permissive license. Same systemic risk as all skill collections: untrusted markdown + scripts executed by agents with broad tool permissions.

## Gap (what it leaves open — the part that matters for this repo)

Methodology without verification. No conformance test ("does this agent setup follow the methodology?"), no red-team skill, no audit trail. Governance tooling can treat superpowers-style repos as first-class test targets.

## Links

- Repo: https://github.com/obra/superpowers

## 給自己的判斷（3 行中文）

- 方法論型 skill 比單點 skill 更黏，但也更難審。
- 可借鑑它的文件結構來寫 linter 規則。
- 不要正面做競品，做它的檢測器。
