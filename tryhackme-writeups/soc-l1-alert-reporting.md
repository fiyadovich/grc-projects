# TryHackMe: SOC L1 Alert Reporting

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** SOC / Defensive Security  
**Status:** Completed ✅

---

## Room Overview

This room covered how L1 SOC analysts document, report, and escalate alerts
after triage. It introduced alert reporting, escalation procedures, and
communication best practices, with hands-on practice in a simulated SOC dashboard.

---

## Key Concepts Learned

### The Alert Path
Most alerts are closed as False Positives or handled at L1 level. Complex and
threatening ones are escalated to L2 analysts who remediate most breaches.
Three key terms govern this process:

- **Alert Reporting:** formally documenting investigation details and findings
- **Alert Escalation:** passing suspicious alerts to an L2 analyst for further review
- **Communication:** coordinating with other departments such as IT or HR during analysis

### Why Alert Reports Matter

| Purpose | Explanation |
|---------|-------------|
| Provide context for escalation | Saves L2 analysts time by summarising what happened |
| Save findings for records | Raw SIEM logs are stored 3-12 months but alerts are kept indefinitely |
| Improve investigation skills | Writing reports forces analysts to fully understand what they investigated |

### The Five Ws Report Format
Every alert report should answer these five questions:

- **Who:** which user logged in, ran the command, or downloaded the file
- **What:** the exact action or event sequence that was performed
- **When:** when the suspicious activity started and ended
- **Where:** which device, IP address, or website was involved
- **Why:** the reasoning behind the final verdict, the most important W

### When to Escalate to L2
Escalate an alert if any of the following apply:

1. The alert indicates a major cyberattack requiring deeper investigation or DFIR
2. Remediation actions are required such as malware removal, host isolation, or password reset
3. Communication with customers, partners, management, or law enforcement is required
4. The alert is not fully understood and senior support is needed

### Escalation Process
1. Move the alert to In Progress status and complete the analysis
2. Write a detailed alert report and set the verdict
3. If escalation is required, assign the alert to the L2 analyst on shift
4. L2 receives the alert, reads the report, and contacts L1 if clarification is needed

### Practical Exercise
Completed hands-on alert triage in a simulated SOC dashboard including:
- Investigating a sensitive document leak and identifying the responsible user
- Analysing a suspicious phishing email from a spoofed Microsoft address
- Writing structured alert reports using the Five Ws framework
- Escalating a True Positive alert to the L2 analyst on shift

---

## Personal Takeaways

The Five Ws framework is something I will carry forward into every alert
investigation. It is simple but forces you to be thorough before closing or
escalating anything. The point about raw SIEM logs only being stored for
3-12 months while alerts are kept indefinitely also stood out, it explains
why writing detailed alert comments is so important rather than just clicking
True Positive and moving on.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
