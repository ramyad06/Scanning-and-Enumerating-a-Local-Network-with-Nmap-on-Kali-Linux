# Scanning-and-Enumerating-a-Local-Network-with-Nmap-on-Kali-Linux
This project demonstrates how to use Nmap on Kali Linux to scan and enumerate devices on a local network. It includes active host discovery, port scanning, service detection, and OS fingerprinting.

## 🔧 Commands Used

**Scan for active hosts**  
```bash
nmap -sn 192.168.1.0/24
Use: Performs a "ping scan" to identify live hosts without scanning their ports.

**Scan for Open Ports on a Single Host**  
```bash
nmap -p- 192.168.1.1
Use: Scans all 65,535 ports on the target device to find open ones.





