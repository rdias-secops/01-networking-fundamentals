# DNS 

## What is DNS?

DNS (Domain Name System) translates domain names into IP addresses.
It allows users to access websites using names like google.com instead of numerical IP addresses.

## How does DNS work?

When a user accesses a website, the device sends a DNS request to discover the IP address associated with the domain name.
After receiving the IP address, the device can communicate with the destination server.

### Example

google.com --> 142.250.x.x

github.com --> 140.82.x.x

### Common DNS Servers

| Provider     |     DNS         |
| -------------|-----------------|
| Google       |  8.8.8.8        |
| Cloudflare   |  1.1.1.1        |
| OpenDNS      |  208.67.222.222 |

## How to find your DNS Server

### Windows

Use the following command:

```cmd
ipconfig /all
```

Look for:
- DNS Servers


![Windows DNS](images/dns%20WINDOWS%20screenshot.png)

#### IMPORTANT!

In this example, the local router is being used as the DNS server instead of a public DNS service like Google DNS (8.8.8.8)


### Linux

Use the following command:

```bash
cat /etc/resolv.conf
```

Example:

nameserver 8.8.8.8

![Linux DNS](images/dns%20LINUX%20screenshot.png)

#### IMPORTANT!

In this example, the local router is being used as the DNS server.


## Why is DNS important in cybersecurity?

DNS is important in cybersecurity because attackers may abuse DNS for phishing, malicious redirections, malware communication, and DNS spoofing attacks.