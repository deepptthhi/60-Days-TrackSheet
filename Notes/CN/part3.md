# DNS, DHCP, NAT, Firewalls & Network Troubleshooting

## Introduction

After learning about the OSI Model, TCP/IP Model, TCP, UDP, HTTP, and HTTPS, today's focus is on the services that make the Internet work behind the scenes. Every time you open a website, connect to Wi-Fi, or troubleshoot a network issue, technologies like **DNS**, **DHCP**, and **NAT** are involved.

Today, I will learn:

- DNS
- DHCP
- NAT
- ARP
- ICMP
- Firewalls
- Proxy vs Reverse Proxy
- Load Balancer
- Linux Networking Commands
- Basic Network Troubleshooting

These concepts are frequently asked in **Backend, DevOps, Cloud, Linux, and SRE interviews**.

# What is DNS?

DNS stands for **Domain Name System**.

It is known as the **Phonebook of the Internet**.

Instead of remembering IP addresses, users type domain names.

Example

```
google.com

↓

DNS

↓

142.x.x.x

↓

Google Server
```

Without DNS, users would have to remember IP addresses for every website.

## DNS Resolution Process

```
Browser

↓

DNS Resolver

↓

Root Server

↓

TLD Server

↓

Authoritative Server

↓

IP Address Returned

↓

Browser Connects to Server
```

# What is DHCP?

DHCP stands for **Dynamic Host Configuration Protocol**.

Its job is to automatically assign IP addresses to devices.

Without DHCP:

- IP addresses must be configured manually.

With DHCP:

- IP Address
- Subnet Mask
- Gateway
- DNS Server

are assigned automatically.

Example

```
Laptop joins Wi-Fi

↓

Router (DHCP)

↓

IP Assigned

↓

Internet Access
```

# What is NAT?

NAT stands for **Network Address Translation**.

It allows multiple private devices to share one public IP address.

Example

```
Phone

Laptop

TV

↓

Wi-Fi Router

↓

Single Public IP

↓

Internet
```

Advantages

- Saves IPv4 addresses
- Improves security
- Hides internal network

# Public vs Private IP

## Public IP

- Visible on the Internet
- Assigned by ISP
- Globally unique

Example

```
49.205.x.x
```

## Private IP

Used inside local networks.

Common ranges

```
10.0.0.0/8

172.16.0.0 – 172.31.255.255

192.168.0.0/16
```

# What is ARP?

ARP stands for **Address Resolution Protocol**.

Purpose:

Convert an IP Address into a MAC Address.

Example

```
192.168.1.20

↓

ARP

↓

00:1A:2B:3C:4D:5E
```

# What is ICMP?

ICMP stands for **Internet Control Message Protocol**.

Used for:

- Network diagnostics
- Error reporting

Examples

- ping
- traceroute

# Firewalls

A Firewall monitors incoming and outgoing network traffic.

It allows or blocks connections based on predefined rules.

Example

```
Internet

↓

Firewall

↓

Allowed Traffic

↓

Server
```

Types

- Hardware Firewall
- Software Firewall

# Proxy Server

A Proxy Server sits between the client and the Internet.

```
Client

↓

Proxy

↓

Internet
```

Uses

- Hide client IP
- Content filtering
- Caching

# Reverse Proxy

A Reverse Proxy sits in front of backend servers.

```
Client

↓

Reverse Proxy

↓

Backend Server
```

Uses

- Load balancing
- SSL termination
- Security
- Caching

Example

- Nginx
- HAProxy

# Load Balancer

A Load Balancer distributes traffic across multiple servers.

```
Users

↓

Load Balancer

↓

Server 1

Server 2

Server 3
```

Advantages

- High Availability
- Scalability
- Better Performance

Common Algorithms

- Round Robin
- Least Connections
- IP Hash

# Linux Networking Commands

## ping

Checks connectivity.

```bash
ping google.com
```

## traceroute

Shows packet path.

```bash
traceroute google.com
```

## nslookup

Finds DNS information.

```bash
nslookup google.com
```

## dig

Detailed DNS lookup.

```bash
dig google.com
```

## ip addr

Displays IP addresses.

```bash
ip addr
```

## ss

Shows active sockets.

```bash
ss -tuln
```

## netstat

Displays network connections.

```bash
netstat -tuln
```

## curl

Sends HTTP requests.

```bash
curl https://google.com
```

## wget

Downloads files.

```bash
wget https://example.com/file.zip
```

# Basic Network Troubleshooting

Suppose a website is not opening.

Check in this order:

```
1. Internet Connection

↓

2. IP Address

↓

3. DNS Resolution

↓

4. Ping Server

↓

5. Firewall

↓

6. Web Server

↓

7. Application Logs
```

# What Happens When You Open a Website?

Example:

```
https://www.google.com
```

```
Browser

↓

DNS resolves google.com

↓

DHCP already assigned IP

↓

TCP Connection

↓

HTTPS Request

↓

Router uses NAT

↓

Internet

↓

Google Server

↓

Response

↓

Browser Displays Website
```

# Best Practices

- Use HTTPS instead of HTTP.
- Keep firewalls properly configured.
- Monitor DNS health.
- Use load balancers for high availability.
- Avoid exposing private IP addresses.
- Use Linux networking tools for troubleshooting.

# Common Interview Questions

1. What is DNS?
2. What is DHCP?
3. Why do we need NAT?
4. Difference between Public and Private IP?
5. What is ARP?
6. What is ICMP?
7. Difference between Proxy and Reverse Proxy?
8. What is a Load Balancer?
9. How does ping work?
10. How would you troubleshoot if a website is not accessible?

# Summary

Today, I learned:

- DNS and how domain names are resolved.
- DHCP and automatic IP assignment.
- NAT and IP address translation.
- Public vs Private IP addresses.
- ARP and MAC address resolution.
- ICMP and network diagnostics.
- Firewalls and network security.
- Proxy and Reverse Proxy.
- Load Balancers.
- Essential Linux networking commands.
- Basic network troubleshooting techniques.

These concepts are essential for understanding how modern networks operate and are widely used in Backend Development, DevOps, Cloud Computing, Linux Administration, and Site Reliability Engineering (SRE).