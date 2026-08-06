# OSI Model, TCP/IP Model & TCP vs UDP

## Introduction

After learning the fundamentals of Computer Networks, the next step is understanding **how data travels from one computer to another**. To make communication organized and standardized, networking follows layered models. The two most important networking models are the **OSI Model** and the **TCP/IP Model**.

Today, i learnt:

- OSI Model
- TCP/IP Model
- Data Encapsulation
- IP Address Basics
- TCP vs UDP
- TCP Three-Way Handshake
- DNS Basics
- HTTP vs HTTPS
- Common Networking Ports

These topics are among the most frequently asked in **SRE, DevOps, Backend, and Cloud Engineering interviews**.

# What is the OSI Model?

OSI stands for **Open Systems Interconnection**.

It is a conceptual model that divides network communication into **7 layers**.

Purpose:

- Standardize network communication
- Simplify troubleshooting
- Allow devices from different manufacturers to communicate

## OSI Layers

```
7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data Link
1. Physical
```

## Layer 7 – Application

Provides network services directly to users.

Examples:

- HTTP
- HTTPS
- FTP
- SMTP
- DNS

Example:

Opening a website in a browser.

## Layer 6 – Presentation

Responsible for:

- Data formatting
- Encryption
- Compression

Example:

HTTPS encrypts data before transmission.

## Layer 5 – Session

Responsible for:

- Creating sessions
- Managing sessions
- Terminating sessions

Example:

Keeping a user logged into an application.

## Layer 4 – Transport

Responsible for:

- End-to-end communication
- Reliability
- Error recovery
- Flow control

Protocols:

- TCP
- UDP

## Layer 3 – Network

Responsible for:

- IP Addressing
- Routing
- Path Selection

Protocol:

- IP

Device:

- Router

## Layer 2 – Data Link

Responsible for:

- MAC Addresses
- Error Detection
- Frame Delivery

Device:

- Switch

## Layer 1 – Physical

Responsible for transmitting bits.

Examples:

- Ethernet cable
- Fiber cable
- Wireless signals

Device:

- Hub

# Mnemonic

Top to Bottom

```
All
People
Seem
To
Need
Data
Processing
```

Bottom to Top

```
Please
Do
Not
Throw
Sausage
Pizza
Away
```

# TCP/IP Model

The Internet actually uses the TCP/IP Model.

It has **4 layers**.

```
Application

↓

Transport

↓

Internet

↓

Network Access
```

## Comparison

| OSI | TCP/IP |
|------|---------|
| 7 Layers | 4 Layers |
| Reference Model | Practical Model |
| Theoretical | Used on Internet |

# Data Encapsulation

When sending data:

```
Application Data

↓

Segment

↓

Packet

↓

Frame

↓

Bits
```

Receiving follows the reverse process.

# IP Address

Every device connected to a network has an IP address.

Example

```
192.168.1.10
```

Types:

- Public IP
- Private IP
- IPv4
- IPv6

# TCP

TCP stands for **Transmission Control Protocol**.

Features:

- Reliable
- Connection-oriented
- Ordered delivery
- Error checking
- Retransmission

Examples:

- Banking
- Email
- File Transfer
- Web Browsing

# TCP Three-Way Handshake

Before communication begins, TCP establishes a connection.

```
Client

↓

SYN

↓

Server

↓

SYN + ACK

↓

Client

↓

ACK

↓

Connection Established
```

Purpose:

- Synchronize communication
- Confirm both devices are ready

# UDP

UDP stands for **User Datagram Protocol**.

Features:

- Fast
- Connectionless
- No error recovery
- No ordering guarantee

Examples:

- Live Streaming
- Video Calls
- Online Games
- DNS

# TCP vs UDP

| TCP | UDP |
|------|-----|
| Reliable | Faster |
| Connection-oriented | Connectionless |
| Ordered | Unordered |
| Error recovery | No recovery |
| Higher overhead | Lower overhead |

# DNS Basics

DNS stands for **Domain Name System**.

Purpose:

Convert domain names into IP addresses.

Example

```
google.com

↓

142.x.x.x
```

Without DNS, users would need to remember IP addresses instead of website names.

# HTTP

HTTP stands for **HyperText Transfer Protocol**.

Characteristics:

- Not encrypted
- Port 80
- Faster
- Less secure

# HTTPS

HTTPS stands for **HyperText Transfer Protocol Secure**.

Characteristics:

- Encrypted
- Uses SSL/TLS
- Port 443
- Secure communication

# HTTP vs HTTPS

| HTTP | HTTPS |
|------|--------|
| Not Secure | Secure |
| Port 80 | Port 443 |
| No Encryption | Encryption |
| Faster | Slightly slower |

# Common Port Numbers

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
| 27017 | MongoDB |

# Real-World Example

Opening **https://www.google.com**

```
Browser

↓

DNS converts google.com to IP

↓

TCP Handshake

↓

HTTPS Request

↓

Router forwards packets

↓

Google Server

↓

Response

↓

Browser displays webpage
```

# Best Practices

- Use HTTPS instead of HTTP.
- Prefer TCP when reliability is important.
- Use UDP for real-time communication.
- Understand the OSI layers for troubleshooting.
- Remember common port numbers for interviews.



# Understanding these concepts is essential for troubleshooting network issues, designing scalable backend systems, and succeeding in Backend, DevOps, Cloud, and SRE interviews.