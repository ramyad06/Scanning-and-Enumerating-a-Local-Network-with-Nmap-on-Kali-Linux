# Scanning-and-Enumerating-a-Local-Network-with-Nmap-on-Kali-Linux
This project demonstrates how to use Nmap on Kali Linux to scan and enumerate devices on a local network. It includes active host discovery, port scanning, service detection, and OS fingerprinting.

By the end of this project, I did-
- Perform **host discovery** on a network.
- Identify **open ports** and running services.
- Detect **operating systems and firewall rules**.
- Enumerate devices and analyze network security.

---

## Pre-requisites
- Basic understanding of **networking concepts** (IP addresses, ports, and protocols).
- Familiarity with using the **command line interface (CLI)**.
- **Kali Linux** installed (either on a **virtual machine**, **dual boot**, or as a **live boot**).
- A **local network** with multiple connected devices (computers, routers, IoT devices, etc.).

---

## Lab Set-up and Tools

### Tools Required:
- **Kali Linux** – A Debian-based Linux distribution for penetration testing.
- **Nmap** – A network scanning and security auditing tool (pre-installed on Kali Linux).
- **A Local Network** – Multiple connected devices for enumeration and scanning.

### Installation:
Nmap is **pre-installed** on Kali Linux. However, you can verify or update it using the following command:
```bash
sudo apt-get update && sudo apt-get install -y nmap
```
---

## 🔧 Commands Used

**Scan for active hosts**  
```bash
nmap -sn 192.168.1.0/24
```
![Scan Result](Aggressive Scan (Includes OS, Services, and Traceroute).png)

Use: Performs a "ping scan" to identify live hosts without scanning their ports.

**Scan for Open Ports on a Single Host**  
```bash
nmap -p- 192.168.1.1
```
Use: Scans all 65,535 ports on the target device to find open ones.

**Detect Running Services and Their Versions**
```bash
nmap -sV 192.168.1.1
```
Use: Identifies open ports and determines the versions of running services.

**Perform OS Detection**
```bash
nmap -O 192.168.1.1
```
Use: Uses TCP/IP fingerprinting to detect the operating system of the target.

**Aggressive Scan (Includes OS, Services, and Traceroute)**
```bash
nmap -A 192.168.1.1
```
Use: Runs OS detection, service version detection, script scanning, and traceroute in one command.

**Scan a Subnet for All Active Devices and Their Open Ports**
```bash
nmap -sS -p 22,80,443 192.168.1.0/24
```
Use: Performs a Stealth SYN scan on ports 22 (SSH), 80 (HTTP), and 443 (HTTPS) for all devices on the subnet.

**Detect Firewall and Perform an Intense Scan**
```bash
nmap -sS -sV -O -A -T4 192.168.1.1
```
Use: Runs a stealth scan, detects OS and services, applies aggressive timing (T4), and detects firewall presence.





