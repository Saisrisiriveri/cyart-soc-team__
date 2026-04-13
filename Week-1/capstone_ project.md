**Capstone Project:**

**Abstract**

This report presents the theoretical understanding and practical implementation of Security Operations Center (SOC) concepts. The objective of this task is to learn how SOC analysts detect, analyze, and respond to cybersecurity incidents using industry-standard tools and frameworks. The report covers SOC fundamentals, security monitoring, log management, incident response, and hands-on tasks such as log analysis and alert configuration.

**Introduction**

A Security Operations Center (SOC) is a centralized unit responsible for monitoring, detecting, and responding to cybersecurity threats in an organization. SOC teams operate continuously to ensure system security and protect sensitive data from attacks.

SOC analysts use tools such as:

*   Splunk
*   Elastic SIEM
*   Wireshark

They follow frameworks like:

*   National Institute of Standards and Technology (NIST)
*   MITRE ATT&CK

**SOC Fundamentals and Operations**

Purpose of SOC

*   Detect cyber threats proactively
*   Monitor systems continuously
*   Respond to incidents quickly

SOC Manager

|

\-------------------

| | |

Tier 1 Tier 2 Tier 3

(Alert (Invest. (Threat

Monitor) Analyst) Hunting)

**SOC Roles**

*   Tier 1 Analyst: Monitors alerts
*   Tier 2 Analyst: Investigates incidents
*   Tier 3 Analyst: Performs threat hunting
*   SOC Manager: Oversees operations

**Key Functions**

*   Log analysis
*   Alert triage
*   Threat intelligence integration

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnAAAAADCAIAAACcWKWyAAAAAXNSR0IArs4c6QAAAEdJREFUWEft0DERADEIAMEkBYMnxOINJT+vgXavv2Zvdx8RIECAAAECC4GqeovdSoAAAQIECPwCmXlnBgYBAgQIECCwEYiID2E7BWPUJdaOAAAAAElFTkSuQmCC)

**SOC Workflow Diagram**

Logs / Alerts

↓

Detection

↓

Triage

↓

Investigation

↓

Response

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnAAAAADCAIAAACcWKWyAAAAAXNSR0IArs4c6QAAAEdJREFUWEft0DERADEIAMEkBYMmzOINJT+vgXavv2Zvdx8RIECAAAECC4GqeovdSoAAAQIECPwCmXlnBgYBAgQIECCwEYiIDzVPBWCuuZORAAAAAElFTkSuQmCC)

**Security Monitoring Basics**

Security monitoring involves tracking system and network activities to detect:

*   Unauthorized access
*   Malware activity
*   Policy violations

**Tools Used**

*   SIEM tools (Splunk, Elastic)
*   Network analyzers like Wireshark

**Key Metrics**

*   False Positives
*   False Negatives
*   Mean Time to Detect (MTTD)

Systems / Network

↓

Log Collection

↓

SIEM

↓

Alerts Generated

↓

SOC Analyst

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnAAAAADCAIAAACcWKWyAAAAAXNSR0IArs4c6QAAAEdJREFUWEft0DERADEIAMEkBYMmzOINJT+vgXavv2Zvdx8RIECAAAECC4GqeovdSoAAAQIECPwCmXlnBgYBAgQIECCwEYiIDzVPBWCuuZORAAAAAElFTkSuQmCC)

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnAAAAADCAIAAACcWKWyAAAAAXNSR0IArs4c6QAAAEdJREFUWEft0DERADEIAMEkBYMmzOINJT+vgXavv2Zvdx8RIECAAAECC4GqeovdSoAAAQIECPwCmXlnBgYBAgQIECCwEYiIDzVPBWCuuZORAAAAAElFTkSuQmCC)

**Log Management Fundamentals**

Logs are records of system activities.

*   Log Lifecycle
*   Collection
*   Normalization
*   Storage
*   Analysis
*   Log Types
*   Windows Event Logs
*   Syslog
*   HTTP logs

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnEAAAADCAIAAABzms6MAAAAAXNSR0IArs4c6QAAAElJREFUWEft0DEBADEIBMEkBRbwg1G8oeSbd0A71+8Vc7v7GAECBAgQILATqKq3e1ATIECAAAECv8CdGRgECBAgQIDARiAiMvMDAzIFpQwxKy0AAAAASUVORK5CYII=)

**Basic Security Concepts**

**CIA Triad Diagram**

Confidentiality

/ \\

/ \\

/ \\

Integrity -------- Availability

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAnEAAAADCAIAAABzms6MAAAAAXNSR0IArs4c6QAAAElJREFUWEft0DEBADEIBMEkBRYQhFC8oeSbd0A71+8Vc7v7GAECBAgQILATqKq3e1ATIECAAAECv8CdGRgECBAgQIDARiAiMvMDLzAFqKmK7LMAAAAASUVORK5CYII=)

**Incident Response Lifecycle**

Based on National Institute of Standards and Technology:

*   Preparation
*   Identification
*   Containment
*   Eradication
*   Recovery
*   Lessons Learned

**Log Analysis (Windows Event Viewer)**

**Steps:**

Open Event Viewer

Go to Windows Logs → Security

**Filter:**

Event ID = 4625

Identify failed login attempts

**Result:**

Multiple failed logins indicate a brute-force attack.

**Snort Rule Testing**

**Tool:** Snort

**Steps:**

Install Snort

Add rule in local.rules

Run Snort

**Rule Used:** alert tcp any any -> any 80 (msg:"Malicious Domain"; content:"malicious.com"; http\_uri; sid:1000001;)

**Test using:**

curl [http://malicious.com](http://malicious.com)

**Result:**

Snort successfully detected malicious.

**Tool:** Nessus

**Steps:**

*   Install Nessus Essentials
*   Scan Metasploitable VM
*   Export report

**Result:**

Top vulnerabilities identified based on CVSS score.

**Log Collection Pipeline**

**Steps:**

Install Fluentd on Ubuntu

**Generate log:**

logger "Test message"

Forward logs to Elastic SIEM

**Result:**

Logs successfully collected and analyzed.

**Network Monitoring Using Wireshark**

Open: Wireshark

Steps:

*   *   Select eth0 interface
    *   Click Start Capture
    *   Generate traffic by opening websites
    *   Stop capture

Filter example:

http

**Dashboard Creation**

**Tools: Kibana**

**Dashboard Metrics:**

Top attacker IPs

Event frequency

Alert severity

**The knowledge gained includes:**

Log analysis

Threat detection

Incident response

Alert configuration

This training is essential for building a career as a SOC Analyst.

**Conclusion:**

This SOC training task provided practical exposure to real-world cybersecurity operations. The implementation of tools like Snort, Wireshark, and SIEM platforms helped in understanding how security analysts detect threats and respond to incidents.