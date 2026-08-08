# Cloud Computing Basics

## Introduction

After learning Linux and Computer Networks, the next important topic is **Cloud Computing**. Modern applications are rarely hosted on a developer's personal computer. Instead, companies use cloud platforms to run applications, store data, manage databases, and scale systems based on demand.

Today, I will learn the fundamentals of cloud computing and understand how platforms such as **AWS, Azure, and Google Cloud** provide infrastructure and services over the Internet.

# What is Cloud Computing?

Cloud Computing means using computing resources over the Internet instead of owning and managing all the physical hardware ourselves.

These resources can include:

- Servers
- Storage
- Databases
- Networking
- Computing power
- Security services
- Monitoring
- AI/ML services

Instead of buying a physical server:

```text
Company
   ↓
Buys Server
   ↓
Installs Hardware
   ↓
Maintains Server
```

With cloud:

```text
Company
   ↓
Cloud Provider
   ↓
Virtual Server
   ↓
Application
```

# Why Do We Need Cloud Computing?

Traditional infrastructure requires companies to purchase and maintain physical servers.

Problems include:

- High hardware cost
- Maintenance
- Limited scalability
- Hardware failures
- Large upfront investment
- Difficult capacity planning

Cloud computing solves many of these problems by allowing companies to provision resources when they need them.

# Example

Imagine an e-commerce website.

During normal days:

```text
1000 users
```

During a festival sale:

```text
100,000 users
```

With traditional infrastructure, the company needs to purchase enough servers in advance.

With cloud computing, resources can be scaled based on demand.

```text
Normal Traffic
     ↓
Few Servers

High Traffic
     ↓
More Servers
```

# Cloud Service Providers

The major cloud providers are:

### AWS

Amazon Web Services.

### Microsoft Azure

Microsoft's cloud platform.

### Google Cloud

Google's cloud computing platform.

All three provide similar categories of services, although their names and implementations differ.

# Cloud Deployment Models

## Public Cloud

Infrastructure is provided by a cloud provider and shared among many customers.

Examples:

- AWS
- Azure
- Google Cloud

## Private Cloud

Cloud infrastructure is dedicated to one organization.

Common in organizations with strict security or compliance requirements.

## Hybrid Cloud

Combination of public and private cloud.

```text
Private Cloud
      ↕
Public Cloud
```

# Cloud Service Models

The three major service models are:

```text
IaaS
PaaS
SaaS
```

# IaaS

IaaS = **Infrastructure as a Service**

The provider gives you infrastructure such as:

- Virtual machines
- Storage
- Networking

You manage:

- Operating system
- Applications
- Runtime
- Configuration

Example:

```text
AWS EC2
```

Think:

> "Give me a server. I will manage the software."

# PaaS

PaaS = **Platform as a Service**

The cloud provider manages more of the infrastructure.

You mainly focus on your application.

Example:

```text
Application
    ↓
PaaS
    ↓
Cloud Infrastructure
```

Examples include:

- AWS Elastic Beanstalk
- Azure App Service
- Google App Engine

Think:

> "I want to deploy my application without managing the server."

# SaaS

SaaS = **Software as a Service**

You simply use the software.

Examples:

- Gmail
- Google Docs
- Microsoft 365
- Slack

You don't manage:

- Servers
- Operating systems
- Infrastructure

# IaaS vs PaaS vs SaaS

| Feature | IaaS | PaaS | SaaS |
|---|---|---|---|
| Servers | Provider | Provider | Provider |
| OS | User | Provider | Provider |
| Application | User | User | Provider |
| Infrastructure Management | More | Less | Very Little |
| Example | EC2 | App Engine | Gmail |

# Cloud Regions

A **Region** is a geographical area where a cloud provider has infrastructure.

Example:

```text
AWS Region
     ↓
Multiple Availability Zones
```

Companies choose regions based on:

- User location
- Latency
- Cost
- Compliance
- Availability

# Availability Zones

An Availability Zone (AZ) is an isolated location inside a cloud region.

Example:

```text
Region

├── Availability Zone 1
├── Availability Zone 2
└── Availability Zone 3
```

Using multiple Availability Zones improves availability.

If one AZ fails:

```text
AZ 1 ❌

AZ 2 ✅

AZ 3 ✅
```

The application can continue running.

# High Availability

High Availability means designing systems so that they continue working even when some components fail.

Example:

```text
Load Balancer
      ↓
 ┌────┼────┐
 ↓    ↓    ↓
Server Server Server
```

If one server fails, traffic can go to the others.

# Scalability

Scalability means the ability of a system to handle increasing workload.

There are two major types.

## Vertical Scaling

Increase the power of one server.

```text
2 CPU
 ↓
8 CPU
```

Also called:

> Scale Up

## Horizontal Scaling

Add more servers.

```text
1 Server
   ↓
3 Servers
   ↓
10 Servers
```

Also called:

> Scale Out

# Elasticity

Elasticity means automatically increasing or decreasing resources based on demand.

Example:

