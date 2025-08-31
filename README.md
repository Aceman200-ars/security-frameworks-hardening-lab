# Security-Frameworks-Hardening-Lab

A hands-on lab implementing and evidencing security controls across **Ubuntu Linux** and **AWS**, mapped to recognized frameworks:
- **DISA STIG: Ubuntu 20**
- **CIS Amazon Web Services Foundations**
- **CIS Ubuntu Linux 22.04 LTS**
- **OWASP Top 10 (A06 – Vulnerable & Outdated Components)**

This repo emphasizes **repeatable checks**, **clear remediation**, and **auditable evidence** (screenshots + command outputs).

## Goals
- Practice applying controls from multiple frameworks
- Document checks, fixes, and follow-up compliance steps
- Produce recruiter-friendly, audit-ready artifacts

## What’s Inside
- `controls/` – one Markdown per control, with **Check / Fix / Additional steps / Evidence**
- `scripts/` – small, idempotent scripts to verify or enforce controls
- `docs/` – environment, framework overview, control mapping, and screenshots
- `reports/` – executive summary + audit log of what ran and when

## Ethics
Lab-only resources. No production secrets, keys, or PII are stored here. See `ETHICS.md`.

## Quickstart
1. Review `docs/environment.md`.
2. Run checks (e.g., `bash scripts/ubuntu/check_temp_account_expiry.sh`).
3. Capture evidence and place in `docs/screenshots/`.
4. Update the corresponding file in `controls/...` with your results.
5. Summarize outcomes in `reports/executive-summary.md`.


