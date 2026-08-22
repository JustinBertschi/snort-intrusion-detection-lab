SNORT-Based Intrusion Detection Lab (IDS)

A hands-on cybersecurity lab focused on network intrusion detection, security monitoring, vulnerability assessment, and threat analysis using Snort IDS in an isolated virtualized environment.

Project Overview

This project demonstrates the deployment and configuration of a Snort-based Intrusion Detection System within a multi-VM cybersecurity lab.

The lab was designed to simulate network reconnaissance and common attack activity while monitoring traffic, generating alerts, analyzing detections, and evaluating the effectiveness of IDS rules.

Lab Objectives

* Configure a multi-VM cybersecurity environment using VirtualBox
* Deploy and configure Snort IDS
* Create and configure custom Snort detection rules
* Capture and review Snort alerts and logs
* Practice intrusion detection and threat analysis
* Perform vulnerability assessments against lab systems
* Simulate common attack techniques in a controlled environment
* Evaluate the IDS response to different types of malicious or suspicious activity
* Document findings in a structured lab report

Tools & Technologies

* Snort IDS
* VirtualBox
* Nmap
* Lynis
* Linux virtual machines
* Network traffic analysis
* Custom Snort rules
* IDS alert logging

Vulnerability Assessment

Vulnerability and exposure assessments were performed against systems within the isolated lab environment.

Nmap

Nmap was used for:

* Host discovery
* Port scanning
* Service identification
* Network reconnaissance
* Identifying exposed network services

Lynis

Lynis was used to perform security auditing and vulnerability assessment of Linux systems within the lab.

The results helped identify potential weaknesses, configuration issues, and areas where system security could be improved.

Intrusion Detection Testing

Several controlled attack scenarios were simulated to determine how effectively Snort could identify suspicious or malicious behavior.

Testing included:

Port Scanning

Network reconnaissance and port scanning activity was generated to determine whether Snort could identify scanning behavior and produce appropriate alerts.

Brute-Force Activity

Repeated authentication attempts were simulated in the lab to evaluate IDS visibility into potential brute-force activity.

Malware Execution Simulation

Controlled malware-related activity was performed within the isolated environment to evaluate the IDS system’s ability to recognize associated suspicious network behavior.

Snort Configuration

Snort was configured to:

* Monitor network traffic
* Apply detection rules to observed packets
* Generate alerts when rule conditions were met
* Log security events for later investigation
* Support custom rules for lab-specific detection scenarios

Custom Snort rules were used to better understand how network signatures are constructed and how rule configuration affects detection.

Threat Analysis

Generated alerts were reviewed to determine:

* What activity triggered the alert
* Which Snort rule detected the event
* The source and destination involved
* The type of network activity observed
* Whether the detection accurately represented the simulated attack
* How effectively the IDS detected each attack scenario

Lab Reporting

A lab report was created documenting the findings from each attack scenario.

The report evaluated:

* Attack type
* Detection method
* Snort alerts generated
* Relevant log information
* IDS effectiveness
* Observed weaknesses or limitations
* Potential detection improvements

Skills Demonstrated

This project demonstrates practical experience with:

* Intrusion Detection Systems
* Snort configuration
* Snort rule development
* Security monitoring
* Network reconnaissance
* Vulnerability scanning
* Threat analysis
* Alert investigation
* Log analysis
* Virtualized cybersecurity labs
* Network security
* Defensive security testing
* Security documentation

Project Purpose

The purpose of this project was to gain hands-on experience with defensive cybersecurity operations by building an isolated environment where network attacks could be safely simulated, detected, analyzed, and documented.

The project provided practical experience with the workflow used by security analysts when identifying suspicious network activity and investigating IDS alerts.

Disclaimer

All scanning, attack simulation, and security testing associated with this project was performed in an authorized, isolated lab environment for educational and cybersecurity training purposes.