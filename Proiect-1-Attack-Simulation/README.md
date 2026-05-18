# Project 1 - Full Attack Simulation

Reconnaissance to exploitation on Metasploitable 2, including a full Wireshark capture and CVE-2007-2447 exploitation.

## Full writeup

Read the complete walkthrough with methodology, findings, and application security takeaways:

**[mihaitapalaga.dev/blog/metasploitable-attack-simulation](https://mihaitapalaga.dev/blog/metasploitable-attack-simulation)**

## What's in this folder

| Path | Description |
|------|-------------|
| `captures/Proiect 1.pcapng` | Full Wireshark capture of the attack chain. Open in Wireshark to walk through traffic phase by phase. |
| `screenshots/` | High-resolution screenshots of each attack phase (recon, scanning, exploitation, shell, post-exploitation). |

## Quick summary

- Target: Metasploitable 2 (Ubuntu 8.04) on isolated VirtualBox host-only network
- Recon: netdiscover to find live hosts on 192.168.56.0/24
- Scanning: Nmap with version detection and default scripts, OS fingerprinting
- Exploitation: CVE-2007-2447, Samba 3.0.20 Username Map Script RCE via Metasploit
- Post-exploitation: read /etc/shadow, demonstrate root access scope
- Traffic analysis: Wireshark capture annotated by attack phase

Full repository at the root README: [../README.md](../README.md)
