# Chapter 1: Getting Started with the Basics  
       *Linux Basics for Hackers*

## Overview
This chapter introduces the foundational concepts of Linux that are essential for anyone entering the field of cybersecurity and ethical hacking. Linux is the backbone of most hacking tools, servers, and security environments. Mastering these basics is mandatory before moving to advanced exploitation techniques.

---

## Why Linux is Important for Cybersecurity
- Linux is the most widely used operating system in cybersecurity.
- Most penetration testing and forensic tools are built for Linux.
- Web servers, cloud infrastructure, routers, and firewalls commonly run Linux.
- Understanding Linux gives low-level control over systems, which is crucial for attackers and defenders.

---

## Linux Distributions (Distros)
- Linux comes in many distributions designed for different purposes.
- Security-focused distributions include tools for:
  - Penetration testing
  - Digital forensics
  - Network analysis
  - Malware research
- Kali Linux is the most popular distribution for ethical hacking and learning cybersecurity.

---

## GUI vs Command Line Interface (CLI)
### Graphical User Interface (GUI)
- Easy for beginners
- Mouse-based interaction
- Limited power and automation

### Command Line Interface (Terminal)
- Fast and powerful
- Allows automation and scripting
- Preferred by hackers and security professionals

⚠️ Real-world hacking is performed primarily using the terminal, not the GUI.

---

## Linux File System Structure
Linux uses a single-rooted directory structure (`/`) instead of drive letters.

Important directories:
- `/` – Root of the filesystem
- `/home` – User home directories
- `/root` – Root user’s home directory
- `/etc` – System configuration files
- `/bin` – Essential command binaries
- `/var` – Logs and variable data

Understanding the file system is critical for:
- Privilege escalation
- Log analysis
- Malware placement
- System enumeration

---

## Basic Linux Commands
Some essential commands introduced:
- `pwd` – Display current working directory
- `ls` – List files and directories
- `cd` – Change directory
- `whoami` – Show current user
- `man` – View command manuals

These commands help in navigating and understanding the system environment.

---

## Getting Help in Linux
Linux provides built-in documentation tools:
- `man <command>` – Detailed manual pages
- `<command> --help` – Quick usage reference

A strong cybersecurity learner must be able to read and understand manual pages independently.

---

## Root User vs Normal User
- Normal users have restricted permissions.
- Root user has complete control over the system.
- Many attacks aim to escalate privileges from a normal user to root.

Understanding user roles is the foundation of privilege escalation techniques.

---

## Key Takeaways
- Linux knowledge is essential for cybersecurity.
- Terminal proficiency is more important than GUI familiarity.
- Understanding the file system reveals attack surfaces.
- Command-line fluency improves speed and confidence.
- Root access represents full system compromise.

---

## Learning Status
- [x] Understood Linux importance
- [x] Learned basic filesystem structure
- [x] Practiced basic commands
- [ ] Daily terminal practice (ongoing)

---

 This chapter builds the foundation for all future cybersecurity learning.