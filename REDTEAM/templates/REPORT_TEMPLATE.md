# <GabrielsMind Security Report>

**Project:** <Project / System Name>  
**Client:** <Client Name>  
**Report ID:** <GM-YYYY-XX>  
**Version:** <Draft/Final and number>  
**Date:** <DD.MM.YYYY>  
**Classification:** <Confidential | Internal | Public>

---

## Document History
| Version | Author | Description | Date |
|--------:|:------|:------------|:-----|
| <0.1> | <Analyst Name> | <Draft> | <DD.MM.YYYY> |
| <1.0> | <Analyst Name> | <Final> | <DD.MM.YYYY> |

---

## Table of Contents
1. Executive Summary  
2. Introduction  
3. Engagement Information  
   3.1 Contacts / Team  
   3.2 Timeline  
   3.3 Scope  
   3.4 Methodology  
4. Risk Overview  
5. Detailed Findings  
6. Conclusion  
7. Appendix  

---

## 1. Executive Summary
**Purpose.**  
<Brief purpose and context of the assessment.>

**Overall Risk.**  
<One-line risk statement (e.g., "Moderate", reasons why).>

**Key Recommendations.**  
- <Prioritize remediation of Critical/High findings>  
- <Implement least privilege & hardening>  
- <Establish patch & secrets management>  
- <Schedule re-test after fixes>

---

## 2. Introduction
<Background, objectives, assessment type (black/grey/white-box), business context.>

---

## 3. Engagement Information

### 3.1 Contacts / Team
| Name | Role | Mobile | E-mail |
|:-----|:-----|:------|:-------|
| <Name> | <Role> | <+31 ...> | <name@example.com> |

### 3.2 Timeline
| Date | Event |
|:-----|:-----|
| <DD.MM.YYYY> | <Kickoff / Testing / Reporting> |

### 3.3 Scope
**In-scope components**
- <System/Host/URL/Network>
- <…>

**Limitations / Exclusions**  
<Any constraints, blacklisted hosts, test windows, etc.>

**Roles / Accounts Tested**  
- <Account/Role>  
- <…>

### 3.4 Methodology
- **Approach:** <e.g., grey-box with credentialed testing>  
- **Standards/References:** <OWASP, MITRE ATT&CK, NIST, vendor guides>  
- **Risk Model:** <CVSS v3.1 + qualitative context>  
- **Tools:** <nmap, Burp, Nessus, CrackMapExec, etc.>

---

## 4. Risk Overview
- **Critical:** <#>  
- **High:** <#>  
- **Medium:** <#>  
- **Low:** <#>  
- **Info:** <#>

| ID | Finding | Severity | CVSS | Status |
|:--:|:--------|:---------|:-----|:------|
| <GM-2025-1> | <Finding title> | <High> | <7.6 / vector> | <Open> |
| <…> |  |  |  |  |

---

## 5. Detailed Findings
<!-- Duplicate the following block for each finding -->
<!-- Or keep separate files and paste them here before delivery -->

### <GM-2025-1>: <Finding Title>
**Severity:** <Critical/High/Medium/Low/Info>  
**CVSS:** <score>  
**Vector:** `<CVSS:3.1/...>`  
**Affected:** <Asset / URL / IP / Component>

**Prerequisites**  
<Conditions required for exploitation (auth level, network location, etc.).>

**Description**  
<Clear explanation of the vulnerability and where it exists.>

**Evidence**  
```text
<Logs / HTTP requests / Commands / Tool output / Screenshots path>
```

**Impact**  
<What an attacker can achieve; business/technical consequences.>

**Recommendation**  
<Actionable steps; configuration/code changes; process controls; compensating controls.>

**References**  
- <OWASP/cheatsheet link>  
- <CWE/CVE/vendor advisory>  

---

## 6. Conclusion
<Overall posture, key takeaways, and next steps: remediation plan, re-test window, hardening themes.>

---

## 7. Appendix
- Tools used (versions)
- Raw scan outputs (as attachments/links)
- Additional logs/evidence
- Glossary of terms