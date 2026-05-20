# TryHackMe: Intro to Cyber Threat Intel

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** Threat Intelligence  
**Status:** Completed ✅

---

## Room Overview

This room introduced Cyber Threat Intelligence (CTI) as a practical front-line
tool for SOC analysts. It covered the intelligence lifecycle, indicator types,
sharing standards, and key frameworks used to contextualise and respond to threats.

---

## Key Concepts Learned

### What is CTI?
CTI provides the context that helps analysts decide which alerts represent genuine
danger. It seeks to answer three essential questions:
- Who or what is on the other end of this alert indicator?
- What was their behaviour in the past?
- How does my organisation respond right now?

### Data vs Information vs Intelligence

| Layer | Definition | Example |
|-------|-----------|---------|
| Data | An unprocessed observable | 45.155.205.3:443 |
| Information | Data plus factual annotation | IP registered to Hetzner, first seen 2023 |
| Intelligence | Analysed information that answers so-what | IP belongs to BumbleBee C2, block immediately |

### Key Indicator Types
- **IOC (Indicator of Compromise):** evidence of a breach such as a C2 address in logs
- **IOA (Indicator of Attack):** a malicious action currently underway
- **TTP (Tactics, Techniques, Procedures):** adversary methodologies expressed in MITRE ATT&CK IDs

### Indicator Types and First Resources

| Indicator | Example | First Resources |
|-----------|---------|----------------|
| IP Address | 45.155.205.3 | WHOIS, VirusTotal, Shodan |
| Domain | malicious-updates.net | WHOIS age, passive DNS, urlscan.io |
| URL | hxxp://malicious.net/login | URLhaus, urlscan.io, Any.Run |
| File Hash | e99a18c428cb... | VirusTotal, Hybrid-Analysis, MalShare |
| Email Address | billing@evil.com | MXToolbox, Have I Been Pwned |
| Local Artifact | Registry run key | Sigma rules, EDR prevalence query |

### Threat Intelligence Classifications
- **Strategic:** high-level trends and patterns affecting business decisions
- **Tactical:** adversary TTPs and techniques such as new malspam methods
- **Operational:** campaign-specific details about motives and targets
- **Technical:** atomic indicators and artifacts such as IPs and hashes

### The CTI Lifecycle (Six Phases)
1. **Direction:** define the intelligence requirements and questions to answer
2. **Collection:** gather raw data from internal telemetry, commercial feeds, OSINT, and ISACs
3. **Processing:** normalise, correlate, and deduplicate indicators into usable formats
4. **Analysis:** evaluate relevance, grade confidence, and turn information into judgement
5. **Dissemination:** deliver tailored intelligence to the right stakeholders in the right format
6. **Feedback:** measure outcomes and refine the process for the next cycle

### Traffic Light Protocol (TLP)

| Label | Sharing Boundary |
|-------|-----------------|
| TLP: CLEAR | No restriction, share freely |
| TLP: GREEN | Share with peer community, not publicly |
| TLP: AMBER | Organisation-wide, need-to-know external sharing only |
| TLP: RED | Named recipients only |

### Key Frameworks

**MITRE ATT&CK**
A comprehensive matrix cataloguing adversary tactics and techniques. L1 analysts
match alert behaviour to technique IDs and include them in triage notes for L2.

**MITRE D3FEND**
Maps defensive techniques to ATT&CK entries, helping analysts identify practical
mitigations for detected techniques.

**Cyber Kill Chain (Lockheed Martin)**
Seven phases of an adversary attack:
Reconnaissance, Weaponisation, Delivery, Exploitation, Installation,
Command and Control, Actions on Objectives.

**CVE, CVSS, and NVD**
- CVE: catalogue number for discovered vulnerabilities
- CVSS: 0-10 severity scale for vulnerabilities
- NVD: canonical repository linking CVEs to scores, exploits, and affected products

### Intelligence Sharing Standards
- **STIX:** structured JSON schema for describing threat information in machine-readable form
- **TAXII:** secure APIs for exchanging threat intelligence in near real-time, supporting
Collection and Channel sharing models

---

## Personal Takeaways

The TLP system was something I had heard of but never fully understood before
this room. The idea that a stricter TLP label always prevails when combining
indicators from multiple sources makes complete sense from a legal and trust
perspective. The CTI lifecycle also connected a lot of dots for me, particularly
how the feedback phase closes the loop and drives continuous improvement rather
than treating intelligence as a one-time exercise. The distinction between IOC,
IOA, and TTP is something I will use in every writeup going forward.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
