# GoodBank — Incident Response Plan

**Document Type:** Incident Response Plan  
**Version:** 1.0  
**Status:** Draft  
**Created:** May 2026  
**Author:** Firas Yasin  
**Classification:** Internal Use Only  
**Review Date:** May 2027

---

## 1. Purpose

This Incident Response Plan (IRP) establishes a structured approach for
GoodBank to detect, contain, eradicate, and recover from cybersecurity
incidents. It ensures that incidents are handled consistently, damage is
minimised, and regulatory obligations are met across all operating regions.

---

## 2. Scope

This plan applies to all GoodBank systems, staff, contractors, and third-party
vendors across all operating regions including:

- United Arab Emirates
- United Kingdom
- Malaysia
- European Union operations (Germany, Netherlands, Belgium, Austria, Switzerland)

---

## 3. Regulatory Framework

| Regulation | Region | Incident Reporting Requirement |
|------------|--------|-------------------------------|
| NESA Information Assurance Standards | UAE | Notify NESA of critical incidents |
| FCA Operational Resilience | UK | Report material incidents to FCA |
| UK GDPR | UK | Notify ICO within 72 hours of data breach |
| GDPR | EU | Notify supervisory authority within 72 hours |
| FADP | Switzerland | Notify FDPIC of high-risk data breaches |
| BNM RMiT | Malaysia | Report significant incidents to BNM |
| PDPA | Malaysia | Notify affected individuals of data breaches |
| PCI-DSS | Global | Report cardholder data breaches immediately |

---

## 4. Incident Classification

### 4.1 Severity Levels

| Level | Name | Description | Response Time |
|-------|------|-------------|---------------|
| P1 | Critical | Major breach, ransomware, or system-wide outage | Immediate, within 15 minutes |
| P2 | High | Confirmed malware, data exfiltration attempt, or significant unauthorised access | Within 1 hour |
| P3 | Medium | Suspicious activity, policy violation, or minor unauthorised access | Within 4 hours |
| P4 | Low | False positive, minor policy violation, or informational alert | Within 24 hours |

### 4.2 Incident Types
- Data breach or exfiltration
- Ransomware or destructive malware
- Unauthorised access to systems or data
- Phishing or social engineering attack
- Denial of Service attack
- Insider threat activity
- Third-party vendor compromise
- Regulatory compliance violation

---

## 5. Incident Response Team

| Role | Responsibility |
|------|---------------|
| CISO | Overall incident authority and regulatory reporting |
| SOC Manager | Incident coordination and escalation decisions |
| SOC Analyst L1 | Initial detection, triage, and alert reporting |
| SOC Analyst L2 | Deep investigation, containment, and eradication |
| IT Infrastructure Team | System isolation, recovery, and patching |
| Legal and Compliance | Regulatory notifications and legal obligations |
| HR | Insider threat investigations |
| Communications | Internal and external communications |
| Third-Party Forensics | Engaged for P1 and P2 incidents requiring DFIR |

---

## 6. Incident Response Phases

### Phase 1: Preparation
Ensuring GoodBank is ready to respond to incidents before they occur.

- Maintain and test the incident response plan annually
- Deploy and configure SIEM, EDR, and logging across all systems
- Conduct regular phishing awareness training for all staff
- Establish relationships with third-party forensics providers
- Define and document escalation paths and contact lists
- Run tabletop exercises and simulated incident drills quarterly

### Phase 2: Detection and Analysis
Identifying and assessing potential security incidents.

- Monitor SIEM dashboards and alerts continuously
- Perform initial triage using the Five Ws framework:
  - Who was involved?
  - What activity occurred?
  - When did it start and end?
  - Where was it detected?
  - Why is it suspicious?
- Classify the incident severity using the P1 to P4 scale
- Document all findings in the incident ticket
- Escalate to L2 if the incident meets escalation criteria

### Phase 3: Containment
Limiting the impact and spread of the incident.

**Short-term containment:**
- Isolate affected hosts from the network
- Block malicious IP addresses and domains at the firewall
- Disable compromised user accounts
- Preserve evidence before making changes

**Long-term containment:**
- Apply temporary patches or workarounds
- Implement enhanced monitoring on affected systems
- Notify relevant internal teams and management

### Phase 4: Eradication
Removing the root cause of the incident.

- Identify and remove all malware and malicious artifacts
- Patch exploited vulnerabilities
- Reset compromised credentials
- Review and harden affected system configurations
- Verify eradication through forensic analysis

### Phase 5: Recovery
Restoring systems and operations to normal.

- Restore affected systems from clean backups
- Verify system integrity before returning to production
- Monitor restored systems closely for signs of reinfection
- Gradually restore access and services
- Confirm business operations have returned to normal

### Phase 6: Post-Incident Activity
Learning from the incident to improve future response.

- Conduct a post-incident review within 5 business days
- Document a full timeline of the incident
- Identify root cause and contributing factors
- Record lessons learned and recommended improvements
- Update the incident response plan if needed
- Submit regulatory reports where required

---

## 7. Communication Procedures

### Internal Communication
- Incident Commander notifies senior management immediately for P1 and P2
- All incident communications use encrypted channels
- Regular status updates provided every hour for active P1 incidents

### External Communication
- Legal team manages all communications with regulators
- Communications team manages customer and media notifications
- No external statements are made without CISO and Legal approval

### Regulatory Notification Timelines
| Regulation | Notification Deadline |
|------------|----------------------|
| UK GDPR and EU GDPR | 72 hours from discovery |
| PDPA Malaysia | As soon as practicable |
| PCI-DSS | Immediately upon confirmation |
| FCA | As soon as reasonably practicable |
| NESA UAE | As per NESA incident reporting guidelines |

---

## 8. Evidence Handling

- All evidence must be collected and preserved in a forensically sound manner
- Chain of custody must be maintained for all evidence
- Evidence must not be modified or deleted during an active investigation
- Digital evidence includes logs, memory dumps, disk images, and network captures
- Physical evidence includes hardware and printed documents

---

## 9. Incident Response Playbooks

The following playbooks provide step-by-step guidance for specific incident types:

| Incident Type | Playbook |
|---------------|---------|
| Ransomware Attack | Isolate, preserve, notify, recover from backup |
| Data Breach | Contain, assess scope, notify regulators, notify affected individuals |
| Phishing Attack | Block sender, reset credentials, scan for compromise |
| Insider Threat | Preserve evidence, involve HR and Legal, disable access |
| DDoS Attack | Activate DDoS protection, notify ISP, implement rate limiting |

---

## 10. Plan Maintenance

This plan will be reviewed and updated:
- Annually as part of GoodBank's security governance cycle
- Following any significant security incident
- When regulatory requirements change
- When significant changes occur to GoodBank's infrastructure

---

*Created as part of a GRC learning portfolio. GoodBank is a fictional organisation
used for educational purposes.*
