# TCP/IP

## What is TCP/IP?

TCP/IP is a suite of communication protocols used to connect devices and transmit data across networks and the internet.

## What is IP?

IP (Internet Protocol) is responsible for addressing and routing packets between devices across networks.

## What is TCP?

TCP (Transmission Control Protocol) is responsible for reliable communication between devices.
It ensures that data arrives correctly, in order, and without loss.

## How TCP/IP works

When a device accesses a website:

1. DNS translates the domain name into an IP address.
2. IP identifies the destination.
3. TCP establishes a reliable connection.
4. Data is transmitted between devices.


#### Basic Connectivity Test

The 'ping' command was used to test basic network connectivity.


```bash
ping -c 10 google.com
```


![Ping test using google.com](images/tcp-ip%20ping%20LINUX%20screenshot.png)



In this example, the domain 'google.com' was automatically resolved into the IP address '142.250.79.206' through DNS resolution.


## TCP Handshake

SYN -> SYN-ACK -> ACK

### Handshake explication

TCP uses a three-way handshake to establish a connection between devices.

- SYN: initiates the connection
- SYN-ACK: acknowledges the request
- ACK: confirms the connection

### Example of Communication

User accesses:

google.com

DNS resolves the domain name into an IP address.

TCP establishes the connection.

Data is exchanged between the client and the server.

### TCP Packet Analysis with Wireshark

The following capture shows TCP packets captured with Wireshark during network communication.

Highlighted elements:

- Source and destination IP addresses
- TCP acknowledgment packets (ACK)
- TLSv1.3 encrypted communication
- HTTPS communication over port 443



![TCP Analysis](images/wireshark%20analysis%20LINUX%20screenshot.png)


### TCP Stream Analysis

The TCP Stream feature allows analysts to follow the communication flow between two hosts.
In this example, the captured traffic appears unreadable because the communication is encrypted using TLS.
This demonstrates how HTTPS protects transmitted data.


![TCP Stream Analysis](images/tcp-stream-analysis%20LINUX%20screenshot.png)


## Common Protocols

| Protocol |       Function           |
|-------------------------------------|
| HTTP     | Web communication        |
| HTTPS    | Secure web communication |
| DNS      | Domain name resolution   |
| SSH      | Secure remote access     |
| FTP      | File transfer            |

## Why is TCP/IP important in cybersecurity?

Understanding TCP/IP is essential in cybersecurity because attackers and defenders analyze packets, ports, protocols, and network communication during attacks and defensive operations. For example:

- packet analysis
- port scanning
- MITM
- SYN Flood
- sniffing
