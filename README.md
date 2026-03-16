# Financial Application Security Assessment

## Executive Summary
This project presents a security assessment of FinSecure network architecture in order to identify potential risk that could afect the confidentiality, integrity, and availability of sensitive financial systems. 
The assessment analyzes the system architecture, operational practices, and data handling procedures to determine where vulnerabilities may exist within the environment

Several security risks were identified during the assessment. Some of the most significant risks include unsecured administrative access through Remote Desktop Protocol (RDP), a flat network architecture that could allow attackers
to move laterally between systems, weak encryption practices during data transmission, and the lack of centralized monitoring capabilities. These weakness could allow attackers to gain unauthorized access to internal systems, 
intercept sensitive data being transmitted on the network, and remain undetected on the network for extended periods of time.

To reduce these risks, several security improvements are recommended. These include implementing stronger authentication controls for administrative access, introducing network segmentation to limit lateral movement, enforcing
strong encryption standards for data at rest and in transit, deploying centralized logging and monitoring through a SIEM system, and improving identity and access management policies.

Implementing these recommendations would significantly improve the organizations ability to protect its internal network and its sensitive data and detect malicious activity much quicker to reduce the overall security risk within
its environment.

---

## Project Overview

This project analyzes the security posture of a fictional financial services organization and evaluates risks within its network architecture, data protection practices, and operational security controls.

The purpose of this project is to simulate a real-world security assessment by reviewing the organization's infrastructure and identifying potential security risks along with recommended mitigation strategies.

---

# Scenario Background

FinSecure Corp is a regional financial services organization that manages customer financial transactions, employee records, and internal accounting documentation. The company operates both on-premises systems and remote office resources.

As part of a planned infrastructure expansion, FinSecure is reviewing its data protection and security operations to ensure alignment with organizational policies and regulatory requirements.

---

# Current Operations

Several internal processes are used to exchange and manage sensitive data across the organization.

- The Human Resources and Finance departments exchange payroll data using an internal FTP server that operates with legacy file transfer protocols.
- Customer financial data is transmitted from internal applications to third-party partners through HTTPS connections supporting multiple TLS versions, including TLS 1.0.
- Email messages with attached financial reports are sometimes used to share sensitive information between employees.
- Remote employees connect to internal systems through a VPN service that supports multiple TLS versions and is configured for split-tunnel access.
- System administrators manage virtual machines on the internal network using Remote Desktop Protocol (RDP).

---

# Data Storage Practices

The organization stores financial and operational data across several internal systems.

- Daily backups of customer transaction data are written to a shared offsite storage repository accessible by multiple departments.
- Files stored in the offsite environment are maintained in their original format without server-side encryption.
- The on-premises finance server stores customer PII and financial records in a relational database that maintains data in clear text on disk.
- Application encryption keys are stored in configuration files located on the same servers that host the associated applications.
- Endpoint laptops synchronize working files to local directories using standard file synchronization tools.
- Archived HR records are maintained in a document management system that applies password protection to compressed archive files.

---

# Key Management and Policy Overview

- Encryption keys are generated within individual applications and maintained by the respective system owners.
- Some systems use self-signed certificates that are manually renewed during routine maintenance windows.
- The organization's encryption policy is periodically reviewed according to internal governance schedules.

---

# System Architecture Overview

FinSecure operates a distributed infrastructure consisting of a corporate network and a centralized data center.

The data center hosts core application systems including:

- Application servers
- File servers
- Finance virtual machines
- Web interface systems
- Customer records database
- Accounting systems

Employees access internal resources through the corporate network, which contains departmental subnets for Human Resources and IT operations.

Remote employees connect through a VPN gateway, and network traffic passes through a perimeter firewall and internal switch before reaching departmental systems.

---

# Architecture Diagram

The following diagram illustrates the simplified network architecture evaluated in this security assessment.

![Architecture Diagram](Architecture-Diagram.drawio.png)

---

# Operational Environment Summary

## Monitoring and Detection

- System, application, and network logs are stored locally on the devices where they are generated and retained for 30 days.
- Firewall and VPN activity reports are reviewed weekly by IT staff.
- Endpoint antivirus software generates local alerts but does not forward those alerts to a centralized monitoring system.
- Security events are documented and handled by IT administrators as part of normal operational responsibilities.

---

## Incident Response and Access Control

- IT staff coordinate incident response through the internal help desk ticketing system.
- Remote administrators authenticate using usernames and passwords.

---

## System Maintenance and Patching

- Operating system and application updates are deployed quarterly after testing in staging environments.
- Updates are installed manually by IT administrators.
- Maintenance activity is recorded in a change-tracking spreadsheet.

---

## Backup and Recovery

- Nightly database backups are stored in an offsite repository managed by the IT department.
- Backup files are retained for 90 days.
- A full restoration test is conducted annually to verify backup integrity.
- IT staff review backup reports after each nightly backup job.

---

## Change and Configuration Management

- System configuration changes are documented by IT staff in a shared spreadsheet.
- Configuration details for virtual machines and offsite resources are updated when modifications occur.
- Certificates used by some systems are renewed manually during maintenance windows.

---

# Assessment Scope

The objective of this project is to evaluate the security risks present within FinSecure's infrastructure and recommend improvements to strengthen the organization's security posture.

The assessment focuses on four key areas:

- Risk Assessment
- Threat Modeling
- Security Control Recommendations
- Monitoring Strategy


This project demonstrates practical cybersecurity skills including:

• Security architecture analysis  
• Risk assessment  
• Threat modeling  
• Defensive security planning  
• Security documentation

These activities are commonly performed by security analysts, blue team professionals, and security engineers when evaluating enterprise systems.

# Author

Mitchell G  
Cybersecurity Student | Blue Team Focus
