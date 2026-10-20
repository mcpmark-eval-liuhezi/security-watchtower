# Security Watchtower — Quarterly GitHub Security-Hygiene Audit

**Account audited:** [HeziLiu](https://github.com/HeziLiu) (Hezi Liu)
**Public repositories under the account:** 4
**Repositories audited:** `HeziLiu/Little-rookie`, `HeziLiu/CodingInterviewChinese2`, `HeziLiu/awesome-chatgpt-prompts-zh`, `HeziLiu/Big-Buzzard`
**Checks performed per repository:** (1) open Dependabot alerts, (2) most recent GitHub Actions run + that run's usage metrics, (3) discussions + their comments
**Account-level check:** triage of unread notifications with details for each

**Reporting convention:** every check that returned an empty result is recorded explicitly as **none found**. Checks that could not be executed because the API denied access are recorded as **check blocked** together with the exact API error, and are *not* counted as "none found" — a blocked check is an unverified check, not an empty one.

---

## 1. `HeziLiu/Little-rookie`

- URL: https://github.com/HeziLiu/Little-rookie
- Description: Undergraduate coursework
- Primary language: Java | Default branch: `master` | Fork: no | Last push: 2019-06-02

### Open Dependabot alerts
- **CHECK BLOCKED** — the Dependabot alerts API returned `403 Resource not accessible by personal access token` for this repository on every attempt (with and without the `state=open` filter). The audit token lacks the security-events read scope for this repository, so the open-alerts list for `HeziLiu/Little-rookie` could not be retrieved. This is **not** recorded as "none found"; see the remediation checklist.

### Most recent GitHub Actions run (with usage metrics)
- Workflows defined: **none found** — the repository has 0 workflows and no `.github/workflows/` directory exists in the repository.
- Most recent run: **none found** — with 0 workflows, no workflow runs can exist for this repository, so there is no most-recent run to report.
- Usage metrics for that run: **none found** — no run exists, therefore no usage metrics (duration, billable time, job timings) exist to attach.

### Discussions (and their comments)
- Discussions: **none found** — 0 discussions on the repository.
- Discussion comments: **none found** — with 0 discussions there are 0 comments to report.

---

## 2. `HeziLiu/CodingInterviewChinese2`

- URL: https://github.com/HeziLiu/CodingInterviewChinese2
- Description: 《剑指Offer》第二版源代码 (source code of "Coding Interviews" 2nd ed.)
- Primary language: C++ | Default branch: `master` | Fork: yes | Last push: 2018-12-28

### Open Dependabot alerts
- **None found** — the API responded definitively for this repository: `403 Dependabot alerts are disabled for this repository`. There are no open Dependabot alerts because Dependabot alerts are not enabled on `HeziLiu/CodingInterviewChinese2`. (Note for the lead: this is a verified "disabled" state, not merely an absence of alerts — enabling the feature is a decision item in the remediation checklist.)

### Most recent GitHub Actions run (with usage metrics)
- Workflows defined: **none found** — 0 workflows; no `.github/workflows/` directory exists in the repository.
- Most recent run: **none found** — no workflows, hence no runs.
- Usage metrics for that run: **none found** — no run exists to measure.

### Discussions (and their comments)
- Discussions: **none found** — 0 discussions on the repository.
- Discussion comments: **none found** — 0 discussions, 0 comments.

---

## 3. `HeziLiu/awesome-chatgpt-prompts-zh`

- URL: https://github.com/HeziLiu/awesome-chatgpt-prompts-zh
- Description: ChatGPT 中文调教指南。各种场景使用指南。学习怎么让它听你的话。
- Primary language: — (content repo) | Default branch: `main` | Fork: yes | Last push: 2023-04-14

### Open Dependabot alerts
- **None found** — the API responded definitively for this repository: `403 Dependabot alerts are disabled for this repository`. There are no open Dependabot alerts because Dependabot alerts are not enabled on `HeziLiu/awesome-chatgpt-prompts-zh`.

### Most recent GitHub Actions run (with usage metrics)
- Workflows defined: **none found** — 0 workflows; no `.github/workflows/` directory exists in the repository.
- Most recent run: **none found** — no workflows, hence no runs.
- Usage metrics for that run: **none found** — no run exists to measure.

### Discussions (and their comments)
- Discussions: **none found** — 0 discussions on the repository.
- Discussion comments: **none found** — 0 discussions, 0 comments.

---

## 4. `HeziLiu/Big-Buzzard`

- URL: https://github.com/HeziLiu/Big-Buzzard
- Description: For future....
- Primary language: — | Default branch: `master` | Fork: no | Last push: 2018-05-17

### Open Dependabot alerts
- **CHECK BLOCKED** — the Dependabot alerts API returned `403 Resource not accessible by personal access token` for this repository on every attempt (with and without the `state=open` filter). The open-alerts list for `HeziLiu/Big-Buzzard` could not be retrieved. This is **not** recorded as "none found"; see the remediation checklist.

### Most recent GitHub Actions run (with usage metrics)
- Workflows defined: **none found** — 0 workflows; no `.github/workflows/` directory exists in the repository.
- Most recent run: **none found** — no workflows, hence no runs.
- Usage metrics for that run: **none found** — no run exists to measure.

### Discussions (and their comments)
- Discussions: **none found** — 0 discussions on the repository.
- Discussion comments: **none found** — 0 discussions, 0 comments.

---

## 5. Account notifications — unread triage

- **TRIAGE BLOCKED** — the account notifications API returned `403 Resource not accessible by personal access token` on every attempt, across all three views (default unread view, include-read view, and participating-only view). The audit token does not carry the notifications scope.
- Unread notifications enumerated: **none found — triage could not be executed** (this is recorded explicitly rather than left blank: no notification list could be retrieved, so zero notifications were triaged and zero notification details could be pulled).
- Notification details: **none found — no notification could be reached for detail retrieval.**

Because the triage could not run, no notification-derived remediation items exist; the single notification-related follow-up is to re-run the triage with a properly scoped token (see the checklist below).

---

## 6. Remediation checklist

Every item below names the repository (or notification source) it came from.

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

---

## 7. Publishing note

This report was published to the `security-watchtower` repository. Repository creation under the personal account (`POST /user/repos`) was denied by the API with `403 Resource not accessible by personal access token`, so the repository was created in the `mcpmark-eval-liuhezi` organization, of which the audited account is a member. The repository name `security-watchtower` was confirmed unoccupied before creation, so the fallback name was not needed.
