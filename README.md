# 🛡️ ARP Poisoning Detector

A lightweight, passive network security tool built in Python to detect Man-in-the-Middle (MITM) ARP Spoofing attacks in real-time.

## 📖 Overview
Address Resolution Protocol (ARP) poisoning is a cyberattack where a malicious actor sends falsified ARP messages over a local area network. This links an attacker's MAC address with the IP address of a legitimate computer or server on the network. 

This script acts as a background watchdog. It passively sniffs network traffic, builds a baseline memory of safe IP-to-MAC pairings, and triggers an alert if an attacker attempts to overwrite the network's ARP cache.

## ✨ Features
* **Passive Monitoring:** Does not inject traffic into the network; operates completely silently.
* **Real-time Detection:** Instantly catches MAC address conflicts.
* **Persistent Logging:** Automatically records forensic evidence of attacks to `arp_alerts.log`.
* **Resource Efficient:** Processes packets on the fly without causing memory leaks.

## 🚀 How to Use

**1. Install Prerequisites**
You will need Python 3 and the Scapy library installed.
```bash
pip install scapy
