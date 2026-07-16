# Networking Concepts

Networking is the process of connecting two or more devices so they can communicate and share data.

---

# 1. What is a Network?

## Purpose

A network allows multiple devices to communicate and share information.

## Real Life Example

Your home Wi-Fi connects your laptop, mobile phone, smart TV, and other devices.

```
Laptop
   \
    \
   Router ---- Internet
    /
   /
Mobile
```

## DevOps Example

A web server communicates with a database server over a network.

---

# 2. Types of Networks

## LAN (Local Area Network)

### Purpose

A network that covers a small geographical area such as a home, office, or school.

### Example

Office computers connected through a switch.

### Advantages

- High Speed
- Low Cost
- Easy to Manage

---

## MAN (Metropolitan Area Network)

### Purpose

A network that covers an entire city.

### Example

A bank connecting all its branches within Lucknow.

---

## WAN (Wide Area Network)

### Purpose

A network that covers large geographical areas.

### Example

The Internet.

---

## PAN (Personal Area Network)

### Purpose

A small network for personal devices.

### Example

Mobile phone connected to Bluetooth earbuds or smartwatch.

---

# 3. IP Address

## Purpose

An IP Address uniquely identifies a device on a network.

## Example

```
192.168.1.10
```

## Types

### IPv4

32-bit address

Example

```
192.168.1.20
```

### IPv6

128-bit address

Example

```
2401:4900:abcd::1
```

---

# 4. Public IP vs Private IP

## Public IP

Assigned by the Internet Service Provider (ISP).

Accessible over the Internet.

Example

```
49.36.xx.xx
```

## Private IP

Used inside local networks.

Examples

```
192.168.x.x

10.x.x.x

172.16.x.x - 172.31.x.x
```

---

# 5. Static IP vs Dynamic IP

## Static IP

A fixed IP address that does not change.

Commonly used for servers.

---

## Dynamic IP

Automatically assigned by DHCP.

Mostly used in home Wi-Fi networks.

---

# 6. MAC Address

## Purpose

A MAC Address uniquely identifies the network interface card (NIC) of a device.

Example

```
00:1A:2B:3C:4D:5E
```

Unlike an IP address, the MAC address is generally permanent.

---

# 7. Subnet Mask

## Purpose

A subnet mask separates the network portion and the host portion of an IP address.

Example

IP Address

```
192.168.1.20
```

Subnet Mask

```
255.255.255.0
```

Network

```
192.168.1
```

Host

```
20
```

---

# 8. Gateway

## Purpose

A gateway connects one network to another.

Usually, the router acts as the default gateway.

Example

```
Laptop
   ↓
Gateway (Router)
   ↓
Internet
```

Check Gateway

```bash
ip route
```

---

# Summary

| Concept | Description |
|----------|-------------|
| Network | Connects devices for communication |
| LAN | Small area network |
| MAN | City-wide network |
| WAN | Large area network |
| PAN | Personal device network |
| IP Address | Logical address of a device |
| MAC Address | Physical address of a network card |
| Subnet Mask | Divides network and host portions |
| Gateway | Connects different networks |

---

# Interview Questions

## Q1. What is the difference between an IP Address and a MAC Address?

| IP Address | MAC Address |
|------------|-------------|
| Logical Address | Physical Address |
| Can Change | Usually Permanent |

---

## Q2. Difference between LAN and WAN?

| LAN | WAN |
|------|------|
| Small Area | Large Area |
| Faster | Comparatively Slower |

---

## Q3. Which IP is used inside a home network?

Private IP

---

## Q4. Which device usually acts as the default gateway?

Router

---

## Useful Commands

Display IP Address

```bash
ip addr
```

Display Routing Table

```bash
ip route
```

Display MAC Address

```bash
ip link
```

---

---

# 9. DNS (Domain Name System)

## Purpose

DNS converts a domain name into an IP address.

## Example

Instead of remembering

```
142.250.183.78
```

you simply type

```
google.com
```

DNS finds the corresponding IP address.

## Real Life Example

A phone contact saves a person's name instead of remembering their phone number.

## Command

```bash
nslookup google.com
```

or

```bash
dig google.com
```

---

# 10. DHCP (Dynamic Host Configuration Protocol)

## Purpose

DHCP automatically assigns network configuration to devices.

It provides

- IP Address
- Subnet Mask
- Gateway
- DNS Server

## Example

When you connect your laptop to Wi-Fi, you do not manually enter an IP address.

The router automatically assigns one.

---

# 11. Ports

## Purpose

A port identifies a specific service running on a device.

One IP address can have many services.

Ports help distinguish them.

## Common Ports

| Port | Service |
|------|----------|
| 20/21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |
| 3306 | MySQL |
| 5432 | PostgreSQL |
| 6379 | Redis |
| 8080 | Tomcat |

## Commands

```bash
ss -tuln
```

```bash
netstat -tuln
```

---

# 12. TCP vs UDP

## TCP

Reliable protocol.

Guarantees data delivery.

Examples

- HTTP
- HTTPS
- SSH
- FTP

---

## UDP

Fast protocol.

Does not guarantee delivery.

Examples

- Video Streaming
- Gaming
- DNS
- VoIP

---

## Difference

| TCP | UDP |
|------|------|
| Reliable | Faster |
| Connection-Oriented | Connectionless |
| Error Checking | Minimal Error Checking |
| Slower | Faster |

---

# 13. OSI Model

OSI has seven layers.

| Layer | Name |
|--------|------|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |

## Mnemonic

All People Seem To Need Data Processing

---

# 14. TCP/IP Model

TCP/IP consists of four layers.

| Layer |
|--------|
| Application |
| Transport |
| Internet |
| Network Access |

---

# Difference between OSI and TCP/IP

| OSI | TCP/IP |
|------|---------|
| 7 Layers | 4 Layers |
| Reference Model | Practical Model |
| Mainly Educational | Used on the Internet |

---

# Useful Commands

Check IP Address

```bash
ip addr
```

Check Routing Table

```bash
ip route
```

Check Listening Ports

```bash
ss -tuln
```

DNS Lookup

```bash
nslookup google.com
```

Show Network Interfaces

```bash
ip link
```

---

# Summary

| Concept | Purpose |
|----------|----------|
| DNS | Converts domain names into IP addresses |
| DHCP | Automatically assigns IP addresses |
| Port | Identifies network services |
| TCP | Reliable communication |
| UDP | Fast communication |
| OSI | 7-layer networking model |
| TCP/IP | Practical networking model |

---

# Interview Questions

## Q1. What is DNS?

DNS converts a domain name into an IP address.

---

## Q2. What does DHCP provide?

- IP Address
- Gateway
- DNS
- Subnet Mask

---

## Q3. Which protocol is reliable?

TCP

---

## Q4. Which protocol is faster?

UDP

---

## Q5. Which protocol is used for video streaming?

UDP

---

## Q6. Which port is used by SSH?

22

---

## Q7. Which port is used by HTTPS?

443

---

## Q8. How many layers are there in the OSI Model?

7

---

## Q9. How many layers are there in the TCP/IP Model?

4