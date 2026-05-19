# DHCP

## What is DHCP?

DHCP (Dynamic Host Configuration Protocol) is a network protocol responsible for automatically assigning IP addresses and network configuration information to device connected to a network.

Instead of manually configuring IP addresses, DHCP dynamically provides:

- IP address
- Subnet mask
- Default gateway
- DNS server

This simplifies network administration and reduces configuration errors.

## Why DHCP is important?

DHCP is essential in modern networks because it automates IP address assigment and centralizes network configuration management.

Without DHCP, administrator would need to manually configure every device on the network.

## DHCP Communication Ports

| Protocol | Port | Function |
|---|---|---|
| UDP | 67 | DHCP Server |
| UDP | 68 | DHCP Client |

## DHCP DORA Process

### DHCPDISCOVER

The client sends a broadcast message searching for available DHCP servers on the network.

### DHCPOFFER

The DHCP server responds by offering an available IP address and network configuration information.

### DHCPREQUEST

The client requests to use the offered IP address.

### DHCPACK

The DHCP server confirms the assigment and finalizes the configuration process.

## DHCP DORA Process Flow

Client -> DHCPDISCOVER

Server -> DHCPOFFER

Client -> DHCPREQUEST

Server -> DHCPACK

# Practical Analysis with Wireshark

### Starting packet capture

Wireshark was used to capture DHCP traffic during IP address renewal.

## Used Commands

### Linux

```bash
sudo dhclient -r
sudo dhclient
```

### Windows

```cmd
ipconfig /release
ipconfig /renew
```

## Wireshark filter

```text
dhcp
```

### DHCP DORA capture

![DORA capture](images/dora%20LINUX%20screenshot.png)


The capture above demonstrates the DHCP DORA process during IP address assignment.

- DHCP Discover:
  The client broadcasts a request searching for a DHCP server.

- DHCP Offer:
  The DHCP server offers an available IP address and network configuration.

- DHCP Request
  The client requests to use the offered IP address.

- DHCP ACK:
  The server confirms the lease and assigns the configuration to the client.

  The destination address 255.255.255.255 indicates a broadcast message sent to all devices on the local network because the client still does not have a valid IP address during the initial negotiation process.


### DHCP lease explanation

![Assigned IP](images/ip%20a%20dhcp%20LINUX%20screenshot.png)


After the DHCP ACK message, the IP address was successfully assigned to the network interface.

The 'ip a' command confirms that the interface received the IPv4 address:

```bash
10.0.2.15/24
```

### Used Commands

The following commands were used to release and renew the DHCP lease in Linux:

```bash
sudo dhclient -r
sudo dhclient
```

