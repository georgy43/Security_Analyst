1. Executive Summary

This report presents the findings of a security assessment conducted on a local test network using Nmap and Wireshark. The objective was to identify open ports, running services, insecure protocols, and potential vulnerabilities within the network environment.

The assessment revealed multiple exposed services and instances of unencrypted communication, which could pose security risks if left unmitigated. Recommendations have been provided to strengthen network defenses and reduce the attack surface.

2. Scope of Assessment

Target Network: Local test network (e.g., 192.168.1.0/24)

Assessment Type: Internal security assessment

Tools Used:

Nmap (Port scanning & service detection)

Wireshark (Packet capture & traffic analysis)

Testing Environment: Controlled lab / Virtual Machine

This assessment was conducted strictly for educational purposes.

3. Methodology
Phase 1: Network Discovery and Port Scanning (Nmap)

The following activities were performed:

Host discovery to identify active devices.

Port scanning to detect open TCP ports.

Service version detection.

Aggressive scan for OS and additional information.

Purpose:

Identify exposed services.

Detect unnecessary open ports.

Assess possible vulnerabilities.

Phase 2: Network Traffic Analysis (Wireshark)

The following steps were performed:

Selected active network interface.

Captured live traffic.

Applied filters (HTTP, TCP, DNS).

Inspected packet contents and protocol details.

Purpose:

Identify plaintext data transmission.

Detect suspicious or abnormal traffic.

Analyze communication patterns.

4. Findings
4.1 Open Ports and Services (Nmap Results)

Example findings:

Port	Service	Observation	Risk Level
22	SSH	Remote access enabled	Medium
80	HTTP	Unencrypted web service	Medium
445	SMB	File sharing service exposed	High
3306	MySQL	Database port accessible	High
Analysis:

SMB (445) exposure increases risk of ransomware and lateral movement.

HTTP (80) allows unencrypted data transmission.

Database ports (3306) should not be publicly accessible.

Open ports increase the system’s attack surface.

4.2 Traffic Analysis Findings (Wireshark Results)

Observations during packet capture:

HTTP traffic transmitted in plaintext.

DNS queries visible without encryption.

TCP handshake processes observed.

No encrypted protection for certain services.

Security Concerns:

Credentials transmitted over HTTP can be intercepted.

Unsecured traffic may allow packet sniffing attacks.

Sensitive information can be exposed in shared networks.

5. Risk Assessment
Vulnerability	Impact	Likelihood	Risk Rating
Open SMB Port	Data compromise	High	High
Unencrypted HTTP	Credential theft	Medium	Medium
Exposed Database	Unauthorized access	High	High
Weak Firewall Rules	Increased attack surface	Medium	Medium–High


7. Conclusion

The assessment successfully identified several potential security risks within the test network. The combination of Nmap scanning and Wireshark traffic analysis provided valuable insight into:

Exposed services

Network communication patterns

Security misconfigurations

Regular security assessments are essential to reduce vulnerabilities, prevent unauthorized access, and maintain a secure network infrastructure.


Wireshark 

Operating System: Ubuntu/Linux