```text
Low Traffic
    ↓
2 Servers

High Traffic
    ↓
10 Servers

Traffic Drops
    ↓
2 Servers
```

This is extremely important in cloud environments because it prevents wasting resources.

# Cloud Storage

Cloud providers offer different types of storage.

## Object Storage

Stores files as objects.

Examples:

- Images
- Videos
- PDFs
- Backups

AWS example:

```text
S3
```

## Block Storage

Acts like a disk attached to a virtual machine.

AWS example:

```text
EBS
```

## File Storage

Provides shared file systems.

AWS example:

```text
EFS
```

# Compute

Cloud providers provide virtual computing resources.

AWS example:

```text
EC2
```

Instead of purchasing a physical server, you can create a virtual machine.

Example:

```text
EC2 Instance
     ↓
Linux
     ↓
Node.js
     ↓
Express
     ↓
Application
```

# Networking in Cloud

Cloud networking includes:

- Virtual Networks
- Subnets
- IP Addresses
- Route Tables
- Firewalls
- Load Balancers

AWS uses:

```text
VPC
```

VPC = **Virtual Private Cloud**

It provides an isolated network environment for your cloud resources.

# Security Groups

A security group acts like a virtual firewall for cloud resources.

Example:

```text
Allow TCP 22
Allow TCP 80
Allow TCP 443
```

This means:

- Port 22 → SSH
- Port 80 → HTTP
- Port 443 → HTTPS

# Identity and Access Management

Cloud platforms need to control who can access which resources.

AWS provides:

```text
IAM
```

IAM = **Identity and Access Management**

It manages:

- Users
- Roles
- Permissions
- Policies

Example:

```text
Developer
    ↓
IAM Role
    ↓
Read S3
```

The developer may be allowed to read files but not delete them.

# Monitoring

Cloud systems need continuous monitoring.

Things we monitor include:

- CPU
- Memory
- Network traffic
- Disk usage
- Request count
- Error rate
- Latency

AWS provides:

```text
CloudWatch
```

Monitoring is especially important for SREs.

# Cloud Cost

Cloud resources are generally paid based on usage.

This is called:

> Pay-as-you-go

For example:

```text
More resources used
        ↓
Higher cost
```

Therefore, cloud engineers need to consider both performance and cost.

# Shared Responsibility Model

Cloud security is shared between the cloud provider and the customer.

The provider generally manages:

```text
Physical Infrastructure
Hardware
Data Centers
```

The customer is responsible for things such as:

```text
Application
Data
Access Permissions
Configuration
```

The exact responsibility depends on the service being used.

# Example Cloud Architecture

A simple web application could look like:

```text
User
  ↓
DNS
  ↓
Load Balancer
  ↓
Application Servers
  ↓
Database
  ↓
Object Storage
```

Monitoring can observe the entire system:

```text
                Monitoring
                    ↓
User → Load Balancer → Servers → Database
                    ↓
                 Storage
```

# Cloud and SRE

Cloud computing is extremely important for SRE because modern SRE teams manage systems that run on cloud infrastructure.

An SRE may work with:

- Virtual machines
- Containers
- Load balancers
- Cloud networking
- Auto scaling
- Monitoring
- Logging
- IAM
- Storage
- Databases
- Disaster recovery

# Important Cloud Terms

| Term | Meaning |
|---|---|
| Cloud | Computing resources delivered over the Internet |
| Region | Geographic cloud location |
| Availability Zone | Isolated infrastructure location within a region |
| IaaS | Infrastructure as a Service |
| PaaS | Platform as a Service |
| SaaS | Software as a Service |
| Scalability | Ability to handle increased workload |
| Elasticity | Automatically adjust resources based on demand |
| High Availability | Ability to continue operating during failures |
| VPC | Isolated virtual network |
| IAM | Identity and access management |
| Object Storage | Storage for files/objects |
| Load Balancer | Distributes traffic across servers |

# What I Should Learn Next

After understanding cloud basics, the next step should be **AWS Fundamentals**.

Recommended order:

```text
Cloud Basics
     ↓
AWS Global Infrastructure
     ↓
IAM
     ↓
EC2
     ↓
S3
     ↓
VPC
     ↓
Security Groups
     ↓
RDS
     ↓
Load Balancer
     ↓
Auto Scaling
     ↓
CloudWatch
     ↓
AWS Project
```

# Summary

Today, I learned:

- What Cloud Computing is.
- Why organizations use cloud platforms.
- AWS, Azure, and Google Cloud.
- Public, Private, and Hybrid Cloud.
- IaaS, PaaS, and SaaS.
- Regions and Availability Zones.
- High Availability.
- Vertical and Horizontal Scaling.
- Elasticity.
- Cloud Storage.
- Cloud Compute.
- VPC and cloud networking.
- Security Groups.
- IAM.
- Cloud Monitoring.
- Pay-as-you-go pricing.
- Shared Responsibility Model.
- How cloud computing relates to SRE.

Cloud computing provides the infrastructure on which modern applications run. Understanding these fundamentals is essential before moving into AWS, Docker, Kubernetes, CI/CD, and advanced SRE concepts.