# Remediation Checklist — Quarterly Security-Hygiene Audit

Every item names the repository (or notification source) it came from. Source report: `reports/audit.md`.

- [ ] Re-run the open-Dependabot-alerts check for **`HeziLiu/Little-rookie`** using a token with the security-events read scope — the check was blocked by a `403 Resource not accessible by personal access token` error, so the result is unverified rather than "none found".
- [ ] Re-run the open-Dependabot-alerts check for **`HeziLiu/Big-Buzzard`** using a token with the security-events read scope — blocked by the same `403` error; result unverified rather than "none found".
- [ ] Decide whether to enable Dependabot alerts on **`HeziLiu/CodingInterviewChinese2`** — the check confirmed the feature is disabled, which is why the open-alerts result is "none found"; enabling it would give real coverage for this fork.
- [ ] Decide whether to enable Dependabot alerts on **`HeziLiu/awesome-chatgpt-prompts-zh`** — feature confirmed disabled; "none found" reflects the disabled state, not a scanned-clean state.
- [ ] Document the CI posture of **`HeziLiu/Little-rookie`** — no GitHub Actions workflows exist (none found), so there is no recent run or usage to review; confirm this is intentional for legacy coursework, or add a workflow.
- [ ] Document the CI posture of **`HeziLiu/CodingInterviewChinese2`** — no workflows (none found); consider archiving this unmaintained 2018 fork instead.
- [ ] Document the CI posture of **`HeziLiu/awesome-chatgpt-prompts-zh`** — no workflows (none found); confirm intentional.
- [ ] Document the CI posture of **`HeziLiu/Big-Buzzard`** — no workflows (none found); consider archiving this inactive 2018 repository or defining its intended purpose.
- [ ] Confirm the discussions posture of **`HeziLiu/Little-rookie`**, **`HeziLiu/CodingInterviewChinese2`**, **`HeziLiu/awesome-chatgpt-prompts-zh`**, and **`HeziLiu/Big-Buzzard`** — all four have 0 discussions and 0 comments (none found); no action required unless community engagement is planned.
- [ ] Re-run the **unread-notifications triage for the HeziLiu account** with a token that carries the notifications scope — every attempt (default, include-read, participating-only) returned `403 Resource not accessible by personal access token`, so no notification could be enumerated or detailed this cycle.
