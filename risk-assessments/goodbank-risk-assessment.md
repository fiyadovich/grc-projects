# GoodBank — Information Security Risk Assessment

**Document Type:** Risk Assessment  
**Version:** 1.0  
**Status:** Draft  
**Created:** May 2026  
**Author:** Firas Yasin  
**Classification:** Internal Use Only  
**Review Date:** May 2027

---

## 1. Purpose

This risk assessment identifies, evaluates, and prioritises information security 
risks to GoodBank's operations, systems, and customer data across all operating 
regions. It supports GoodBank's commitment to maintaining a robust security 
posture in line with applicable regulatory frameworks.

---

## 2. Scope

This assessment covers GoodBank's information assets, systems, and processes 
across all operating regions including:

- United Arab Emirates
- United Kingdom
- Malaysia
- European Union operations (Germany, Netherlands, Belgium, Austria, Switzerland)

---

## 3. Regulatory Framework

| Regulation | Region | Relevance |
|------------|--------|-----------|
| NESA Information Assurance Standards | UAE | National cybersecurity requirements |
| FCA Operational Resilience | UK | Financial services security standards |
| UK GDPR | UK | Data protection and access controls |
| GDPR | EU | Data protection for EU customer data |
| FADP | Switzerland | Federal data protection requirements |
| BNM RMiT | Malaysia | Risk management in technology |
| PDPA | Malaysia | Personal data protection |
| PCI-DSS | Global | Cardholder data security |
| ISO 27001 | Global | Information security management |
| NIST CSF | Global | Cybersecurity framework reference |

---

## 4. Risk Methodology

### 4.1 Risk Rating Formula
Risk is calculated using the following formula:

**Risk Score = Likelihood x Impact**

### 4.2 Likelihood Scale
| Score | Level | Description |
|-------|-------|-------------|
| 1 | Rare | Unlikely to occur, no known history |
| 2 | Unlikely | Could occur but not expected |
| 3 | Possible | May occur at some point |
| 4 | Likely | Will probably occur |
| 5 | Almost Certain | Expected to occur regularly |

### 4.3 Impact Scale
| Score | Level | Description |
|-------|-------|-------------|
| 1 | Negligible | Minimal impact on operations or customers |
| 2 | Minor | Limited impact, manageable without escalation |
| 3 | Moderate | Noticeable impact, requires management attention |
| 4 | Major | Significant impact on operations or reputation |
| 5 | Critical | Severe impact, potential regulatory action or major financial loss |

### 4.4 Risk Rating Matrix
| Score | Rating |
|-------|--------|
| 1 to 4 | Low |
| 5 to 9 | Medium |
| 10 to 14 | High |
| 15 to 25 | Critical |

---

## 5. Risk Register

### Risk 1: Phishing Attack Leading to Credential Compromise

| Field | Detail |
|-------|--------|
| Asset | Employee email accounts and credentials |
| Threat | Social engineering via phishing emails |
| Vulnerability | Insufficient email filtering and staff awareness |
| Likelihood | 4 (Likely) |
| Impact | 4 (Major) |
| Risk Score | 16 (Critical) |
| Affected Regions | All regions |
| Regulatory Impact | GDPR, UK GDPR, NESA, PCI-DSS |

**Recommended Controls:**
- Deploy advanced email filtering and anti-phishing solutions
- Implement mandatory phishing awareness training for all staff
- Enforce MFA across all employee accounts
- Conduct regular simulated phishing exercises

---

### Risk 2: Ransomware Attack on Core Banking Systems

| Field | Detail |
|-------|--------|
| Asset | Core banking infrastructure and customer data |
| Threat | Ransomware deployment via malicious email or compromised credentials |
| Vulnerability | Unpatched systems, insufficient endpoint protection |
| Likelihood | 3 (Possible) |
| Impact | 5 (Critical) |
| Risk Score | 15 (Critical) |
| Affected Regions | All regions |
| Regulatory Impact | FCA, NESA, BNM RMiT, PCI-DSS |

**Recommended Controls:**
- Maintain regular offline backups of all critical systems
- Deploy EDR solutions across all endpoints
- Implement network segmentation to limit lateral movement
- Establish and regularly test an incident response plan

