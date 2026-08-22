SNORT-Based Intrusion Detection Lab (IDS)

A hands-on cybersecurity lab focused on network intrusion detection, security monitoring, vulnerability assessment, and threat analysis using Snort IDS in an isolated virtualized environment.

Project Overview

This project demonstrates the deployment and configuration of a Snort-based Intrusion Detection System within a multi-VM cybersecurity lab using VirtualBox.

The environment uses Kali Purple as the traffic-generation and security-testing system and Ubuntu Linux as the monitored system running Snort IDS.

The lab is designed to simulate network reconnaissance and common attack activity while monitoring traffic, generating alerts, analyzing detections, and evaluating the effectiveness of custom Snort rules.

Lab Architecture

┌──────────────────────────────┐
│          VirtualBox          │
│                              │
│  Kali Purple                 │
│  Traffic/Test VM             │
│       │                      │
│       │ Virtual Network      │
│       ▼                      │
│  Ubuntu                      │
│  ┌────────────────────────┐  │
│  │        Snort IDS       │  │
│  │                        │  │
│  │ Ping Detection         │  │
│  │ Port Scan Detection    │  │
│  │ SSH Brute-Force Alert  │  │
│  │ SQLi Detection         │  │
│  │ ICMP Flood Detection   │  │
│  │ File Transfer Alert    │  │
│  └────────────────────────┘  │
└──────────────────────────────┘

Traffic Flow

Kali Purple
Traffic / Security Testing
        │
        │ Controlled Lab Traffic
        ▼
Ubuntu Linux
        │
        ▼
Snort IDS
        │
        ├── Packet Inspection
        ├── Custom Rule Matching
        ├── Alert Generation
        └── Security Event Logging

All testing is performed inside an authorized and isolated VirtualBox environment.

Lab Objectives

* Configure a multi-VM cybersecurity environment using VirtualBox
* Deploy and configure Snort IDS on Ubuntu
* Use Kali Purple as a controlled security-testing system
* Create and configure custom Snort detection rules
* Capture and review Snort alerts and logs
* Practice intrusion detection and threat analysis
* Perform vulnerability assessments against lab systems
* Simulate common attack techniques in a controlled environment
* Evaluate IDS responses to suspicious or malicious activity
* Document findings in a structured lab report

Tools & Technologies

* Snort IDS
* Kali Purple
* Ubuntu Linux
* VirtualBox
* Nmap
* Lynis
* Linux networking
* Network traffic analysis
* Custom Snort rules
* IDS alert logging

Snort Detection Rules

Custom Snort rules are used to identify different types of network activity generated from the Kali Purple testing VM.

ICMP Ping Detection

Detects ICMP Echo Request traffic sent toward the monitored Ubuntu system.

This provides a basic introduction to identifying network discovery and reconnaissance activity.

Port Scan Detection

Monitors network traffic for patterns associated with port scanning and reconnaissance.

Port scanning tests are used to determine whether Snort can identify suspicious attempts to discover exposed services.

SSH Brute-Force Alert

Monitors repeated connection attempts directed toward the SSH service.

The rule identifies network behavior that may be consistent with brute-force activity.

Snort detects the network connection pattern, while authentication logs can be reviewed separately to determine whether login attempts actually failed.

SQL Injection Detection

Custom HTTP rules are used to identify basic request patterns associated with SQL injection attempts.

This demonstrates application-layer traffic inspection and signature-based detection.

ICMP Flood Detection

Monitors the frequency of ICMP Echo Requests and generates an alert when traffic exceeds a configured threshold.

This helps demonstrate rate-based detection of potential denial-of-service activity.

File Transfer Alert

Monitors network traffic for selected file-transfer indicators.

This provides experience using Snort to identify potentially suspicious file activity moving across the network.

Vulnerability Assessment

Vulnerability and exposure assessments are performed against systems within the isolated lab environment.

Nmap

Nmap is used for:

* Host discovery
* Port scanning
* Service identification
* Network reconnaissance
* Identifying exposed network services

The resulting traffic can also be analyzed by Snort to evaluate how effectively reconnaissance activity is detected.

Lynis

