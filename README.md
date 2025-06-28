# 🛡️ SOC Home Lab – Blue Team Attack & Defense Simulation

## 📌 Overview

This project documents a personal SOC (Security Operations Center) lab that simulates real-world blue team scenarios: packet captures, log ingestion, detection, and basic threat hunting using tools like **Wireshark**, **Splunk**, and **Metasploit**.

---

## 🎯 Objectives

- Analyze packet captures (PCAP) using Wireshark
- Detect simulated malicious behavior (e.g., scans, exploits)
- Ingest logs into Splunk for analysis
- Simulate threat actor behavior using Metasploit
- Build a structured, documented portfolio for cybersecurity job readiness

---

## 🖥️ Lab Environment

| Component        | Description                               |
|------------------|-------------------------------------------|
| Host System      | Any OS (macOS, Windows, Linux)            |
| Virtualization   | UTM, VirtualBox, VMware, or Hyper-V       |
| Guest OS         | Kali Linux (2024.1)                       |
| Tools Installed  | Wireshark, Splunk, Metasploit             |

> 💡 _I used UTM on macOS, but this guide is platform-independent and works on VirtualBox, VMware, or Hyper-V._

---

## ⚙️ Setup Instructions

### 1. Install Virtualization + Kali Linux

- Download a virtualization platform (UTM, VirtualBox, VMware, Hyper-V)
- Download Kali ISO: https://www.kali.org/get-kali/
- Create a VM: 2 CPUs, 4GB RAM, network bridged or shared
- Install Kali inside the VM

### 2. Install Core Tools in Kali

```bash
# Wireshark
sudo apt update && sudo apt install wireshark -y

# Metasploit (pre-installed in Kali)
msfconsole

# Splunk
wget <Splunk_DEB_URL>
sudo dpkg -i splunk*.deb
sudo /opt/splunk/bin/splunk start --accept-license
```

---

## 🔬 Simulated Scenarios

| Scenario                      | Tool        | Outcome                             |
|------------------------------|-------------|-------------------------------------|
| ICMP scan + traffic sniffing | Wireshark   | Filters, frame inspection           |
| Exploit with Metasploit      | Metasploit  | Created event logs in Splunk        |
| Log correlation              | Splunk      | Dashboards, alert rules             |

---

## 📁 Project Structure

```bash
SOC-Home-Lab/
├── README.md
├── wireshark/
│   └── ICMP-capture.pcap
├── splunk/
│   └── dashboard-screenshot.png
├── metasploit/
│   └── session-log.txt
└── screenshots/
    ├── lab-topology.png
    ├── splunk-ui.png
```

---

## 📸 Screenshots

Screenshots of:
- Network capture in Wireshark
- Splunk ingestion & dashboard
- Metasploit terminal logs

---

## 📄 Lessons Learned

- How packet capture tools help analyze suspicious activity
- SIEM tools like Splunk can visualize and correlate events
- Simulating attacker behavior sharpens defensive mindset

---

## 📚 Future Plans

- Add ELK Stack or Security Onion to simulate large-scale ingestion
- Integrate Windows logs using Wazuh agent
- Document threat hunting methods with MITRE ATT&CK mapping

---

## ✍️ Author

**Ibrahim Musa**  
Cybersecurity Master's Student – Paris  
Aspiring SOC Analyst | Blue Team Focus  
📫 [LinkedIn](https://linkedin.com/in/ibrahim-musa-m)

---

## 🪪 License

MIT – feel free to fork, adapt, and build on this lab.
