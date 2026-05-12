# Default Gateway

## What is a Default Gateway?

A default gateway is the device responsible for forwarding traffic from a local network to other networks, such as the internet.
In most home networks, the router acts as the default gateway.

## How does it work?

When a device wants to communicate with another device outside its local network, the traffic is sent to the default gateway.
The gateway then forwards the traffic to the correct destination.

### Example

Device IP: 192.168.0.10
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.0.1

Explanation:
- .10 = your device/host
- .1 = router/gateway

## How to Find your Default Gateway

### Windows

Use the following command in Command Prompt:

```cmd
ipconfig
```

![Windows Default Gateway](images/default-gateway%20WINDOWS%20screenshot.png)


Look for: Default Gateway

### Linux

Use the following command:

```bash
ip route
```

![Linux Default Gateway](images/default-gateway%20LINUX%20screenshot.png)


Example: 

```bash
default via 192.168.0.1 dev eth0
```

'192.168.0.1' is the default gateway.

## Why is it important in cybersecurity?

Understanding the default gateway is important in cybersecurity because attackers and defenders often analyze network routes, traffic flow, firewall rules, and communication between networks.

The gateway is also a common target in attacks such as:
- Man-in-the-Middle (MITM)
- ARP Spoofing
- Rogue Gateway attacks


