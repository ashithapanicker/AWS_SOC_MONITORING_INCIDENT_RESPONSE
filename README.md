# AWS SOC Monitoring & Incident Response Lab

## Project Overview

A hands-on Security Operations Center (SOC) lab built using AWS EC2, Splunk Universal Forwarder, and Splunk Enterprise.

The project demonstrates security log collection, event investigation, event correlation, detection engineering, alert configuration, alert validation, benign activity testing, and SSH brute-force incident response.

This is a controlled learning environment using simulated security events.

## Architecture

- **AWS EC2 – Ubuntu:** Generates simulated security events and system logs.
- **Splunk Universal Forwarder:** Collects and forwards logs from the EC2 instance.
- **SSH Reverse Tunnel:** Transfers forwarded logs securely to the local system.
- **Local Windows Laptop – Splunk Enterprise:** Receives, indexes, searches, and analyses the logs.
- **SOC Analyst:** Performs alert triage, investigation, and response.

See `05_Architecture_Diagrams/AWS_SOC_Lab_Architecture_Reverse_SSH_Tunnel.png`.

## Tools & Technologies

- AWS EC2
- Ubuntu Linux
- Splunk Enterprise
- Splunk Universal Forwarder
- Splunk Search Processing Language (SPL)
- SSH Reverse Tunnelling
- UFW Firewall
- Windows

## Project Phases

1. Initial Security Event Investigation
2. Security Event Correlation
3. Detection Engineering – 20 Detection Rules
4. Alert Triage
5. Alert Configuration
6. Detection and Alert Validation
7. Benign Activity and False-Positive Testing
8. SSH Brute-Force Incident Investigation and Response

## Key Results

- Generated and investigated 50 simulated security events in the documented test run.
- Grouped events into 19 activity categories.
- configured 20 detection rules.
- Configured and enabled Splunk alerts.
- Reviewed triggered alerts and performed validation testing.
- Conducted benign activity and false-positive testing.
- Investigated simulated SSH brute-force activity.
- Configured and verified a UFW firewall rule to deny SSH traffic from the simulated source IP.

## Incident Response Highlight

The SSH brute-force scenario involved eight simulated failed login attempts against the `admin` account from `198.51.100.23`.

The investigation found no successful authentication from that source in the reviewed run. A UFW rule was configured to deny SSH traffic from the source IP.

The firewall configuration was verified. An independent connection test from that source was not performed.

## Repository Structure

- `01_Project_Report/` – Final project report
- `02_Phase_Documentation/` – Detailed phase-wise documentation
- `03_Splunk_Screenshots/` – Splunk investigation and detection evidence
- `04_Incident_Response_Evidence/` – SSH investigation and firewall evidence
- `05_Architecture_Diagrams/` – Lab architecture diagram
- `06_GitHub/` – GitHub project materials

## Learning Outcomes

- Security log analysis
- Event correlation
- SPL query development
- Detection engineering
- Alert configuration and triage
- False-positive assessment
- Linux firewall configuration
- Incident investigation and response

## Disclaimer

This project was developed for educational purposes in a controlled lab environment. Security events were simulated and do not represent confirmed real-world attacks. The firewall configuration was demonstrated in the lab and was not independently tested against a connection from the simulated source IP.