---

### Risk 3: Insider Threat and Unauthorised Data Access

| Field | Detail |
|-------|--------|
| Asset | Customer financial data and personally identifiable information |
| Threat | Malicious or negligent employee accessing data beyond their role |
| Vulnerability | Excessive access privileges and insufficient monitoring |
| Likelihood | 3 (Possible) |
| Impact | 4 (Major) |
| Risk Score | 12 (High) |
| Affected Regions | All regions |
| Regulatory Impact | GDPR, UK GDPR, PDPA, FADP, PCI-DSS |

**Recommended Controls:**
- Enforce least privilege access across all systems
- Implement role-based access control (RBAC)
- Deploy user behaviour analytics (UBA) to detect anomalous activity
- Conduct regular access reviews and revoke unnecessary privileges

---

### Risk 4: Third-Party Vendor Security Breach

| Field | Detail |
|-------|--------|
| Asset | Customer data shared with third-party service providers |
| Threat | Security breach at a vendor with access to GoodBank systems or data |
| Vulnerability | Insufficient vendor security assessment and monitoring |
| Likelihood | 3 (Possible) |
| Impact | 4 (Major) |
| Risk Score | 12 (High) |
| Affected Regions | All regions |
| Regulatory Impact | GDPR, UK GDPR, FCA, NESA, BNM RMiT |

**Recommended Controls:**
- Implement a formal third-party risk management programme
- Conduct security assessments before onboarding vendors
- Include security requirements in all vendor contracts
- Monitor vendor access and conduct periodic reviews

---

### Risk 5: DDoS Attack on Online Banking Platform

| Field | Detail |
|-------|--------|
| Asset | GoodBank online banking platform and mobile application |
| Threat | Distributed Denial of Service attack disrupting customer access |
| Vulnerability | Insufficient DDoS protection and capacity planning |
| Likelihood | 3 (Possible) |
| Impact | 3 (Moderate) |
| Risk Score | 9 (Medium) |
| Affected Regions | All regions |
| Regulatory Impact | FCA Operational Resilience, BNM RMiT |

**Recommended Controls:**
- Deploy DDoS protection services
- Implement rate limiting and traffic filtering
- Develop and test a business continuity plan for platform outages
- Establish clear customer communication procedures during outages

---

### Risk 6: Unencrypted Customer Data in Transit

| Field | Detail |
|-------|--------|
| Asset | Customer financial and personal data transmitted between systems |
| Threat | Man-in-the-middle attack intercepting unencrypted data |
| Vulnerability | Use of outdated or weak encryption protocols |
| Likelihood | 2 (Unlikely) |
| Impact | 4 (Major) |
| Risk Score | 8 (Medium) |
| Affected Regions | All regions |
| Regulatory Impact | GDPR, UK GDPR, PDPA, PCI-DSS |

**Recommended Controls:**
- Enforce TLS 1.2 or higher across all data transmission channels
- Conduct regular encryption audits
- Disable legacy protocols such as TLS 1.0 and SSL
- Implement certificate management procedures

---

## 6. Risk Summary

| Risk | Score | Rating |
|------|-------|--------|
| Phishing Attack Leading to Credential Compromise | 16 | Critical |
| Ransomware Attack on Core Banking Systems | 15 | Critical |
| Insider Threat and Unauthorised Data Access | 12 | High |
| Third-Party Vendor Security Breach | 12 | High |
| DDoS Attack on Online Banking Platform | 9 | Medium |
| Unencrypted Customer Data in Transit | 8 | Medium |

---

## 7. Recommendations

Critical risks should be addressed immediately as a priority. High risks should 
be assigned to risk owners with a remediation plan within 30 days. Medium risks 
should be scheduled for remediation within 90 days and monitored regularly.

---

## 8. Review and Maintenance

This risk assessment will be reviewed annually or following any significant 
change to GoodBank's systems, operations, or regulatory environment.

---

*Created as part of a GRC learning portfolio. GoodBank is a fictional organisation 
used for educational purposes.*
