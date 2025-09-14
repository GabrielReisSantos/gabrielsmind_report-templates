# GabrielsMind Security Report

**Project:** Demo Project  
**Client:** Example Ltd.  
**Report ID:** GM-2025-01  
**Version:** 1.0  
**Date:** 14.09.2025  
**Classification:** Confidential

---

## Document History
| Version | Author | Description | Date |
|--------:|:------|:------------|:-----|
| 0.1 | Analyst One | Draft | 10.09.2025 |
| 1.0 | Analyst One | Final | 14.09.2025 |

---

## 1. Executive Summary
**Purpose.**  
Security assessment of Example Ltd.'s Demo Project to identify exploitable vulnerabilities and recommend mitigations.

**Overall Risk.**  
Moderate: several High issues mitigated by limited exposure and partial compensating controls.

**Key Recommendations.**  
- Prioritize patching and configuration hardening for High findings.  
- Implement least privilege and secrets management.  
- Schedule a focused re-test after fixes.

---

## 2. Introduction
A time-boxed, grey-box assessment targeting externally reachable components and exposed internal services.

---

## 3. Engagement Information

### 3.1 Contacts / Team
| Name | Role | Mobile | E-mail |
|:-----|:-----|:------|:-------|
| Gabriel Reis | Lead Pentester | +31 000 000 000 | gabriel@example.com |

### 3.2 Timeline
| Date | Event |
|:-----|:-----|
| 09.09.2025 | Kickoff |
| 10–12.09.2025 | Testing |
| 14.09.2025 | Reporting |

### 3.3 Scope
**In-scope components**
- https://demo.example.com
- 10.0.2.0/24

**Limitations / Exclusions**  
No production DoS; maintenance windows respected.

**Roles / Accounts Tested**  
- `tester@app` (user)  
- `ops@app` (admin)

### 3.4 Methodology
- **Approach:** grey-box with credentialed testing  
- **Standards/References:** OWASP, MITRE ATT&CK, CVSS v3.1  
- **Risk Model:** CVSS v3.1 + qualitative context  
- **Tools:** nmap, Burp Suite, Nessus

---

## 4. Risk Overview
- **Critical:** 0  
- **High:** 1  
- **Medium:** 1  
- **Low:** 1  
- **Info:** 0

| ID | Finding | Severity | CVSS | Status |
|:--:|:--------|:---------|:-----|:------|
| GM-2025-1 | Stored XSS in Blog | High | 7.6 | Open |
| GM-2025-2 | TLS 1.0/1.1 Support | Medium | 5.6 | Open |
| GM-2025-3 | Server version disclosure | Low | qual. | Open |

---

## 5. Detailed Findings

### GM-2025-1: Stored XSS in Blog
**Severity:** High  
**CVSS:** 7.6  
**Vector:** `CVSS:3.1/AV:A/AC:L/PR:L/UI:N/S:C/C:H/I:L/A:N`  
**Affected:** https://demo.example.com/blog

**Prerequisites**  
Authenticated author access to blog post creation.

**Description**  
Unvalidated input in the title field allows stored JavaScript payloads to execute in other users' browsers.

**Evidence**  
```html
<script>alert(1)</script>
```

**Impact**  
Account takeover via cookie theft or CSRF token exfiltration; defacement; user session abuse.

**Recommendation**  
Apply output encoding, strict input validation (allowlist), and CSP. Sanitize rich-text inputs server-side.

**References**  
- https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html  
- https://cwe.mitre.org/data/definitions/79.html

---

## 6. Conclusion
Overall posture is moderate. Address the above issues, then schedule a re-test to verify remediation.

---

## 7. Appendix
- Tooling versions and raw outputs available upon request.