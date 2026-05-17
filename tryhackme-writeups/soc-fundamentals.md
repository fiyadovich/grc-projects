# TryHackMe: SOC Fundamentals

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** SOC / Defensive Security  
**Status:** Completed ✅

---

## Room Overview

This room introduced the Security Operations Center, covering its purpose, 
structure, processes, and the technology used to detect and respond to threats. 
It also included a practical exercise simulating a real SOC alert as a Level 1 Analyst.

---

## Key Concepts Learned

### What is a SOC?
A Security Operations Center is a dedicated facility operated by a specialised 
security team that continuously monitors an organisation's network and resources 
to identify suspicious activity and prevent damage. SOC teams operate 24 hours 
a day, seven days a week.

The two core functions of a SOC are Detection and Response.

### Detection Capabilities
- **Detect vulnerabilities:** identifying weaknesses in systems before attackers exploit them
- **Detect unauthorised activity:** spotting abnormal behaviour like logins from unusual locations
- **Detect policy violations:** catching actions that break security rules such as sending confidential files externally
- **Detect intrusions:** identifying unauthorised access attempts to systems and networks

### Response Capabilities
- Supporting incident response by minimising impact and performing root cause analysis
- Escalating critical detections to higher level analysts and incident response teams

### The Three Pillars of a SOC

**People**
The human element is irreplaceable. Security solutions generate large volumes of 
alerts and it takes trained analysts to separate genuine threats from false positives.

SOC roles and responsibilities:
- **SOC Analyst Level 1:** first responders, perform basic alert triage and report detections
- **SOC Analyst Level 2:** deeper investigation, correlating data from multiple sources
- **SOC Analyst Level 3:** proactively hunt for threats, handle critical incidents
- **Security Engineer:** deploys and configures security solutions
- **Detection Engineer:** builds the security rules that power detection logic
- **SOC Manager:** manages team processes and communicates with the CISO

**Process**
Alert Triage is the foundation of SOC operations. Every alert is analysed using 
the 5 Ws framework:

| W | Question |
|---|---------|
| What | What activity triggered the alert? |
| When | When did it occur? |
| Where | Where was it detected? |
| Who | Who was involved? |
| Why | Was the activity intended or malicious? |

After triage, alerts are escalated as tickets. Critical detections trigger a full 
incident response process including forensic analysis to determine root cause.

**Technology**
Key security solutions used in SOC environments:
- **SIEM (Security Information and Event Management):** collects logs from across the network, applies detection rules, and generates alerts. Provides detection capability only, not response.
- **EDR (Endpoint Detection and Response):** provides real time visibility into endpoint activity and supports automated responses
- **Firewall:** monitors and filters incoming and outgoing network traffic
- Other tools include Antivirus, IDS/IPS, XDR, and SOAR

### Practical Exercise
Completed a real world SOC scenario as a Level 1 Analyst investigating a port 
scan alert using a SIEM dashboard:

| 5 W | Answer |
|-----|--------|
| What | Port scan activity |
| When | June 12, 2024 at 17:24 |
| Where | Destination host 10.0.0.3 |
| Who | Source host Nessus |
| Why | Intended, confirmed by vulnerability assessment team |

---

## Personal Takeaways

The 5 Ws framework for alert triage was something that stuck with me. It is a 
simple but structured way to approach any alert without jumping to conclusions. 
The distinction between SIEM only providing detection and not response was also 
something I had not fully appreciated before this room. A lot of people assume 
SIEM does everything but in practice you need EDR and other tools alon
