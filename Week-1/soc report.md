Security Operations Center (SOC) Internship Report

# Abstract

This report presents the theoretical and practical implementation of Security Operations Center (SOC) activities.

The study focuses on SOC fundamentals, log monitoring, security tools, incident response workflow, and alert management.

Practical tasks include Snort rule testing, log analysis, vulnerability scanning, and monitoring dashboards.

The objective of this report is to understand how SOC analysts detect, investigate, and respond to cybersecurity threats using industry tools and frameworks.

# 1\. Introduction

A Security Operations Center (SOC) is responsible for monitoring and defending an organization's IT infrastructure.

SOC teams analyze logs, investigate alerts, and respond to incidents.

They work continuously to detect threats and reduce the impact of cyber attacks.

# 2\. Objectives

• Understand SOC fundamentals and operations

• Learn log management and monitoring techniques

• Implement security tools for threat detection

• Perform incident response analysis

• Document security events

# 3\. SOC Fundamentals and Operations

A SOC monitors networks and systems to detect cyber threats.

Main responsibilities include:

• Continuous monitoring

• Threat detection

• Incident response

• Security reporting

# 4\. SOC Team Roles

Tier 1 Analyst – Monitor alerts and escalate incidents

Tier 2 Analyst – Investigate security events

Tier 3 Analyst – Threat hunting and malware analysis

SOC Manager – Manage SOC operations

# 5\. Security Monitoring

Security monitoring helps detect anomalies and suspicious activities.

Tools used include SIEM platforms, IDS systems, and network analyzers.

Key monitoring metrics:

• Mean Time to Detect (MTTD)

• Mean Time to Respond (MTTR)

• False positives

# 6\. Log Management

Logs are records of system activities.

Log lifecycle includes:

1\. Collection

2\. Normalization

3\. Storage

4\. Analysis

5\. Retention

# 7\. Practical Task – Log Analysis

Windows Event Viewer can detect suspicious activity.

Important Event IDs:

4625 – Failed login

7045 – New service creation

These logs help detect brute force attacks.

# 8\. Security Tools Used

SIEM – Splunk / Elastic

IDS – Snort

EDR – CrowdStrike

Vulnerability Scanner – Nessus

Network Analyzer – Wireshark

# 9\. Snort Intrusion Detection Lab

Snort was installed and configured to detect network traffic.

Custom rule created:

alert tcp any any -> any 80 (msg:"HTTP Test Alert"; sid:1000001; rev:1;)

Traffic generated using curl to test detection.

# 10\. Vulnerability Scanning

Nessus was used to scan a vulnerable machine.

Top vulnerabilities identified:

• Outdated Apache Server

• Weak SSH configuration

• Default credentials

# 11\. Incident Response Process

Incident Response lifecycle includes:

1\. Preparation

2\. Identification

3\. Containment

4\. Eradication

5\. Recovery

6\. Lessons Learned

# 12\. Monitoring Dashboards

Security dashboards help visualize attack trends.

Tools like Kibana and Grafana can display:

• Top source IPs

• Alert frequency

• Failed login attempts

# 13\. Documentation of Security Events

Example Event Documentation:

Date | Source IP | Event ID | Description | Action

\--------------------------------------------------

10-03-2026 | 192.168.1.10 | 4625 | Failed login attempts | Account locked

# 14\. Conclusion

SOC operations play a critical role in protecting organizations from cyber threats.

Using tools like SIEM, IDS, and vulnerability scanners helps detect and respond to attacks efficiently.

This project provided practical experience in security monitoring and incident handling.