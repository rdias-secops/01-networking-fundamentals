# Networking Fundamentals

## Objective
Document my learning process in computer networking, focusing on core concepts that are essential for cybersecurity.

---

## Why Networking Matters in Cybersecurity
Understanding networking is fundamental in cybersecurity. Every attack, defende, and analysis depends on how systems communicate over a network.

---

## Core Concepts

### IP Address
An IP address uniquely identifies a device on a network.

- Example: 192.168.0.1
- Types:
  - Private IP (internal network)
  ex: 192.168.0.10
  -Public IP (internet)
  ex: 82.129.80.111

---

### Subnet Mask
Defines which part of the IP represents the network and which part represents the host.
 - Example: 255.255.255.0 (WRITE MORE HERE)

 ---

 ### Default Gateway
 The device responsible for routing traffic outside the local network.

 ---

### DNS (Domain Name System)
Translates domain names into IP addresses.

- Example:
google.com -> 142.250.x.x

---

### DHCP (Dynamic Host Configuration Protocol)
Automatically assigns IP addresses to devices in a network.

---

### TCP vs UDP
| Protocol | Type       | Reliability | Example Use      |
|----------|------------|------------ |------------------|
| TCP      | Connection | Reliable    | HTTP, HTTPS      |
| UDP      | Connectionless | Fast    | Streaming, DNS   |

---

### Common Ports

| Port | Service  |
|------|----------|
| 21   | FTP      |
| 22   | SSH      |
| 23   | Telnet   |
| 25   | SMTP     |
| 53   | DNS      |
| 80   | HTTP     |
| 443  | HTTPS    |
| 445  | SMB      |

## Basic Networking Commands

### Windows

```bash
ipconfig
ping google.com
tracert google.com
nslookup google.com
netstat -an

```
### Linux

```bash
ifconfig
ip a
ping google.com
traceroute google.com
nslookup google.com
netstat -tuln

```


