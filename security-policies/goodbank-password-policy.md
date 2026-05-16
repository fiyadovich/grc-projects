# GoodBank — Password Policy

**Document Type:** Security Policy  
**Version:** 1.0  
**Status:** Draft  
**Created:** May 2026  
**Author:** Firas Yasin  
**Classification:** Internal Use Only

---

## 1. Purpose

This policy establishes password requirements for all GoodBank employees, 
contractors, and third-party users accessing GoodBank systems and data. It 
exists to protect customer financial data, maintain regulatory compliance, 
and reduce the risk of unauthorised access across all GoodBank operations.

---

## 2. Scope

This policy applies to all GoodBank staff, contractors, vendors, and systems 
across all operating regions including:

- United Arab Emirates
- United Kingdom
- Malaysia
- European Union operations (Germany, Netherlands, Belgium, Austria, Switzerland)

---

## 3. Regulatory Framework

GoodBank operates under multiple regulatory jurisdictions. This policy is 
designed to satisfy requirements across all of them.

| Regulation | Region | Relevance |
|------------|--------|-----------|
| NESA Information Assurance Standards | UAE | National cybersecurity requirements |
| FCA Operational Resilience | UK | Financial services security standards |
| UK GDPR | UK | Data protection and access controls |
| GDPR | EU | Data protection for EU customer data |
| FADP | Switzerland | Federal data protection requirements |
| Bank Negara Malaysia (BNM) RMiT | Malaysia | Risk management in technology |
| PDPA | Malaysia | Personal data protection |
| PCI-DSS | Global | Cardholder data security |

---

## 4. Password Requirements

### 4.1 General User Accounts
- Minimum length of 12 characters
- Must include uppercase letters, lowercase letters, numbers, and special characters
- Must not contain the user's name, username, or date of birth
- Must not reuse any of the last 12 passwords
- Must be changed every 90 days

### 4.2 Privileged and Administrator Accounts
- Minimum length of 16 characters
- Must meet all general password requirements
- Must be changed every 60 days
- Must never be shared between users

### 4.3 Service and System Accounts
- Minimum length of 20 characters
- Must be unique per system
- Must be rotated every 180 days or immediately following a security incident
- Must be stored in an approved password vault only

### 4.4 Customer-Facing Accounts
- Minimum length of 10 characters
- Multi-factor authentication (MFA) required for all online banking access
- Account lockout after 5 failed attempts
- Password reset requires identity verification

---

## 5. Prohibited Practices

The following are strictly prohibited across all GoodBank systems:

- Using default or vendor-supplied passwords
- Writing passwords down or storing them in plain text
- Sharing passwords with colleagues, managers, or third parties
- Using the same password across multiple systems
- Sending passwords via email, chat, or any unencrypted channel
- Using personal information such as birthdays or names in passwords

---

## 6. Multi-Factor Authentication (MFA)

MFA is mandatory for:

- All remote access to GoodBank systems
- All privileged and administrator accounts
- All access to customer data systems
- All cloud-based applications and services
- Any access from unmanaged or personal devices

Approved MFA methods include authenticator apps, hardware tokens, and SMS 
verification as a last resort only.

---

## 7. Password Storage and Transmission

- All passwords must be stored using strong hashing algorithms (bcrypt or Argon2)
- Passwords must never be stored in plain text or reversible encryption
- All password transmission must occur over encrypted channels (TLS 1.2 minimum)
- Approved password managers must be used for storing privileged credentials

---

## 8. Account Lockout Policy

| Account Type | Failed Attempts Before Lockout | Lockout Duration |
|--------------|-------------------------------|------------------|
| General User | 5 attempts | 30 minutes |
| Privileged User | 3 attempts | 60 minutes |
| Customer Account | 5 attempts | 30 minutes |
| System Account | 3 attempts | Requires manual review |

---

## 9. Exceptions

Any exceptions to this policy must be:

- Submitted in writing to the Information Security team
- Approved by the Chief Information Security Officer (CISO)
- Documented with a clear business justification
- Reviewed every 90 days

---

## 10. Policy Violations

Violations of this policy may result in:

- Immediate suspension of system access
- Disciplinary action up to and including termination
- Regulatory reporting where required by law
- Legal action where applicable

---

## 11. Review and Maintenance

This policy will be reviewed annually or following any of the following events:

- A security incident involving compromised credentials
- Changes to applicable regulations
- Significant changes to GoodBank systems or infrastructure

---

## 12. References

- NIST Special Publication 800-63B (Digital Identity Guidelines)
- ISO/IEC 27001 (Information Security Management)
- PCI-DSS v4.0
- UK GDPR and FCA Guidelines
- BNM Risk Management in Technology (RMiT)
- GDPR (EU) 2016/679
- FADP (Switzerland)
- PDPA (Malaysia)

---

*Created as part of a GRC learning portfolio. GoodBank is a fictional organisation 
used for educational purposes.*
