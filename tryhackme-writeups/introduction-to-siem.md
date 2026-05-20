# TryHackMe: Introduction to SIEM

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** SOC / Defensive Security  
**Status:** Completed ✅

---

## Room Overview

This room introduced Security Information and Event Management (SIEM) systems,
covering how different devices generate logs, the challenges of managing isolated
logs, and how SIEM solves these problems through centralisation, normalisation,
correlation, and real-time alerting.

---

## Key Concepts Learned

### Log Sources
Every device in a network generates logs when activities occur. Log sources
fall into two categories:

**Host-Centric Log Sources**
Capture events occurring within or related to the host:
- User file access and authentication attempts
- Process execution activity
- Registry key modifications
- PowerShell execution

**Network-Centric Log Sources**
Generated when hosts communicate with each other or the internet:
- SSH connections
- FTP file access
- Web traffic
- VPN connections
- Network file sharing activity

### Challenges of Isolated Logs
Working with logs across multiple devices without a centralised solution creates
several problems:
- **Numerous log sources:** hundreds of events per second scattered across devices
- **No centralisation:** requires SSH or RDP into each device to analyse logs individually
- **Limited context:** individual logs cannot tell the whole story without correlation
- **Limited analysis:** manually reviewing all logs is nearly impossible at scale
- **Format issues:** different devices generate logs in different formats

### What is SIEM?
SIEM collects logs from various sources, standardises their format, correlates
them, and detects malicious activities using detection rules. Core features include:

- **Centralised Log Collection:** pulls logs from all sources into one place via agents or APIs
- **Normalisation:** breaks raw logs into consistent fields through parsing
- **Correlation:** identifies relationships between logs from different sources to detect patterns
- **Real-time Alerting:** triggers alerts when detection rule conditions are met
- **Dashboards and Reporting:** presents analysed data as actionable insights

### Common Log Ingestion Methods
1. **Agent/Forwarder:** lightweight tool installed on endpoints that captures and sends logs
2. **Syslog:** widely used protocol for real-time log collection from various systems
3. **Manual Upload:** offline data ingestion for quick analysis
4. **Port-Forwarding:** endpoints forward data to the SIEM on a configured listening port

### Common Linux Log Locations
| Path | Contents |
|------|----------|
| /var/log/httpd | HTTP request, response, and error logs |
| /var/log/cron | Cron job events |
| /var/log/auth.log | Authentication-related logs |
| /var/log/kern | Kernel-related events |

### Detection Rules
SIEM uses logical expressions to trigger alerts. Examples:
- Five failed login attempts in 10 seconds triggers a Multiple Failed Login Attempts alert
- Successful login after multiple failures triggers a Suspicious Login alert
- Event ID 104 (event log cleared) triggers an Event Log Cleared alert
- Event ID 4688 with process name whoami triggers a WHOAMI Command Execution alert

### Alert Investigation Process
When an alert is triggered analysts:
1. Examine the events and flows associated with the alert
2. Check which rule conditions were met
3. Determine if it is a True or False Positive
4. Take appropriate action such as isolating the host, blocking an IP, or tuning the rule

---

## Personal Takeaways

The log correlation example in this room was what made SIEM click for me. A
user logging in via VPN from a new IP, accessing documents, running PowerShell,
and making an outbound connection all look normal individually. Correlated
together they paint a very different picture. That is the whole point of SIEM
and why having normalised logs matters so much, you cannot correlate what you
cannot compare. The Splunk rooms recommended at the end are now on my list
given that Splunk Core Certified User is on my cert roadmap.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
