# CMS Security

> **Difficulty:** Beginner  
> **Estimated Completion Time:** 3-4 Hours

---

# Introduction

Content Management Systems (CMS) are platforms that allow users to create, manage, and publish digital content without requiring extensive programming knowledge.

Popular CMS platforms include:

- WordPress
- Drupal
- Joomla
- Magento
- Ghost

Because CMS platforms are widely used on the internet, they are frequent targets during penetration tests.

Attackers commonly target:

- Outdated CMS versions
- Vulnerable plugins and modules
- Weak administrator credentials
- Insecure configurations
- File upload vulnerabilities
- Authentication weaknesses
- Exposed configuration files

A penetration tester must understand how to identify, enumerate, and exploit CMS installations.

---

# Learning Objectives

After completing this section, you should be able to:

- Identify common CMS platforms
- Perform CMS reconnaissance
- Enumerate users, plugins, themes, and modules
- Detect outdated CMS versions
- Search for known vulnerabilities
- Exploit common CMS weaknesses
- Use CMS enumeration tools
- Perform post-exploitation after CMS compromise
- Understand common CMS security defenses

---

# Topics Covered

## 01. WordPress Enumeration

Learn how to identify and enumerate WordPress installations.

Topics include:

- WordPress architecture
- Identifying WordPress websites
- WordPress directories
- Version detection
- User enumeration
- Theme enumeration
- Plugin enumeration
- Interesting files
- WPScan usage
- Directory brute forcing
- Common WordPress misconfigurations

Tools covered:

- WPScan
- Gobuster
- Curl

---

## 02. WordPress Exploitation

Learn how to exploit common WordPress vulnerabilities.

Topics include:

- Weak administrator credentials
- WordPress brute force attacks
- XML-RPC attacks
- Vulnerable plugins
- Vulnerable themes
- File upload vulnerabilities
- Theme editor exploitation
- WordPress Metasploit modules
- Reverse shell deployment
- Post-exploitation techniques

Common attack workflow:

```
Identify WordPress
|
Enumerate Users
|
Enumerate Plugins
|
Find Vulnerabilities
|
Exploit
|
Obtain Shell
|
Privilege Escalation
```

---

## 03. Drupal Security Assessment

Learn how to perform security assessments against Drupal installations.

Topics include:

- Drupal architecture
- Identifying Drupal websites
- Version enumeration
- Module enumeration
- Theme enumeration
- User discovery
- Configuration file discovery
- Droopescan usage
- Directory enumeration
- Drupal vulnerabilities
- Drupalgeddon vulnerabilities
- Remote Code Execution
- Post-exploitation

Important files:

```
CHANGELOG.txt

README.txt

sites/default/settings.php
```

Tools covered:

- Droopescan
- Gobuster
- Searchsploit
- Metasploit

---

## 04. Joomla Security Assessment

Learn how to identify and exploit Joomla installations.

Topics include:

- Joomla identification
- Joomla version detection
- Component enumeration
- Template enumeration
- User enumeration
- Extension discovery
- Vulnerable Joomla components
- Configuration files
- Known Joomla vulnerabilities
- Exploitation techniques
- Post-exploitation

Tools covered:

- Joomscan
- Gobuster
- Searchsploit
- Metasploit

---

# CMS Enumeration Methodology

A common CMS assessment workflow:

```
Website Reconnaissance

↓

Identify CMS

↓

Detect Version

↓

Enumerate Components

↓

Find Vulnerabilities

↓

Exploit Vulnerability

↓

Obtain Access

↓

Post-Exploitation

↓

Privilege Escalation
```

---

# Common CMS Attack Vectors

## Weak Credentials

Many CMS compromises happen because administrators use:

- Default passwords
- Weak passwords
- Password reuse

Examples:

```
admin:admin

admin:password

administrator:123456
```

---

## Vulnerable Plugins and Modules

Third-party extensions are one of the biggest risks.

Common vulnerabilities:

- Remote Code Execution
- SQL Injection
- File Upload
- Authentication Bypass
- Local File Inclusion

---

## Outdated Versions

Older CMS versions often contain publicly known vulnerabilities.

Always check:

- CMS version
- Plugin versions
- Module versions
- Theme versions

Search vulnerabilities:

```bash
searchsploit cms-name
```

---

## File Upload Vulnerabilities

Poorly configured upload systems can allow attackers to upload:

- Web shells
- Malicious scripts
- Backdoors

Attack flow:

```
Upload File

↓

Execute File

↓

Obtain Shell
```

---

# Common CMS Tools

## Enumeration

- WPScan
- Droopescan
- Joomscan
- Gobuster
- Nikto

## Exploitation

- Metasploit
- Searchsploit
- Burp Suite

## Post Exploitation

- Netcat
- LinPEAS
- WinPEAS
- Manual enumeration

---

# eJPT Exam Focus

CMS security is an important part of web application penetration testing.

Focus on:

- Identifying CMS platforms
- Running enumeration tools
- Finding vulnerable plugins/modules
- Searching public exploits
- Exploiting weak credentials
- Uploading shells
- Understanding post-exploitation

Remember:

```
Enumeration First

↓

Exploit Second
```

Never attack blindly.

---

# Practical Tips

- Always identify the CMS before attacking.
- Check versions before searching exploits.
- Enumerate plugins and modules.
- Look for backup files.
- Check configuration files.
- Test default credentials.
- Search public vulnerabilities.
- Keep detailed notes.

---

# Summary

In this section, you learned how to assess the security of popular CMS platforms.

You covered:

- WordPress enumeration
- WordPress exploitation
- Drupal security assessment
- Joomla security assessment
- CMS reconnaissance
- Vulnerability discovery
- Exploitation techniques
- Post-exploitation methodology

CMS security knowledge is essential for web penetration testing and is directly applicable to the **eJPT certification exam**.

---

# What's Next?

➡ **07. Pivoting & Tunneling**

The next section introduces internal network movement techniques, including:

- Pivoting concepts
- Port forwarding
- SSH tunneling
- Proxychains
- Routing through compromised hosts
- Internal network enumeration
- Lateral movement basics
```
