# TryHackMe: Defensive Security Intro

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** Defensive Security / Blue Team  
**Status:** Completed ✅

---

## Room Overview

This room introduced the world of defensive security, covering the role of the
blue team, core defensive functions, digital forensics, incident response, and
a hands-on SIEM simulation as a SOC analyst.

---

## Key Concepts Learned

### What is Defensive Security?
Defensive security, known as the blue team, focuses on two main tasks:
- Preventing intrusions from occurring
- Detecting intrusions when they occur and responding properly

Core defensive security activities include:
- **Cyber Security Awareness:** training users on phishing and social engineering
- **Asset Management:** documenting and managing all systems within the organisation
- **Preventative Security:** firewalls and Intrusion Prevention Systems as first line of defence
- **Logging and Monitoring:** comprehensive logging of network and system activity to detect threats
- **Frameworks, Policies and Procedures:** creating robust security policies for appropriate device use

### Security Operations Centre (SOC)
A SOC is a team of cybersecurity professionals that monitors networks and systems
for malicious events. Key areas of focus include:
- **Trends and Vulnerability Awareness:** staying current with industry threats and risks
- **Policy Violations:** monitoring adherence to the organisation's security policies
- **Unauthorised and Illegal Activity:** detecting deviations from baseline behaviour
- **Intrusion and Breach Detection:** identifying and responding to security breaches

### Digital Forensics
Digital forensics applies forensic science to digital devices to preserve and
analyse evidence during incident investigations. Key sources of evidence include:
- **File System:** reveals installed programs, created, overwritten, and deleted files
- **System Memory:** used when an attacker runs malicious code without saving to disk
- **System Logs:** provide detailed records of system activity even after attacker cleanup
- **Network Logs:** help answer questions about ongoing attacks and their scope

### Incident Response
Incident response is how organisations manage security events such as breaches,
data leaks, and cyberattacks. The four phases are:

| Phase | Description |
|-------|-------------|
| Preparation | Creating resources, teams, and frameworks to handle incidents, including phishing awareness training |
| Detection and Analysis | Using tools and processes to detect incidents and assess their scope and severity |
| Containment, Eradication, and Recovery | Limiting impact, eliminating the cause, and restoring affected systems |
| Post-Incident Activity | Reviewing the incident, identifying lessons learned, and improving future response |

### Practical Exercise
Completed a hands-on SIEM simulation as a SOC analyst, navigating security
alerts and events to identify suspicious activity and locate a flag. This
practical exercise demonstrated how real SOC analysts triage and investigate
alerts in a Security Information and Event Management system.

---

## Personal Takeaways

The four phases of incident response are something that stuck with me, especially
the Post-Incident Activity phase which is often overlooked. A lot of teams focus
on containing and recovering from incidents but skip the review process, which
means they keep making the same mistakes. The digital forensics section was also
interesting since memory forensics is something I had not thought about before,
the idea that an attacker can run malicious code entirely in memory without
touching the disk is a technique worth understanding deeply.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
