# Privilege Escalation

> **Difficulty:** Beginner - Intermediate  
> **Focus:** Linux & Windows Privilege Escalation  
> **Certification:** eJPT Preparation

---

# Introduction

Privilege Escalation is the process of gaining higher permissions after obtaining initial access to a system.

During a penetration test, attackers commonly start with a low-privileged account. The objective is to identify weaknesses that allow access to administrator or root privileges.

The main goal:

```
Low Privileged User

↓

Administrator / Root

↓

Full System Control
```

Privilege escalation is a critical phase after exploitation because gaining initial access does not always provide complete control over the target.

---

# Why Privilege Escalation Matters

A compromised low-level account usually has limited permissions.

Examples:

Linux:

```
user
```

Windows:

```
NT AUTHORITY\LOCAL SERVICE
```

These accounts cannot normally:

- Access sensitive files
- Modify system settings
- Install software
- Control services
- Access administrator data

Privilege escalation allows penetration testers to demonstrate the real impact of a vulnerability.

---

# Privilege Escalation Types

There are two main categories:

---

# Vertical Privilege Escalation

Increasing privileges on the same system.

Example:

```
Normal User

↓

Administrator

↓

SYSTEM / Root
```

Common techniques:

- SUID exploitation
- Sudo abuse
- Weak permissions
- Service exploitation
- Token impersonation

---

# Horizontal Privilege Escalation

Accessing another user account with similar privileges.

Example:

```
User A

↓

User B
```

Common techniques:

- Credential reuse
- Password attacks
- Session hijacking
- Stored credentials

---

# Privilege Escalation Methodology

A typical workflow:

```
Initial Access

↓

Identify Current User

↓

Collect System Information

↓

Enumerate Privileges

↓

Search For Weaknesses

↓

Exploit Misconfiguration

↓

Obtain Root / Administrator

```

---

# Enumeration Phase

Enumeration is the most important part of privilege escalation.

Never exploit blindly.

The first step is understanding the environment.

---

# Linux Privilege Escalation Enumeration

Important information:

## Current User

```bash
whoami
```

or:

```bash
id
```

---

## System Information

```bash
uname -a
```

Shows:

- Kernel version
- Architecture
- Operating system information

---

## User Information

```bash
cat /etc/passwd
```

Look for:

- Users
- Service accounts
- Interesting accounts

---

## Sudo Permissions

```bash
sudo -l
```

Important because:

```
User can execute command as root
```

---

## SUID Files

Search:

```bash
find / -perm -4000 2>/dev/null
```

Look for:

- Dangerous binaries
- Misconfigured programs

---

## Cron Jobs

Check:

```bash
cat /etc/crontab
```

Look for:

- Writable scripts
- Root scheduled tasks

---

# Windows Privilege Escalation Enumeration

Important commands:

---

## Current User

```cmd
whoami
```

---

## User Privileges

```cmd
whoami /priv
```

Look for:

```
SeImpersonatePrivilege
```

---

## System Information

```cmd
systeminfo
```

Collect:

- Windows version
- Patch level
- Architecture

---

## Users

```cmd
net users
```

---

## Administrators

```cmd
net localgroup administrators
```

---

## Services

```cmd
sc query
```

Look for:

- Weak permissions
- Vulnerable services

---

# Linux Privilege Escalation Topics

This section covers:

---

# 01. Linux PrivEsc Basics

Fundamentals of Linux privilege escalation.

Topics:

- Linux permissions
- Users and groups
- Enumeration commands
- System information gathering
- Common escalation paths

---

# 02. Sudo Misconfiguration

Sudo allows users to execute commands with elevated privileges.

Example:

```bash
sudo -l
```

Potential issues:

- Allowed commands
- Dangerous binaries
- Incorrect sudo rules

Common abuses:

- GTFOBins
- Command injection
- Shell escapes

---

# 03. SUID Exploitation

SUID binaries execute with the owner's privileges.

Example:

```
-rwsr-xr-x root root binary
```

Enumeration:

```bash
find / -perm -4000 2>/dev/null
```

Common vulnerable binaries:

- find
- vim
- python
- bash
- nmap

---

# Windows Privilege Escalation Topics

This section covers:

---

# 04. Windows PrivEsc Basics

Introduction to Windows privilege escalation.

Topics:

- Windows users
- Security model
- ACL permissions
- Tokens
- Services
- Registry

---

# 05. User Enumeration

Understanding Windows accounts.

Topics:

- Local users
- Domain users
- Groups
- Administrator discovery
- Service accounts

Commands:

```cmd
whoami

net users

net localgroup administrators
```

---

# 06. Automated Enumeration Tools

Automating privilege escalation discovery.

Tools covered:

## Linux

- LinPEAS
- LinEnum
- Linux Exploit Suggester

## Windows

- WinPEAS
- PowerUp
- Seatbelt
- PrivescCheck
- BloodHound

---

# Common Privilege Escalation Techniques

## Weak File Permissions

Example:

```
Root/SYSTEM executes file

↓

User can modify file

↓

Replace content

↓

Gain privileges
```

---

## Vulnerable Services

Example:

```
SYSTEM service

↓

Writable executable

↓

Replace binary

↓

SYSTEM shell
```

---

## Stored Credentials

Search:

- Configuration files
- Scripts
- Registry
- Backups

Examples:

```
password.txt

config.xml

database.conf
```

---

## Kernel Exploits

Process:

```
Identify Version

↓

Search Vulnerabilities

↓

Exploit

↓

Elevate Privileges
```

---

## Token Abuse

Windows-specific.

Common privileges:

```
SeImpersonatePrivilege

SeDebugPrivilege

SeBackupPrivilege
```

---

# Common Tools

## Enumeration

- LinPEAS
- WinPEAS
- PowerUp
- BloodHound
- Seatbelt

---

## Exploitation

- GTFOBins
- Metasploit
- Searchsploit
- Exploit-DB

---

# Recommended Workflow

Professional methodology:

```
Gain Initial Access

↓

Identify User

↓

Enumerate System

↓

Check Privileges

↓

Search Misconfigurations

↓

Research Vulnerability

↓

Exploit

↓

Obtain Higher Privileges

↓

Maintain Access
```

---

# eJPT Exam Focus

Privilege escalation is a major part of penetration testing.

Focus on:

Linux:

- sudo -l
- SUID binaries
- Weak permissions
- Cron jobs

Windows:

- User enumeration
- Service vulnerabilities
- Stored credentials
- Token privileges

Tools:

- LinPEAS
- WinPEAS
- PowerUp

---

# Practical Tips

- Always enumerate before exploiting.
- Understand why a vulnerability works.
- Verify automated findings manually.
- Check common misconfigurations first.
- Keep detailed notes.
- Look for credentials everywhere.
- Privilege escalation often depends on small mistakes.

---

# Summary

Privilege escalation is one of the most important skills in penetration testing.

In this section, you learned:

- Linux privilege escalation fundamentals
- Sudo abuse
- SUID exploitation
- Windows privilege escalation basics
- User enumeration
- Automated enumeration tools
- Common escalation techniques

These skills are essential for the **eJPT certification** and provide the foundation required for more advanced certifications such as **eCPPT and OSCP**.

---

# What's Next?

➡ **08. Pivoting & Tunneling**

Next section:

- Pivoting concepts
- Network discovery
- SSH tunneling
- Proxychains
- Port forwarding
- Internal network attacks
- Lateral movement basics
```
```
