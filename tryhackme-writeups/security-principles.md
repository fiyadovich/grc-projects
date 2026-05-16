# TryHackMe: Security Principles

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** Security Fundamentals  
**Status:** Completed ✅

---

## Room Overview

This room covered the foundational principles of cybersecurity including the CIA 
triad, security models, design principles, and the difference between 
vulnerability, threat, and risk.

---

## Key Concepts Learned

### The CIA Triad
The three core functions of any security system:
- **Confidentiality:** only authorised users can access the data
- **Integrity:** data cannot be altered without detection
- **Availability:** systems and services must be accessible when needed

### Beyond CIA: The DAD Triad
The opposite of CIA, representing attack outcomes:
- **Disclosure:** attacker gains access to confidential data
- **Alteration:** attacker modifies data
- **Destruction/Denial:** attacker makes systems unavailable

### Authenticity and Nonrepudiation
Two additional security concepts beyond the CIA triad:
- **Authenticity:** confirming data or documents are genuine and from the claimed source
- **Nonrepudiation:** ensuring a party cannot deny having sent or created something

### The Parkerian Hexad
An expanded security model with six elements: Availability, Utility, Integrity, 
Authenticity, Confidentiality, and Possession. Utility and Possession extend 
beyond CIA to cover situations where data exists but cannot be used.

### Security Models

**Bell-LaPadula Model** focuses on confidentiality:
- No read up: a lower clearance subject cannot read higher clearance data
- No write down: a higher clearance subject cannot write to lower clearance levels
- Summarised as "write up, read down"

**Biba Model** focuses on integrity:
- No read down: a higher integrity subject should not read lower integrity data
- No write up: a lower integrity subject should not write to higher integrity levels
- Summarised as "read up, write down"

**Clark-Wilson Model** also focuses on integrity using:
- Constrained Data Items (CDI): data whose integrity must be preserved
- Unconstrained Data Items (UDI): all other data
- Transformation Procedures (TPs): programmed operations maintaining CDI integrity
- Integrity Verification Procedures (IVPs): procedures that verify CDI validity

### ISO/IEC 19249 Architectural Principles
1. Domain Separation: group related components with shared security attributes
2. Layering: structure systems in layers to apply security policies at each level
3. Encapsulation: hide low level implementation and expose only necessary methods
4. Redundancy: ensure availability and integrity through backup systems
5. Virtualisation: share hardware across multiple systems for security boundaries

### ISO/IEC 19249 Design Principles
1. Least Privilege: grant only the minimum permissions needed to perform a task
2. Attack Surface Minimisation: reduce known and unknown vulnerabilities
3. Centralised Parameter Validation: validate all inputs through a central library
4. Centralised General Security Services: centralise authentication and security functions
5. Preparing for Error and Exception Handling: design systems to fail safely

### Zero Trust vs Trust but Verify
- **Trust but Verify:** always verify behaviour even when an entity is trusted, 
using logging and automated monitoring
- **Zero Trust:** treat trust itself as a vulnerability, every entity is considered 
adversarial until proven otherwise, requiring authentication and authorisation 
before accessing any resource

### Vulnerability, Threat, and Risk
Three terms that are often confused but have distinct meanings:
- **Vulnerability:** a weakness in a system
- **Threat:** a potential danger associated with that weakness
- **Risk:** the likelihood of a threat exploiting a vulnerability and its impact on the business

### Shared Responsibility Model
In cloud environments, security responsibilities are split between the provider 
and the customer depending on the service type. IaaS gives customers more control 
and responsibility while SaaS places more responsibility on the provider.

---

## Personal Takeaways

The Bell-LaPadula and Biba models were confusing at first because they seem 
counterintuitive. The way it clicked for me was thinking about government 
clearance levels where you can share upward but not downward. Zero Trust also 
stood out as something very relevant to modern security given how many breaches 
happen through insider threats or compromised internal accounts.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
