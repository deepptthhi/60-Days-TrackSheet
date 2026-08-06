# Day 37 - Learning OSI Model, TCP/IP Model & TCP vs UDP

## What did I learn?

Today, I learned how data travels across a network using standardized communication models. After understanding the basics of computer networks yesterday, today's learning focused on the **OSI Model**, **TCP/IP Model**, and the protocols that make internet communication reliable and efficient.

The first concept I learned was the **OSI Model**. I understood that it is a seven-layer conceptual model used to standardize network communication. Each layer has a specific responsibility, from transmitting raw bits at the Physical Layer to providing services directly to users at the Application Layer. Learning the purpose of each layer helped me understand how network communication is organized and how problems can be identified more easily.

I then learned about the **TCP/IP Model**, which is the practical networking model used on the Internet. I understood that it consists of four layers—Application, Transport, Internet, and Network Access. Comparing it with the OSI Model helped me understand why the TCP/IP Model is widely used in real-world networking.

Another important concept I learned was **Data Encapsulation**. I understood that as data moves down the networking layers, additional information is added at each layer before transmission. On the receiving side, this process is reversed to recover the original data.

I also learned the basics of **IP Addresses**. I understood that every device connected to a network requires a unique IP address for communication. I briefly explored IPv4, IPv6, Public IPs, and Private IPs and understood their role in identifying devices on a network.

One of the most important topics I learned today was the difference between **TCP** and **UDP**. I learned that TCP provides reliable, connection-oriented communication with error checking and ordered delivery, making it suitable for applications like banking, email, and file transfers. On the other hand, UDP is connectionless and faster, making it ideal for online gaming, live streaming, video calls, and DNS.

I also learned about the **TCP Three-Way Handshake**, which establishes a reliable connection before data transfer begins. Understanding the sequence of SYN, SYN-ACK, and ACK helped me see how TCP ensures both devices are ready to communicate.

Towards the end of today's learning, I explored **DNS**, **HTTP**, and **HTTPS**. I understood that DNS converts domain names into IP addresses, while HTTP and HTTPS are protocols used for communication between web browsers and servers. I also learned that HTTPS provides encrypted communication using SSL/TLS, making it much more secure than HTTP.

Finally, I studied several **common networking port numbers** such as 22 (SSH), 53 (DNS), 80 (HTTP), and 443 (HTTPS). These ports allow different network services to communicate over the same device.

By the end of today's learning, I realized that the OSI Model, TCP/IP Model, and networking protocols provide the foundation for all internet communication. Understanding these concepts is essential for troubleshooting networks and building reliable backend, cloud, and distributed applications.

## What challenges did I face?

The biggest challenge today was remembering the responsibilities of all **seven OSI layers**. Initially, the layers seemed similar, but after relating each one to its specific role, they became easier to understand.

I also found it slightly confusing to differentiate between the **OSI Model** and the **TCP/IP Model**. After comparing their layers and understanding that the OSI Model is a reference model while TCP/IP is used in real-world networking, the difference became much clearer.

Another challenge was understanding when to use **TCP** and **UDP**. Real-world examples like file transfers for TCP and video streaming for UDP helped me understand their practical applications.

## What new concepts did I understand?

### OSI Model

I learned how the seven layers organize network communication and simplify troubleshooting.

### TCP/IP Model

I understood the four-layer networking model used on the Internet.

### Data Encapsulation

I learned how data is packaged and prepared before being transmitted across a network.

### IP Address

I understood that every network device requires a unique IP address for communication and its classes.

### TCP

I learned that TCP provides reliable and connection-oriented communication.

### UDP

I understood that UDP provides fast communication without guaranteeing delivery.

### TCP Three-Way Handshake

I learned how TCP establishes a reliable connection before transmitting data.

### DNS

I understood that DNS converts domain names into IP addresses.

### HTTP & HTTPS

I learned the difference between secure and non-secure web communication.

### Port Numbers

I understood how different network services use specific port numbers for communication.

## What computer/software engineering fundamentals did I learn today?

Today's learning helped me understand how communication between devices is standardized using networking models and protocols. I also realized that reliable software systems depend on protocols such as TCP, IP, DNS, and HTTPS to exchange information securely and efficiently.

Another important takeaway was understanding that network communication follows a layered architecture. This modular design makes systems easier to develop, troubleshoot, and maintain while allowing different technologies to work together.

## What changed in my thinking?

Before today, I thought network communication happened directly between devices without much structure.

After today's learning, I realized that every request passes through multiple networking layers, protocols, and communication mechanisms before reaching its destination. Understanding these layers gave me a much clearer picture of how the internet actually works.

The biggest realization for me today was that concepts like the OSI Model, TCP/IP, TCP, UDP, DNS, and HTTPS are not just theoretical—they form the foundation of every website, cloud service, and distributed application we use every day.

## Today's One Line Summary

> **"Today I learned how networking models and protocols such as the OSI Model, TCP/IP, TCP, UDP, DNS, and HTTPS work together to enable reliable and secure communication across the Internet."**