# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---

## Scans Performed

### 1. Basic Scan
- **Command:**
# Nmap Scan Lab — TryHackMe Vulnversity

This project documents my Nmap scans against the TryHackMe Vulnversity machine.

---

## Target Machine

- **IP Address:** 10.10.95.25
- **Platform:** TryHackMe
- **Room:** Vulnversity

---


## Scans Performed

### 1. Basic Scan
- **Command:**
nmap -Pn 10.10.55.48 -oN scans1/scan_basic.txt

##summary of results
Host is up (0.17s latency).
Not shown: 849 closed ports, 146 filtered ports
PORT     STATE SERVICE
21/tcp   open  ftp
22/tcp   open  ssh
139/tcp  open  netbios-ssn
445/tcp  open  microsoft-ds
3128/tcp open  squid-http

### 2.Service Version Detection
 **Command:**
nmap -Pn -sV 10.10.13.10 -oN scans1/scan_service_detection.txt

##summary of results
Host is up (0.16s latency).
PORT     STATE SERVICE     VERSION
21/tcp   open  ftp         vsftpd 3.0.5
22/tcp   open  ssh         OpenSSH 8.2p1 Ubuntu 4ubuntu0.13 (Ubuntu Linux; protocol 2.0)
139/tcp  open  netbios-ssn Samba smbd 4.6.2
445/tcp  open  netbios-ssn Samba smbd 4.6.2
3128/tcp open  http-proxy  Squid http proxy 4.10
3333/tcp open  http        Apache httpd 2.4.41 ((Ubuntu))

### 3.OS Detection
sudo nmap -Pn -T4 -O 10.10.13.10 -oN scans1/scan_os_detection.txt
##summary of results
Host is up (0.16s latency).
No exact OS matches for host.
Network Distance: 2 hops.


### 4. Full TCP Scan (All Ports)
nmap -Pn -p 1-65535 10.10.95.25 -oN scans1/scan_full_tcp.txt
## summary of results
All 65535 scanned ports on 10.10.95.25 are filtered.
##Faster Full Tcp scan
nmap -Pn -T4 -p- --min-rate 1000 10.10.113.211 -oN scans1/scan_full_tcp_fast.txt
##summary of results
Host is up.
All 65535 scanned ports on 10.10.113.211 are filtered.
Nmap done: 1 IP address (1 host up) scanned in 140.21 seconds.

### 5.Aggressive Scan
##command used
nmap -Pn -T4 -A 10.10.113.211 -oN scans1/scan_aggressive.txt
##summary of results
Host is up.
All 1000 scanned ports on 10.10.113.211 are filtered.
Service detection performed. No services identified due to all ports filtered.


Analysis & Learnings
Filtered Ports: Many TryHackMe machines showed all ports filtered, likely due to firewall rules .

Scan Performance: Full scans without tuning were slow. Adding -T4 and --min-rate significantly reduced scan time.

Service Version Detection: Crucial for identifying vulnerabilities and understanding the environment.

OS Detection: Often inconclusive on virtualized labs, but banner info hinted at Linux distributions.

Proper Folder Management: Learned to create correct directories to avoid file writing errors during scans.



Summary:
This Nmap Scan Lab was a hands-on exercise exploring various scanning techniques. While some machines were fully filtered, the scans provided valuable insights into Nmap usage, network behavior, and common challenges in penetration testing labs.
