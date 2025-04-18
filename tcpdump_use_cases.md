# 🧠 When SOC Analysts Use tcpdump or Packet Capture

While SIEM tools handle most log ingestion, SOC analysts use `tcpdump` or `Wireshark` when:

1. Logs are missing or incomplete
2. They need to observe **live traffic behavior**
3. A system is compromised and needs **forensic review**
4. They are validating firewall rules or detection logic
5. Testing and learning in lab environments

## 🔎 Common Use Cases

| Use Case | Command |
|----------|---------|
| Investigating a live scan | tcpdump -i eth0 host [attacker_ip] |
| Capture all traffic except SSH | tcpdump -i eth0 port not 22 |
| Save packets for later | tcpdump -i eth0 -w capture.pcap |

Manual packet capture reinforces the skills needed for deep analysis beyond SIEM alerts.
