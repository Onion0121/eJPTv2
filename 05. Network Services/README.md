# Network Services

Windows and Linux systems expose a variety of network services that allow administrators and users to remotely access resources, share files, manage systems, and monitor devices. While these services are essential for daily operations, they also represent common attack surfaces that penetration testers must understand.

This section focuses on identifying, enumerating, and interacting with some of the most frequently encountered network services during penetration tests and the **INE eJPT** exam.

---

# Learning Objectives

After completing this section, you should be able to:

- Understand the purpose of common network services.
- Identify services using Nmap and service detection.
- Enumerate SMB shares and users.
- Perform Samba reconnaissance.
- Use RPC Client to gather Windows domain information.
- Enumerate SNMP devices and extract useful information.
- Understand Remote Desktop Protocol (RDP) authentication and enumeration.
- Exploit insecure IIS upload functionality using ASPX Web Shells.
- Recognize common misconfigurations and security weaknesses.

---

# Topics Covered

## SMB Enumeration

Learn how to enumerate Windows SMB shares, identify accessible resources, and gather information about users, permissions, and shared folders.

Topics include:

- SMB versions
- Anonymous shares
- SMB scripts
- smbclient
- Nmap NSE
- CrackMapExec
- Enum4linux

---

## Samba Enumeration

Discover Linux Samba servers and enumerate available shares, users, and configuration weaknesses.

Topics include:

- Samba reconnaissance
- Share enumeration
- Anonymous access
- Version detection
- Samba vulnerabilities

---

## RPC Client

Learn how to use **rpcclient** to enumerate Windows domains and Active Directory environments.

Topics include:

- Anonymous authentication
- User enumeration
- Group enumeration
- Password policies
- RID cycling
- Domain information

---

## Remote Desktop Protocol (RDP)

Understand how to identify and assess Windows Remote Desktop services.

Topics include:

- Service detection
- Nmap RDP scripts
- FreeRDP
- Password attacks
- BlueKeep detection
- Credential reuse

---

## SNMP Enumeration

Learn how to extract valuable information from devices exposing SNMP.

Topics include:

- UDP scanning
- Community strings
- SNMPWalk
- SNMPCheck
- Useful OIDs
- Metasploit SNMP modules

---

## IIS ASPX Web Shell

Explore how insecure IIS file upload functionality can lead to remote code execution.

Topics include:

- IIS identification
- File upload vulnerabilities
- ASPX Web Shells
- Msfvenom payload generation
- Reverse shells
- Basic Windows post-exploitation

---

# Recommended Workflow

A typical enumeration process during a penetration test looks like this:

```
Host Discovery
        │
        ▼
Port Scanning (Nmap)
        │
        ▼
Service Identification
        │
        ▼
SMB Enumeration
        │
        ▼
RPC Enumeration
        │
        ▼
SNMP Enumeration
        │
        ▼
RDP Assessment
        │
        ▼
IIS Enumeration
        │
        ▼
Credential Discovery
        │
        ▼
Initial Access
```

---

# Common Tools

Throughout this section, you will frequently use:

- Nmap
- smbclient
- enum4linux
- rpcclient
- CrackMapExec (NetExec)
- snmpwalk
- snmp-check
- Hydra
- Gobuster
- Nikto
- Metasploit Framework
- Msfvenom
- xfreerdp
- davtest

---

# eJPT Exam Tips

For the eJPT exam, remember these key points:

- Always perform thorough service enumeration before attempting exploitation.
- Anonymous SMB and RPC access are common in lab environments.
- SNMP often leaks valuable information without authentication.
- Reuse credentials discovered on one service against others such as SMB, RDP, SSH, or web applications.
- Enumerate before exploiting—most successful attacks begin with good reconnaissance.
- Document every finding, including usernames, shares, services, and credentials.

---

# Conclusion

Network service enumeration is one of the most important phases of any penetration test. A properly executed enumeration process often reveals the information needed to obtain initial access without relying on complex exploits.

By mastering the techniques in this section, you will be prepared to identify common Windows and Linux services, gather critical information, discover credentials, and leverage exposed services during the **INE eJPT** exam and real-world penetration testing engagements.

**Next Section:** **06. CMS Security**
