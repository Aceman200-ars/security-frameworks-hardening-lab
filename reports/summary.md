# Security Frameworks – Executive Summary (Lab 6)

**Analyst:** Jack Grainger  
**Course:** IT 369 – DL1  
**Date:** Fall 2025  

---

## Overview
This report summarizes the results of applying multiple security frameworks (STIG, CIS, OWASP) across Ubuntu and AWS environments. The purpose is to demonstrate compliance verification, remediation steps, and evidence collection.

---

## Key Findings
- **Ubuntu Temporary Accounts** – Configured to expire ≤ 72 hours. ✔️
- **AWS Root Access Keys** – Active root key detected and deactivated. ✔️ (recommend deletion)
- **IAM Password Policy** – Updated to enforce password reuse prevention (24 remembered). ✔️
- **Ubuntu Sudo Group** – Only analyst account present, least privilege maintained. ✔️
- **Ubuntu Outdated Packages** – Detected and remediated with upgrade. ✔️
- **UFW Firewall** – Confirmed installed. ✔️
- **Root GID** – Correctly set to 0. ✔️
- **nftables Service** – Initially disabled; remediated and enabled. ✔️
- **AppArmor** – Installed and running. ✔️
- **AWS Root MFA** – Hardware MFA enabled. ✔️

---

## Compliance Impact
- Reduced risk of unauthorized persistence via temporary accounts.
- Closed critical AWS IAM misconfigurations.
- Strengthened password policies to meet CIS standards.
- Enforced least privilege across sudo and root group.
- Improved endpoint hardening (UFW, nftables, AppArmor).

---

## Audit Log
| Date       | Action Taken                                 | Result |
|------------|----------------------------------------------|--------|
| 2025-08-15 | Ran chage checks on temp accounts            | Expiry enforced |
| 2025-08-16 | Downloaded IAM credential report             | Root key active |
| 2025-08-16 | Deactivated root access key                  | Success |
| 2025-08-18 | Enabled password reuse prevention            | Success |
| 2025-08-20 | Verified sudo group membership               | 1 user only |
| 2025-08-22 | Applied Ubuntu updates                       | Success |
| 2025-08-24 | Verified UFW firewall present                | Installed |
| 2025-08-25 | Checked root GID                             | Correct |
| 2025-08-26 | Enabled nftables                             | Running |
| 2025-08-28 | Verified AppArmor enabled                    | Active |
| 2025-08-29 | Confirmed AWS MFA enabled for root           | Active |

---

## Conclusion
All tested controls achieved compliance, with remediation steps taken where gaps were identified.  
The lab demonstrates hands-on application of **security frameworks, compliance auditing, and evidence collection**.
