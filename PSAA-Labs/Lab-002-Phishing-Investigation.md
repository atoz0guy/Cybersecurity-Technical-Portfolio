# Lab 002: Phishing & Business Email Compromise (BEC) Investigation
**Date:** 2026-05-11
**Investigator:** @atoz0guy
**Tools:** custom-python-scoring, MXToolbox, PhishTank

---

## 1. Analysis of the Threat
* **Subject:** Urgent Invoice - Action Required
* **Sender:** `ceo.office@company-urgent-updates.com` (Spoofed Domain)
* **Payload:** Malicious URL disguised as a PDF link.

## 2. Risk Scoring (Automated)
Using my [grc_audit_logger_w-risk-scoring.py](https://github.com/atoz0guy/Python-Automation-Lab/blob/main/grc_audit_logger_w-risk-scoring.py):
* **Likelihood:** 4 (Likely - Targeted BEC is rising).
* **Impact:** 5 (Critical - Potential for financial wire fraud).
* **Total Risk Score:** 20 (**HIGH**)

## 3. GRC Control Deficiencies
* **Control ID:** AC-7 (Unsuccessful Logins) - Attacker attempted to use harvested credentials.
* **Control ID:** SI-8 (Spam Protection) - The email gateway failed to flag the look-alike domain.

## 4. Remediation Action
* **Immediate:** URL blocked at the firewall level.
* **ServiceNow Action:** Ticket #INC-10928 created for password reset of affected users.
