# GRC Audit Report: Internal Access Control Review
**Date:** 2026-05-11
**Auditor:** @atoz0guy
**Framework Alignment:** NIST 800-53 (Access Control)

---

## 1. Executive Summary
This audit was conducted to verify the integrity of user access levels within the internal ticketing system. The goal was to ensure the "Principle of Least Privilege" is being followed.

## 2. Technical Methodology
* **Tool Used:** Custom Python Automation Script (`grc_audit_logger.py`)
* **Platform:** ServiceNow / Local Active Directory Lab
* **Scope:** Review of 50 administrative accounts.

## 3. Findings & Evidence
| Finding ID | Control Impact | Severity | Description |
| :--- | :--- | :--- | :--- |
| AUDIT-001 | AC-2 (Account Management) | **HIGH** | Detected 3 terminated employees with active "Admin" credentials. |
| AUDIT-002 | AC-7 (Unsuccessful Logins) | **MEDIUM** | Brute-force attempts detected on Service Desk portal; lockout policy not triggering. |

## 4. Remediation Plan
1. **Immediate:** Disable flagged accounts in Active Directory.
2. **Long-term:** Automate the offboarding workflow in ServiceNow to sync with HR records.

---
**Status:** ⚠️ Pending Remediation
