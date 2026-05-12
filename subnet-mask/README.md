# Subnet Mask

## What is a subnet mask?

A subnet mask defines which part of an IP address represents the network and which part represents the host.
It helps devices determine whether another device is inside the same local network or if traffic must be sent to the default gateway.

### Example

IP Address: 192.168.0.10
Subnet Mask: 255.255.255.0

Explanation:
- 192.168.0 = network
- .10 = host/device

### CIDR Notation

255.255.255.0 = /24


## Why is subnetting important in cybersecurity?

Understanding subnet masks is important in cybersecurity because it helps identify:
- network segmentation
- local devices
- scan ranges
- firewall configuration
- lateral movement inside networks

## How to identify your subnet mask?

### Windows

Use the following command in Command Prompt:

```cmd
ipconfig
```

![Windows subnet-mask](images/subnet-mask%20WINDOWS%20screenshot.png)

Look for:
- IPv4 Address
- Subnet Mask
- Default Gateway

### Linux

Use the following command:

```bash
ip a
```

![Linux subnet-mask](images/subnet-mask%20LINUX%20screenshot.png)


Example: 

```bash
inet 192.168.0.15/24
```

'/24' means: 
255.255.255.0

