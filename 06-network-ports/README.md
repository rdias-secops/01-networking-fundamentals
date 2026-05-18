# Network Ports

## What are Network Ports?

Network ports are logical endpoints used for communication between devices and network services.
While an IP address identifies a device on the network, a port identifies a specific service or application running on that device.

## IP Address vs Port

Example:

192.168.1.10 -> Device IP address

192.168.1.10:443 -> HTTPS service running on port 443

Think of it like:

- IP address = building address
- Port = apartment number

## Common Network Ports

| Port | Protocol | Service | Description |
|------|------|------|------|
| 20/21 | TCP | FTP | File transfer |
| 22 | TCP | SSH | Secure remote access |
| 23 | TCP | Telnet | Remote access (insecure) |
| 25 | TCP | SMTP | Email transfer |
| 53 | UDP/TCP | DNS | Domain resolution |
| 80 | TCP | HTTP | Web communication |
| 443 | TCP | HTTPS | Secure web communication |

### Initial Port Inspection

![Empty Port Scan](images/command%20ss%20-tuln%203%20LINUX%20screenshot.png)


At first, the 'ss -tuln' command returned no listening ports because no active network services were running on the system.
The command only displays TCP and UDP ports currently opened by applications waiting for incoming connections.
Since no server, web service, or daemon was started yet, the system had nothing listening for external requests.

To demonstrate how listening ports work, a local Python HTTP server was created on port 8080.

```bash
python -m http.server 8080
```
![Open Port 8080](images/command%20ss%20-tuln%20LINUX%20screenshot.png)


After starting the server, port 8080 became visible in LISTEN state.

### Accessing the Local Web Server

The local HTTP server was accessed through the browser using:

```text
http://localhost:8080
```

![localhost:8080](images/command%20ss%20-tuln%202%20LINUX%20screenshot.png)


### Understanding 0.0.0.0:8080

The address '0.0.0.0' means the service is listening on all available  network interfaces.
Port '8080' indicates the application is waiting for HTTP connections on that specific port.

### What does LISTEN mean?

The LISTEN state indicates that a service is actively waiting for incoming client connections.

## TCP vs UDP

| TCP | UDP |
|------|------|
| Reliable | Faster |
| Connection-oriented | Connectionless |
| Error checking | Minimal error checking |
| Used in HTTPS/SSH | Used in DNS/Games/Streaming |

Examples:
- HTTPS → TCP 443
- SSH → TCP 22
- DNS → UDP 53

## Why are ports important in cybersecurity?

Open ports can expose services to the network.

Attackers often scan ports to identify running services and possible vulnerabilities.

Security analysts use port analysis to:

- detect exposed services
- identify unnecessary open ports
- monitor suspicious communication
- reduce attack surface