Lynis is used to perform security auditing and vulnerability assessment of Linux systems within the lab.

The results help identify:

* Potential security weaknesses
* Configuration issues
* System-hardening opportunities
* Areas where security controls could be improved

Intrusion Detection Testing

Controlled security scenarios are generated from Kali Purple to determine how effectively Snort identifies suspicious activity.

Testing includes:

Ping / ICMP Reconnaissance

ICMP traffic is generated from Kali Purple toward the Ubuntu system.

Snort monitors the traffic and generates alerts when configured ICMP rules are matched.

Port Scanning

Network reconnaissance and port-scanning activity is generated to determine whether Snort can recognize scanning patterns and produce appropriate alerts.

Brute-Force Activity

Repeated authentication-related connection attempts are simulated to evaluate IDS visibility into behavior potentially associated with brute-force attacks.

SQL Injection Activity

Basic SQL injection patterns are sent toward test web services to evaluate application-layer Snort detection rules.

ICMP Flood Activity

Higher-frequency ICMP traffic is generated in the controlled lab to evaluate threshold-based alerting.

File Transfer Monitoring

Controlled file transfers are monitored to determine whether configured Snort signatures recognize selected file-transfer indicators.

Malware-Related Traffic Simulation

Controlled malware-related network activity can be simulated within the isolated environment to evaluate Snort’s ability to recognize associated suspicious traffic.

Snort Configuration

Snort is configured to:

* Monitor network traffic
* Inspect packets entering the Ubuntu system
* Apply detection rules to observed traffic
* Generate alerts when rule conditions are met
* Log security events for investigation
* Support custom rules for lab-specific detection scenarios
* Detect both individual signatures and repeated traffic patterns

Custom Snort rules are used to develop a better understanding of how IDS signatures are constructed and how rule configuration affects detection.

Detection Workflow

Kali Purple
     │
     │ Generates Controlled Traffic
     ▼
VirtualBox Network
     │
     ▼
Ubuntu + Snort IDS
     │
     ├── Capture Traffic
     │
     ├── Inspect Packets
     │
     ├── Compare Against Rules
     │
     ▼
Detection Match
     │
     ▼
Snort Alert
     │
     ├── Source IP
     ├── Destination IP
     ├── Protocol
     ├── Detection Rule
     └── Timestamp
     │
     ▼
Security Analysis

Threat Analysis

Generated alerts are reviewed to determine:

* What activity triggered the alert
* Which Snort rule detected the event
* The source and destination systems involved
* The protocol associated with the traffic
* The type of network activity observed
* Whether the alert accurately represented the simulated activity
* How effectively the IDS detected each test scenario
* Whether the rule produced false positives
* How the detection rule could be improved

Lab Reporting

A lab report documents findings from each attack or detection scenario.

The report evaluates:

* Attack or traffic type
* Detection method
* Snort rule used
* Snort alerts generated
* Relevant log information
* Source and destination systems
* IDS effectiveness
* Observed weaknesses or limitations
* False positives
* Potential detection improvements

Skills Demonstrated

This project demonstrates practical experience with:

* Intrusion Detection Systems
* Snort IDS configuration
* Snort rule development
* Signature-based detection
* Threshold-based detection
* Security monitoring
* Network reconnaissance
* Vulnerability scanning
* Threat analysis
* Alert investigation
* Log analysis
* Linux networking
* Virtualized cybersecurity labs
* Network security
* Defensive security testing
* Security documentation

Project Purpose

The purpose of this project is to gain hands-on experience with defensive cybersecurity operations by building an isolated environment where network attacks and suspicious traffic can be safely simulated, detected, analyzed, and documented.

The project provides practical experience with a security-analysis workflow:

Generate Traffic
      ↓
Detect Activity
      ↓
Generate Alert
      ↓
Analyze Event
      ↓
Determine Cause
      ↓
Evaluate Detection
      ↓
Improve Rule
      ↓
Document Findings

This workflow reflects fundamental responsibilities involved in network security monitoring and intrusion detection.

Disclaimer

All scanning, attack simulation, network testing, and security testing associated with this project is performed only within an authorized, isolated lab environment for educational and cybersecurity training purposes.