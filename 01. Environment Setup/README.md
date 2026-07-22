# 01. Environment Setup

![eJPT](https://img.shields.io/badge/Certification-eJPT-red)
![Level](https://img.shields.io/badge/Level-Beginner-green)
![Focus](https://img.shields.io/badge/Focus-Penetration%20Testing-blue)

Welcome to the **Environment Setup** section of this eJPTv2 preparation guide.

Before starting penetration testing, it is essential to build a correct and reliable laboratory environment. A good setup will allow you to practice safely, reproduce attacks, troubleshoot problems, and develop the skills required for the eJPT certification.

This section covers everything needed to prepare your attacker machine, understand virtualization networking, and build a strong Linux foundation.

---

# Objectives

By completing this section, you will understand:

- How the eJPT exam works.
- How to create an effective study strategy.
- How to build a Windows practice environment.
- How to install and configure Kali Linux.
- Essential Linux skills for penetration testing.
- Virtual networking concepts.
- Core networking fundamentals.

---

# Directory Structure

```
01. Environment Setup

├── 01. Exam Overview.md
├── 02. Study Strategy.md
├── 03. Windows Lab Setup.md
├── 04. Kali Linux Installation.md
├── 05. Linux Best Practices.md
├── 06. Virtual Networking NAT Bridged Host-Only.md
├── 07. Networking Fundamentals.md
└── README.md
```

---

# Learning Path

## 01. Exam Overview

Learn about:

- What the eJPT certification validates.
- Exam structure.
- Time limits.
- Required skills.
- Main exam domains.
- Recommended preparation approach.

File:

```
01. Exam Overview.md
```

---

## 02. Study Strategy

Learn how to prepare efficiently.

Topics:

- Building a learning schedule.
- Combining theory and practical labs.
- Taking effective notes.
- Practicing enumeration.
- Developing penetration testing methodology.

File:

```
02. Study Strategy.md
```

---

## 03. Windows Lab Setup

Learn how to create Windows targets for practicing attacks.

Topics:

- Installing Windows virtual machines.
- Configuring network adapters.
- Creating vulnerable environments.
- Preparing targets for exploitation.
- Creating snapshots.

File:

```
03. Windows Lab Setup.md
```

---

## 04. Kali Linux Installation

Set up your primary penetration testing machine.

Topics:

- Installing Kali Linux.
- Updating the system.
- Installing essential packages.
- Configuring the workspace.
- Preparing penetration testing tools.

File:

```
04. Kali Linux Installation.md
```

---

## 05. Linux Best Practices

Develop the Linux skills required for penetration testing.

Topics:

- Filesystem navigation.
- Permissions.
- File management.
- Process management.
- Services.
- Networking commands.
- SSH usage.

File:

```
05. Linux Best Practices.md
```

---

## 06. Virtual Networking: NAT, Bridged & Host-Only

Understand how virtual machines communicate.

Topics:

- NAT networking.
- Bridged networking.
- Host-only networks.
- Internal networks.
- Building isolated penetration testing labs.

File:

```
06. Virtual Networking NAT Bridged Host-Only.md
```

---

## 07. Networking Fundamentals

Learn the networking concepts required before starting attacks.

Topics:

- OSI model.
- TCP/IP model.
- IP addressing.
- Subnetting.
- Ports.
- TCP vs UDP.
- DNS.
- DHCP.
- Routing.
- Common protocols.

File:

```
07. Networking Fundamentals.md
```

---

# Recommended Lab Architecture

A simple eJPT practice environment:

```
                 Internet
                    |
                    |
                 NAT Adapter
                    |
              Kali Linux
                    |
          Host-Only Network
                    |
        -------------------------
        |                       |
     Windows                 Linux
     Target                 Target
```

## Kali Linux

Purpose:

- Attacker machine
- Enumeration
- Exploitation
- Post-exploitation

Network:

```
NAT + Host-Only
```

---

## Target Machines

Purpose:

- Vulnerability practice
- Exploitation
- Privilege escalation

Network:

```
Host-Only
```

---

# Required Software

Recommended virtualization platforms:

- VirtualBox
- VMware Workstation

Recommended operating systems:

### Attacker

```
Kali Linux
```

### Targets

```
Windows 10/11
Windows Server
Metasploitable
OWASP Broken Web Applications
Linux vulnerable machines
```

---

# Tools Introduced in This Section

During this section, you will prepare the environment for tools such as:

| Tool | Purpose |
|------|---------|
| Nmap | Network scanning |
| Metasploit | Exploitation framework |
| Burp Suite | Web security testing |
| Gobuster | Directory enumeration |
| Hydra | Password attacks |
| Wireshark | Network analysis |
| SQLmap | SQL injection testing |
| John the Ripper | Password cracking |

---

# Methodology

Throughout this guide, the following penetration testing methodology will be followed:

```
1. Information Gathering

        ↓

2. Enumeration

        ↓

3. Vulnerability Identification

        ↓

4. Exploitation

        ↓

5. Privilege Escalation

        ↓

6. Post-Exploitation

        ↓

7. Reporting
```

Understanding this workflow is more important than memorizing individual tools.

---

# Notes

## Practice Rule

Always try to understand:

- Why you are running a command.
- What information it provides.
- How the result affects your next step.

Avoid blindly copying commands.

---

## Documentation Rule

During every lab, maintain notes:

Example:

```
Target:
192.168.56.101

Open Ports:
22 SSH
80 HTTP
445 SMB

Findings:
- Anonymous FTP enabled
- Outdated Apache version

Exploitation:
CVE-XXXX

Credentials:
user:password
```

Professional penetration testers document everything.

---

# Completion Checklist

Before moving to the next section, you should have:

- [x] Understanding of the eJPT exam structure.
- [x] A working Kali Linux installation.
- [x] A Windows practice machine.
- [x] Understanding of virtualization networking.
- [x] Basic Linux command-line knowledge.
- [x] Basic networking knowledge.
- [x] A functional penetration testing laboratory.

---

# Next Section

Continue to:

```
02. Pentesting Fundamentals
```

In the next section, you will begin practical penetration testing techniques:

- Reverse shells
- File transfers
- Host discovery
- Nmap scanning
- Vulnerability detection
- UDP enumeration

These concepts form the foundation of the eJPT exam and real-world penetration testing.
