# Introduction to Computer Networks

## Introduction

Every time we browse a website, send a message on WhatsApp, stream a YouTube video, or access cloud services like AWS, thousands of computers communicate with each other within milliseconds. This communication is possible because of **Computer Networks**.

Computer Networks form the foundation of the Internet and are one of the most important subjects for Software Engineers, Backend Developers, DevOps Engineers, Cloud Engineers, and Site Reliability Engineers (SREs).

Today, we will learn:

- What is a Computer Network?
- Why Networks are Needed
- Components of a Network
- Types of Networks
- Network Topologies
- Network Architecture
- Network Devices
- Packet Switching vs Circuit Switching
- Bandwidth, Latency and Throughput
- Real-world Networking Examples

# What is a Computer Network?

A **Computer Network** is a group of two or more computers or devices connected together to communicate and share resources.

Resources include:

- Files
- Printers
- Internet
- Databases
- Applications
- Cloud Services

Example

```
Laptop

↓

Wi-Fi Router

↓

Internet

↓

Google Server

↓

Response
```

Whenever you open Google, your computer communicates with Google's servers through a computer network.

# Why Do We Need Computer Networks?

Networks allow devices to:

- Share information
- Access the Internet
- Communicate with other devices
- Share hardware resources
- Access cloud services
- Improve collaboration

Without networks:

- No Internet
- No Email
- No Video Calls
- No Cloud Computing
- No Online Banking

# Components of a Network

A network consists of:

- Sender
- Receiver
- Communication Medium
- Protocols
- Network Devices

Example

```
Laptop

↓

Wi-Fi

↓

Router

↓

Internet

↓

Server
```

# Types of Networks

## PAN (Personal Area Network)

Smallest network.

Examples:

- Bluetooth
- Smart Watch
- Wireless Earbuds

Range

```
1–10 meters
```

## LAN (Local Area Network)

Covers a small geographical area.

Examples:

- School
- Office
- Home Wi-Fi

Advantages

- Fast
- Secure
- Low Cost

## MAN (Metropolitan Area Network)

Covers an entire city.

Example

Internet provided across Bengaluru.

## WAN (Wide Area Network)

Largest type of network.

Examples

- Internet
- International Bank Networks

The Internet is the world's largest WAN.

# Network Topologies

A topology describes how devices are connected.

## Bus Topology

```
Computer ─ Computer ─ Computer
```

Advantages

- Low cost
- Easy to install

Disadvantages

- Single cable failure affects the network.

## Star Topology

```
      Switch

   /   |   \

 PC1 PC2 PC3
```

Most common topology today.

Advantages

- Easy maintenance
- Fast communication

## Ring Topology

```
PC → PC → PC → PC
↑             ↓
←─────────────
```

Data travels in a circular path.

## Mesh Topology

Every device connects to every other device.

Advantages

- High reliability

Disadvantages

- Expensive

Used in:

- Military
- Data Centers

## Tree Topology

Combination of Star and Bus.

Used in large organizations.

## Hybrid Topology

Combination of multiple topologies.

Used by modern enterprises.

# Network Architecture

## Client-Server

```
Client

↓

Server

↓

Database
```

Examples

- Gmail
- Amazon
- Instagram

Advantages

- Secure
- Centralized
- Easy management

## Peer-to-Peer (P2P)

```
Computer ↔ Computer
```

Every computer acts as both client and server.

Examples

- Torrent
- Local file sharing

# Network Devices

## Hub

- Works at Physical Layer
- Broadcasts data to every device
- No intelligence

## Switch

- Works at Data Link Layer
- Sends data only to the destination device
- Uses MAC addresses

More efficient than Hub.

## Router

- Connects different networks
- Uses IP addresses
- Connects LAN to the Internet

Every home Wi-Fi router performs this task.

## Bridge

Connects two LANs.

## Repeater

Regenerates weak network signals.

Used to increase transmission distance.

## Gateway

Connects networks using different protocols.

Acts as a translator.

## Modem

Converts digital signals into analog signals and vice versa.

Connects homes to Internet Service Providers (ISPs).

## Access Point

Provides wireless connectivity to devices.

# Packet Switching

Data is divided into small packets before transmission.

Example

```
Large File

↓

Packet 1

Packet 2

Packet 3

↓

Internet

↓

Destination

↓

Reassembled
```

Advantages

- Efficient
- Reliable
- Faster resource utilization

The Internet uses Packet Switching.

# Circuit Switching

A dedicated communication path is established before transmission.

Example

Traditional telephone calls.

Advantages

- Reliable connection

Disadvantages

- Wastes bandwidth

# Packet Switching vs Circuit Switching

| Packet Switching | Circuit Switching |
|------------------|-------------------|
| Internet | Telephone |
| Shared path | Dedicated path |
| Efficient | Less efficient |
| Faster resource usage | Reserved bandwidth |

# Bandwidth

Bandwidth is the maximum amount of data that can be transferred over a network in one second.

Example

```
100 Mbps
```

Higher bandwidth allows more data transfer.

# Throughput

Throughput is the actual amount of data successfully transferred.

Example

Bandwidth = 100 Mbps

Actual Speed = 80 Mbps

Throughput = 80 Mbps

# Latency

Latency is the delay between sending and receiving data.

Lower latency means faster communication.

Example

Online Gaming

- Low Latency = Better gameplay

Video Calls

- High Latency = Delay

# Real-World Example

When you open YouTube:

```
Laptop

↓

Wi-Fi Router

↓

ISP

↓

Internet

↓

Google Servers

↓

Video Data

↓

Laptop
```

Thousands of packets travel across the network before the video starts playing.

# Best Practices

- Prefer switches over hubs.
- Use secure Wi-Fi networks.
- Reduce network latency.
- Monitor bandwidth usage.
- Design scalable network architectures.
- Secure networks using firewalls and encryption.

# Summary

Today, you learned:

- What Computer Networks are.
- Why networks are important.
- Components of a network.
- Types of networks (PAN, LAN, MAN, WAN).
- Different network topologies.
- Client-Server and Peer-to-Peer architectures.
- Network devices and their functions.
- Packet Switching vs Circuit Switching.
- Bandwidth, Throughput, and Latency.
- Real-world network communication.

Computer Networks are the backbone of modern computing. Every website, cloud application, mobile app, and distributed system depends on networking to exchange data reliably and efficiently. Understanding networking fundamentals is essential for Backend Development, DevOps, Cloud Computing, and especially Site Reliability Engineering (SRE).