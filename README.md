# 🔐 Secure Network Design – Merged Enterprise Architecture

**Author:** Taylor Wilkerson  
**Course:** Secure Network Design  
**Institution:** Western Governors University  

---

# 📌 Project Overview

This project presents a **secure network architecture design for the merger of two organizations** with existing infrastructure vulnerabilities and security weaknesses.

The goal of the project was to analyze security risks in both companies' networks and design a **secure, scalable, and cost-effective merged network topology**.

The proposed solution integrates:

- Secure network segmentation
- Cloud-based identity services
- Centralized security controls
- Hybrid infrastructure (on-prem + cloud)

---

# 🎯 Project Objectives

This project focuses on the following goals:

- Identify **existing security vulnerabilities**
- Analyze **network infrastructure weaknesses**
- Design a **secure merged network topology**
- Apply **secure network architecture principles**
- Address **regulatory compliance requirements**
- Recommend a **cost-efficient infrastructure strategy**

---

# ⚠️ Identified Network Security Issues

## Company A

### Network Security Vulnerabilities

- Excessive open ports (21–90 and 3389)
- Weak password policy (8 characters, no expiration)

These conditions increase the risk of **unauthorized remote access and brute-force attacks**.

### Infrastructure Vulnerabilities

- End-of-life network hardware
- Vulnerable Meraki MR28 wireless access points
- Excessive user administrative privileges

These weaknesses increase the **attack surface and potential system compromise**.

---

## Company B

### Network Security Vulnerabilities

- Distributed Ruby remote code execution vulnerability
- No multi-factor authentication (MFA) enforcement

This creates high risk of **credential compromise and unauthorized system access**.

### Infrastructure Vulnerabilities

- Apache Tomcat Ghostcat vulnerability
- End-of-life systems and outdated operating systems
- Lack of infrastructure redundancy

These conditions increase the likelihood of **data breaches and service disruptions**.

---

# 🌐 Proposed Merged Network Architecture

The merged network combines both companies into a **secure hybrid infrastructure environment**.

## Core Components

| Component | Function |
|----------|-----------|
| Firewall | Centralized network security and traffic filtering |
| Core Switches | Internal network segmentation |
| Routers | Internal network routing |
| Domain Controller | Centralized identity and access management |
| Virtualization Layer | Server consolidation and resource optimization |
| Application Servers | Internal business applications |
| File Servers | Enterprise data storage |
| VPN Gateway | Secure remote and cloud connectivity |
| Azure AD | Cloud identity management |
| Cloud Storage | Secure off-site data storage |
| SaaS Applications | Cloud-based business tools |

---

# 🧱 OSI Model Mapping

| Network Component | OSI Layer |
|------------------|-----------|
| Switches | Layer 2 – Data Link |
| Routers | Layer 3 – Network |
| Firewall | Layers 3–4 (and Layer 7 for NGFW) |
| Servers | Layer 7 – Application |
| Cloud Services | Layer 7 – Application |
| Workstations | Full OSI stack |

---

# 🛡 Secure Network Design Principles

## Defense in Depth

Multiple security layers protect the environment:

- Perimeter firewall protection
- Network segmentation
- Secure identity management
- VPN encrypted connections
- Cloud access controls

---

## Principle of Least Privilege

Users receive **only the permissions required to perform their job functions**, reducing the risk of:

- insider threats
- privilege abuse
- malware installation

---

# 📜 Regulatory Compliance Considerations

## HIPAA Security Rule

Relevant because the organization may store **protected health information (PHI)**.

Network design supports HIPAA through:

- centralized identity control
- encrypted VPN connections
- secure network segmentation
- controlled access to sensitive systems

---

## GLBA Safeguards Rule

Relevant for organizations handling **financial customer information**.

Compliance support includes:

- unified firewall protection
- centralized authentication
- improved monitoring and access controls
- stronger protection of financial data

---

# ⚡ Emerging Cybersecurity Threats

## Identity-Based Attacks

Attackers increasingly target **user credentials** through phishing or credential theft.

Mitigation strategies:

- Multi-factor authentication
- Conditional access policies
- Identity monitoring

---

## Ransomware

Merged environments can increase the **blast radius of ransomware attacks**.

Mitigation strategies:

- Network segmentation
- Regular backups
- endpoint protection
- rapid patching of vulnerabilities

---

# ☁️ Infrastructure Strategy

The proposed solution uses a **hybrid infrastructure model**.

### On-Premise Benefits

- Low latency for internal systems
- Control over sensitive infrastructure
- Compatibility with legacy systems

### Cloud Benefits

- Scalability
- Reduced hardware costs
- built-in security controls
- simplified identity management

---

# 💰 Cost-Benefit Strategy

Instead of replacing all infrastructure immediately, the design focuses on:

- replacing **end-of-life hardware**
- consolidating servers through **virtualization**
- leveraging **cloud identity and storage**
- maintaining essential on-prem infrastructure

This approach balances **security improvements with budget constraints**.

---

# 🧰 Technologies Referenced

- Microsoft Azure Active Directory
- Virtualization Platforms
- Cisco Networking Equipment
- VPN Technologies
- Enterprise Firewalls

---

# 📚 References

NIST. (2024). CVE-2022-33279 Vulnerability Detail  
https://nvd.nist.gov/vuln/detail/CVE-2022-33279

Pozhogin, A. (2023). Why No User Should Have Local Admin Rights  
https://www.cyberark.com/resources/blog/why-no-user-should-have-local-admin-rights

Sethi, T. (2020). Ghostcat Vulnerability (CVE-2020-1938)  
https://www.synopsys.com/blogs/software-security/ghostcat-vulnerability-cve-2020-1938.html

---

# 👨‍💻 Author

**Taylor Wilkerson**

B.S. IT Management  
M.S. Data Analytics (In Progress)
