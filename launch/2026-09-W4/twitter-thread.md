# Twitter thread — W4 skills governance (10 tweets, post same day as dev.to)

## 1 (hook)
A Cloudflare security skill went 0.5k → 21.4k stars in 3 months (~40x). NVIDIA found 26% of agent skills have vulns. The agent-skills boom just entered its governance phase. Data 🧵

## 2
Context: mattpocock/skills (~269k stars) and obra/superpowers (~291k) proved distribution is solved. Users now pick skills by author brand, not feature lists. Everyone has skills. Nobody trusts them.

## 3
Signal 1: NVIDIA/SkillSpector (~18k) — a scanner reporting ~26% of sampled skills contain vulnerabilities. It put a quotable number on the fear: every SKILL.md install is unsigned code execution.

## 4
Signal 2: cloudflare/security-audit-skill (~21k) — a vendor audit playbook shipped AS a skill, up ~40x since June. "Playbook-as-skill" is now official distribution.

## 5
Signal 3: anthropics/launch-your-agent — idea-to-managed-agent onboarding. Platforms are splitting layers. Vercel ships the framework (Eve). Anthropic runs the hosting. Cloudflare owns the audit.

## 6
The gap: scanners tell you something is wrong. Nobody tells you whether to install, fixes the obvious parts, or gives you a badge to require in PRs. Detection without a trust gate.

## 7
Missing loop: lint → sandbox trial-run → permission manifest → 0-100 score + badge → CI gate. The "eslint moment" for skills. Neutral, single binary, vendor-independent.

## 8
I turned this into a public research repo: biweekly radar, one-page briefs with verdicts, buildable "opportunities" with MVP scopes. First issue = skills governance. github.com/williamlabdev/ai-gap-radar

## 9
Full write-up with numbers + links: [dev.to URL]. Corrections welcome — that's the point of a radar.

## 10 (CTA)
Validation rule is public: if 5+ teams say "run this on my skills repo," I build the linter (single binary + GitHub Action). Star + open an issue.
