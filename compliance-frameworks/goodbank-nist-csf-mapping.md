# GoodBank — NIST Cybersecurity Framework Mapping

**Document Type:** Compliance Framework Mapping  
**Version:** 1.0  
**Status:** Draft  
**Created:** May 2026  
**Author:** Firas Yasin  
**Classification:** Internal Use Only  
**Review Date:** May 2027

---

## 1. Purpose

This document maps GoodBank's current security controls and practices to the
NIST Cybersecurity Framework (CSF). It identifies areas of strength and gaps
requiring improvement across all GoodBank operating regions.

---

## 2. Scope

This mapping covers GoodBank's information systems, processes, and controls
across all operating regions including the UAE, UK, Malaysia, and EU operations.

---

## 3. About the NIST Cybersecurity Framework

The NIST CSF provides a common language for managing cybersecurity risk. It
organises security activities into five core functions:

- **Identify:** understanding assets, risks, and governance
- **Protect:** implementing safeguards to protect critical services
- **Detect:** identifying cybersecurity events in a timely manner
- **Respond:** taking action regarding detected cybersecurity incidents
- **Recover:** maintaining resilience and restoring services after incidents

---

## 4. Control Mapping

### Function 1: Identify (ID)

| Subcategory | Description | GoodBank Control | Status |
|-------------|-------------|-----------------|--------|
| ID.AM-1 | Physical devices and systems inventoried | Asset management register maintained by IT | Implemented |
| ID.AM-2 | Software platforms and applications inventoried | Software inventory tracked via CMDB | Implemented |
| ID.AM-3 | Data flows mapped and documented | Data flow diagrams maintained by IT Security | Partial |
| ID.GV-1 | Information security policy established | GoodBank Information Security Policy in place | Implemented |
| ID.GV-2 | Roles and responsibilities coordinated | RACI matrix defined for security roles | Implemented |
| ID.RA-1 | Asset vulnerabilities identified and documented | Quarterly vulnerability assessments conducted | Implemented |
| ID.RA-3 | Threats identified and documented | Annual threat assessment completed | Partial |
| ID.RM-1 | Risk management processes established | Risk assessment framework in place | Implemented |

### Function 2: Protect (PR)

| Subcategory | Description | GoodBank Control | Status |
|-------------|-------------|-----------------|--------|
| PR.AC-1 | Identities and credentials managed | Active Directory and MFA enforced | Implemented |
| PR.AC-3 | Remote access managed | VPN with MFA required for all remote access | Implemented |
| PR.AC-4 | Access permissions managed using least privilege | Role-based access control implemented | Implemented |
| PR.AT-1 | All users informed and trained | Annual security awareness training | Implemented |
| PR.AT-2 | Privileged users understand roles and responsibilities | Privileged access training completed | Implemented |
| PR.DS-1 | Data at rest protected | AES-256 encryption for all stored customer data | Implemented |
| PR.DS-2 | Data in transit protected | TLS 1.2 minimum enforced across all channels | Implemented |
| PR.IP-1 | Baseline configurations established | Hardened configuration baselines maintained | Partial |
| PR.IP-4 | Backups conducted and maintained | Daily encrypted backups with offsite storage | Implemented |
| PR.PT-3 | Principle of least functionality applied | Unnecessary services disabled on all systems | Partial |

### Function 3: Detect (DE)

| Subcategory | Description | GoodBank Control | Status |
|-------------|-------------|-----------------|--------|
| DE.AE-1 | Baseline of network operations established | Network baseline documented and monitored | Implemented |
| DE.AE-2 | Detected events analysed | SOC analysts triage and analyse all alerts | Implemented |
| DE.CM-1 | Network monitored to detect potential events | 24/7 SIEM monitoring in place | Implemented |
| DE.CM-3 | Personnel activity monitored | User behaviour analytics deployed | Partial |
| DE.CM-7 | Monitoring for unauthorised personnel and devices | Endpoint detection and response deployed | Implemented |
| DE.DP-4 | Event detection information communicated | Alerts escalated per defined escalation paths | Implemented |

### Function 4: Respond (RS)

| Subcategory | Description | GoodBank Control | Status |
|-------------|-------------|-----------------|--------|
| RS.RP-1 | Response plan executed during or after incident | Incident Response Plan documented and tested | Implemented |
| RS.CO-2 | Incidents reported per established criteria | Regulatory reporting procedures defined | Implemented |
| RS.CO-3 | Information shared consistently with response plans | Internal communication procedures in place | Implemented |
| RS.AN-1 | Notifications from detection systems investigated | L1 and L2 analysts investigate all alerts | Implemented |
| RS.MI-1 | Incidents contained | Containment procedures defined in IRP | Implemented |
| RS.MI-2 | Incidents mitigated | Eradication procedures defined in IRP | Implemented |
| RS.IM-1 | Response plans incorporate lessons learned | Post-incident reviews conducted | Partial |

### Function 5: Recover (RC)

| Subcategory | Description | GoodBank Control | Status |
|-------------|-------------|-----------------|--------|
| RC.RP-1 | Recovery plan executed during or after incident | Recovery procedures defined in IRP | Implemented |
| RC.IM-1 | Recovery plans incorporate lessons learned | Annual IRP review process in place | Partial |
| RC.CO-1 | Public relations managed | Communications team handles external messaging | Implemented |
| RC.CO-2 | Reputation repaired after incident | Crisis communications plan in place | Partial |
| RC.CO-3 | Recovery activities communicated to stakeholders | Stakeholder notification procedures defined | Implemented |

---

## 5. Gap Analysis Summary

| Function | Implemented | Partial | Not Implemented |
|----------|-------------|---------|-----------------|
| Identify | 6 | 2 | 0 |
| Protect | 7 | 3 | 0 |
| Detect | 5 | 1 | 0 |
| Respond | 6 | 1 | 0 |
| Recover | 3 | 2 | 0 |
| **Total** | **27** | **9** | **0** |

---

## 6. Recommendations

Priority areas requiring improvement based on partial implementation status:

1. **ID.AM-3:** Complete data flow mapping across all systems and regions
2. **ID.RA-3:** Conduct more frequent threat assessments, at least quarterly
3. **PR.IP-1:** Finalise and enforce hardened configuration baselines across all endpoints
4. **PR.PT-3:** Complete audit of unnecessary services across all systems
5. **DE.CM-3:** Expand user behaviour analytics coverage to all privileged accounts
6. **RS.IM-1:** Formalise post-incident review process with documented lessons learned
7. **RC.IM-1:** Update recovery plans after each significant incident or exercise
8. **RC.CO-2:** Develop and test a formal reputation recovery plan

---

## 7. Review and Maintenance

This mapping will be reviewed annually or following significant changes to
GoodBank's infrastructure, operations, or the NIST CSF framework itself.

---

*Created as part of a GRC learning portfolio. GoodBank is a fictional organisation
used for educational purposes.*
