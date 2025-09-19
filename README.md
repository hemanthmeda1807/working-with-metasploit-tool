# Metasploitable2 Training Lab — Metasploit Usage (Ethical & Educational)

> **Purpose:** Guidance for safely using Metasploit in a controlled, authorized training lab.  
> **Important:** This repository deliberately does **not** contain step-by-step exploit instructions. Use Metasploit only in isolated environments you own or are explicitly authorized to test.

---

## ⚠️ Legal & Safety Notice

- This lab is for authorized, educational use **only**. Do **not** attempt to scan, attack, or access systems you do not own or do not have explicit written permission to test.
- Always follow local laws, your organization’s policy, and ethical guidelines.
- Keep the lab **air-gapped** or on a host-only / internal virtual network to avoid affecting other systems.
- Create snapshots before experimenting and restore snapshots after tests.

---

## 🧰 Prerequisites

- Host machine with enough RAM/CPU to run VMs (recommended ≥ 8 GB RAM)
- Virtualization software (e.g., VirtualBox, VMware Workstation)
- Metasploitable2 VM (download from https://sourceforge.net/projects/metasploitable/files/latest/download)
- Kali Linux or another defensive/security distro for learning tools (optional)
- Basic familiarity with VM snapshots, networks, and Linux commands

---

## 🔧 Safe Lab Setup (Recommended)

1. Create a new VM network that is **host-only** or internal (no Internet routing).
2. Import the Metasploitable2 OVA into your VM software.
3. Add a second VM (Kali or similar) on the same internal network for testing and observation.
4. Ensure both VMs cannot reach your home/office network or the Internet unless intentionally allowed.
5. Take snapshots of all VMs before making changes.
6. Use separate folders for logs and exports; do not store sensitive host data in VM shares.

---
## Working (Authorized Lab Use Only)

> **Important:** The following describes *authorized reconnaissance steps* for a controlled, isolated training lab that you own or have explicit written permission to test. Do **not** run scans or tests against systems you do not own or are not authorized to test.
- **Lab roles**
  - `Metasploitable2` — victim machine 
  - `Kali Linux` — hacker machine  
- Before using any exploitation framework, perform **authorized reconnaissance** to understand the target's exposed services and state in the lab environment.
- Use a reputable port/service scanner to enumerate open ports and identify running services. Example commands (use only in an isolated, permitted lab):
  ```bash
  # Aggressive scan (OS, services, scripts) — authorized lab use only
  nmap -A <ip-address>

  # Service/version detection only — authorized lab use only
  nmap -sV <ip-address>

<img width="1137" height="582" alt="Screenshot 2025-09-19 211933" src="https://github.com/user-attachments/assets/660d71d4-9a6a-4899-9473-295f8a043758" />

### port-1 :- PORT - 22/TCP  SERVICE - ftp  VERSION - vsftpd 2.3.4 ###

> Service version vsftpd 2.3.4 is a backdoor
> 



