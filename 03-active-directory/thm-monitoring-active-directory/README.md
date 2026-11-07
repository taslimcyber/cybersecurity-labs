# TryHackMe: Monitoring Active Directory

Room about monitoring Active Directory and finding anomalies in high volume logs. AD is the main target of attackers in a company and it generates a huge amount of logs every day, so the key is not to look at everything but to isolate the weak signal in the noise. You need to know what is normal to detect what is abnormal.

Log analysis and triage: I correlated critical Windows events (Event IDs 4624, 4768, 4769, 4732, 5136) to rebuild the chain of an attack.

Threat hunting with Splunk: SIEM queries, filtering the machine accounts ($) and stack counting (long tail analysis) to spot authentication anomalies or suspicious movements.

Audit policy hardening: checking the configuration with auditpol to remove blind spots and get full visibility (DS Access, Kerberos logging).

Incident investigation: a user onboarding scenario, finding compromised accounts (Kerberoasting, abusive privilege escalation) and tracing malicious source IPs.

Room link: https://lnkd.in/e7r7xJA5
