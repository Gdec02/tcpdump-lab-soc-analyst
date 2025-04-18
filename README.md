# Manual Packet Capture & Analysis – SOC Analyst Lab

This project simulates the responsibilities of a SOC analyst responding to a port scanning event on an internal network using manual packet capture techniques with `tcpdump`.

## 🛠️ Tools Used
- Kali Linux (Attacker)
- Metasploitable 2 (Target)
- VirtualBox
- tcpdump
- Nmap

## 🧪 Lab Objective
Capture real-time network traffic from a known attack source (Nmap scan) and analyze the packet-level behavior to identify indicators of compromise.

## 🔁 Scenario

- The Kali VM runs an Nmap scan targeting Metasploitable.
- Metasploitable uses `tcpdump` to capture real-time logs of the scanning activity.

## 📋 Key Commands

### On Metasploitable (Target):
```bash
tcpdump -i eth0 host 192.168.56.101
```
Captures all incoming traffic from the attacking machine (Kali).

### On Kali (Attacker):
```bash
nmap -sS -sV 192.168.56.102
```
Performs a stealth scan with service detection.

## 🔍 SOC Relevance
In a real SOC environment, tools like Splunk and Reliaquest GreyMatter ingest logs and generate alerts. However, analysts often rely on tools like `tcpdump` or `Wireshark` during:

- Incident response investigations
- Network troubleshooting
- Verifying suspicious activity
- Capturing forensic evidence

This manual packet capture emulates the core decision-making process and investigative mindset of a SOC analyst.

## 📁 Files
- `commands.txt`: Summary of the exact commands used
- `tcpdump_use_cases.md`: When and why SOC analysts use manual packet capture
