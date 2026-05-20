# TryHackMe: Pyramid of Pain

**Platform:** TryHackMe  
**Difficulty:** Easy  
**Category:** Threat Intelligence  
**Status:** Completed ✅

---

## Room Overview

This room introduced the Pyramid of Pain, a well-known cybersecurity framework
that describes how detecting different types of indicators of compromise affects
an adversary. The higher up the pyramid, the more painful it is for the attacker
to adapt. Used by solutions like Cisco Security, SentinelOne, and SOCRadar.

---

## Key Concepts Learned

### The Pyramid of Pain

The pyramid has six levels, each representing a type of indicator. The higher
the level, the more difficult and costly it is for an adversary to change it.

### Level 1: Hash Values (Trivial)
Hash values uniquely identify files using algorithms like MD5, SHA-1, and SHA-256.
- MD5 produces a 128-bit hash, considered cryptographically insecure
- SHA-1 produces a 160-bit hash, deprecated by NIST in 2011
- SHA-256 produces a 256-bit hash, currently the most widely used standard

Hashes are trivial for attackers to change. Modifying a single bit in a file
produces a completely different hash, making hash-based detection easy to bypass.
Tools like VirusTotal and MetaDefender Cloud are used to look up suspicious hashes.

### Level 2: IP Addresses (Easy)
IP addresses identify devices on a network. Blocking malicious IPs is a common
defensive tactic but not bulletproof since attackers can easily switch to a new IP.

Fast Flux is a technique used by botnets to hide malicious activity by constantly
rotating multiple IP addresses associated with a single domain, making C2
communication harder to detect.

### Level 3: Domain Names (Simple)
Domain names map IP addresses to readable strings. More painful for attackers
than IPs since they need to purchase, register, and configure new domains.

Key concepts:
- **Punycode attacks:** using Unicode characters to create domains that visually
imitate legitimate ones
- **URL shorteners:** used to hide malicious destinations behind shortened links
- Proxy logs and web server logs are used to detect malicious domain activity

### Level 4: Host Artifacts (Annoying)
Host artifacts are traces attackers leave on systems including registry values,
suspicious process executions, files dropped by malware, and other IOCs.
Detecting these forces attackers to change their tools and methods, costing time.

### Level 5: Network Artifacts (Annoying)
Network artifacts include user-agent strings, C2 communication patterns, and
URI patterns in HTTP requests. Tools like Wireshark and TShark help detect
unusual user-agent strings used by malware such as Emotet.

### Level 6: Tools (Challenging)
Attackers use tools to create malicious documents, backdoors, payloads, and
password crackers. Detecting tools through antivirus signatures, YARA rules,
and fuzzy hashing forces attackers to build or find entirely new tools.

Fuzzy hashing (SSDeep) allows similarity analysis between files with minor
differences, helping identify malware variants that would evade standard hash matching.

### Level 7: TTPs (Tough)
TTPs (Tactics, Techniques, and Procedures) represent the complete MITRE ATT&CK
matrix covering every step an adversary takes from initial access to data
exfiltration. Detecting and responding to TTPs leaves attackers with two options:

1. Go back, retrain, and reconfigure their entire approach
2. Give up and find another target

Detecting TTPs is the most effective form of defense as it disrupts the entire
attack chain rather than just individual indicators.

---

## Personal Takeaways

The pyramid completely changed how I think about threat detection. Before this
room I thought blocking IP addresses and checking file hashes was strong defense.
Now I understand those are the easiest things for an attacker to change. The
real value is in detecting TTPs because that forces the attacker to fundamentally
change how they operate, which is extremely costly and time consuming. The Fast
Flux concept was also something I had not come across before and explains why
simple IP blocking is often ineffective against sophisticated threat actors.

---

*Part of my TryHackMe learning journey. [View my profile](https://tryhackme.com/p/FirasYasin)*
