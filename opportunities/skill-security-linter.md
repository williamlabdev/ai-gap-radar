## Pain (who hurts, how often)

Team leads and solo devs installing agent skills (Claude Code / Cursor / Codex / OpenCode) into machines with real credentials. Every `SKILL.md` install is unsigned code execution, yet there is no `eslint moment` for skills. NVIDIA's SkillSpector says ~26% of sampled skills have vulns — but it only scans. (Evidence: `../briefs/nvidia-skillspector.md`, `../briefs/mattpocock-skills.md`.)

## Competitors (with links — what exists today)

| Competitor | Stars | What it does | What it lacks |
|---|---|---|---|
| https://github.com/NVIDIA/SkillSpector | 9.8k | Vuln scanner for skills | No fix, no score/badge, no CI gate |
| https://github.com/cloudflare/security-audit-skill | ~0.5k | Single-vendor audit playbook as skill | Single playbook, no neutral scoring |
| https://github.com/anthropics/launch-your-agent | ~0.5k | Ship-to-managed-agent onboarding | No pre-launch trust gate |

## Differentiation (one paragraph — why a new repo wins)

A neutral, single-binary trust gate that closes the loop: **lint → sandbox trial-run → permission manifest → 0-100 score + badge → CI gate that blocks risky installs**. Scanners tell you something is wrong; this tells you whether to install, fixes the obvious parts (minimal-permission rewrite suggestions), and gives teams a badge to require in PRs. Positioned as the missing step inside Anthropic's launch path and Cloudflare's audit story, not a competitor to either.

## MVP scope (shippable in 1-2 weeks)

- [ ] Static lint rules for SKILL.md + bundled scripts (secret exfil, curl-pipe-sh, overbroad permissions, prompt-injection patterns) — seed from SkillSpector's rule categories
- [ ] Permission-manifest generator (`skill-permissions.json`: network/fs/tools used)
- [ ] 0-100 scorer + SVG badge (`skill-score: 87/100`)
- [ ] GitHub Action: fail PR when score < threshold or manifest missing
- [ ] 30-second demo (asciinema / gif / video)
- [ ] English README (problem → 1-line install → demo → benchmark)

## Launch channels

- [ ] X / HN / r/LocalLLaMA / trendshift
- [ ] PR to https://github.com/punkpeye/awesome-mcp-servers-adjacent skills lists + ClawHub skill registries
- [ ] Demo on `mattpocock/skills` + `obra/superpowers` as test corpus (with permission, findings as issues)

## Validation metrics (first week)

- stars / forks / issues ratio; decision rule for doubling down: 500+ stars + 5+ inbound "run this on my skills repo" issues → build hosted scoreboard; else keep as CLI.

## Spin-off link (filled when the new repo launches)

_(empty — new repo goes here, this file only links out)_

## 證據與備註（中文可）

- 治理三件套同週出現（NVIDIA 掃描 + Cloudflare 審計 + Anthropic 上線引導）是平台在分層，Vercel Eve 做框架、Anthropic 做託管、Cloudflare 做安全——中立評分層沒人做。
- SkillSpector 的規則是最好的冷啟動語料，不要重做掃描器，做掃描器之後的那一層。
- 風險：誤報會殺死信任，MVP 規則要寧少勿多，先求精準再求覆蓋。
