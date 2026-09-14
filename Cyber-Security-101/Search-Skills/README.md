# TryHackMe — Search Skills

## 📌 Overview

**Search Skills** is a TryHackMe room that introduces techniques for efficiently finding cybersecurity information using specialized search engines, vulnerability databases, technical documentation, and online resources.

The challenge demonstrated how security professionals can use tools such as **Shodan, VirusTotal, CVE databases, Linux manual pages, and GitHub** to investigate systems, files, vulnerabilities, and technical information.

---

## 🎯 Objectives

- Learn how to search for cybersecurity information efficiently.
- Understand how Shodan can be used to gather information about internet-connected services.
- Use VirusTotal to investigate potentially suspicious files, URLs, and domains.
- Understand how CVE databases can be used to research known vulnerabilities.
- Use Linux manual pages to understand how command-line tools work.
- Use GitHub to find technical information, tools, and vulnerability-related resources.

---

## 🔍 Methodology

### 1. Search for Internet-Connected Systems

The challenge introduced **Shodan**, a search engine that indexes information about internet-connected devices and services.

Shodan can help security professionals discover information such as:

- Open ports
- Running services
- Service versions
- Exposed devices
- Network-related information

This can be useful during security research and reconnaissance.

### 2. Analyze Files and URLs

I learned how online analysis services such as **VirusTotal** can be used to investigate files, URLs, and other indicators.

These services can provide information such as:

- Malware detection results
- Security vendor detections
- File hashes
- Domain and URL information
- Relationships between indicators

This can help determine whether a file or URL may be suspicious.

### 3. Research Vulnerabilities with CVE

I learned how to search for known vulnerabilities using **CVE (Common Vulnerabilities and Exposures)** information.

A CVE provides a standardized identifier for a publicly known security vulnerability.

For example:

    CVE-YYYY-NNNNN

CVE information can help security professionals understand:

- Which software is affected.
- What version is vulnerable.
- The nature of the vulnerability.
- Available references and technical information.

### 4. Use Linux Manual Pages

One of the most useful skills I learned was using the `man` command to read the official manual documentation for Linux commands and tools.

For example:

    man nc

The manual page provides information about the command, including:

- Description
- Options
- Arguments
- Usage
- Examples
- Additional information

This means that instead of memorizing every option for every security tool, I can use the documentation directly when I need to understand how a command works.

### 5. Search Technical Documentation

The challenge also demonstrated the importance of using technical documentation when learning or troubleshooting tools.

When I encounter an unfamiliar command or tool, I can first look for its official documentation or manual page to understand how it should be used.

### 6. Use GitHub for Security Research

I learned how GitHub can be used as a valuable source of technical information.

GitHub can contain:

- Security tools
- Vulnerability research
- Proof-of-concept code
- Documentation
- Security-related projects
- References to CVEs

This makes GitHub useful for understanding how security tools work and researching known vulnerabilities.

---

## 🛠️ Tools & Techniques

| Tool / Technique | Purpose |
|---|---|
| Shodan | Search and gather information about internet-connected systems and services |
| VirusTotal | Analyze suspicious files, URLs, and security indicators |
| CVE Databases | Research publicly known vulnerabilities |
| `man` | Read documentation for Linux commands and tools |
| Technical Documentation | Understand how tools and technologies work |
| GitHub | Find security tools, research, documentation, and vulnerability information |

---

## 🧠 Key Lessons Learned

- Effective cybersecurity requires the ability to **find and understand information quickly**.
- Shodan can provide valuable information about exposed internet-connected services.
- VirusTotal can help investigate suspicious files and URLs.
- CVE databases provide standardized information about known vulnerabilities.
- The `man` command is an important Linux skill for learning how commands and their options work.
- Technical documentation should be one of the first resources to consult when using an unfamiliar tool.
- GitHub is a useful resource for finding security tools, research, documentation, and vulnerability information.
- Security professionals should learn how to research information rather than trying to memorize every command or tool.

---

## 🚩 Challenge Status

**Room:** Search Skills

**Learning Path:** Cyber Security 101

**Status:** Completed ✅

## 💡 Main Takeaway

> **A good cybersecurity professional does not need to memorize everything. Knowing how to search, read documentation, investigate vulnerabilities, and find reliable technical information is an essential security skill.**