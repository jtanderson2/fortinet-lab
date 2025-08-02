# Fortinet Home Lab Setup

## Contents
- [Introduction](#introduction)
- [Lab Components](#lab-components)
  - [Hardware](#hardware)
  - [Virtual Machines](#virtual-machines)
- [Physical Topology](#physical-topology)
- [Logical Topology](#logical-topology)

## Introduction
This document outlines the home lab setup I use for learning, testing, and validating Fortinet products and network architectures. It's built with a focus on Fortinet SD-WAN, ZTNA and central management via FortiManager/FortiAnalyzer, but is flexible enough for broader security and networking scenarios.


## Lab Components

### Hardware
- **2 × FortiGate 60E**
  - Currently running FortiOS 7.4
- **1 × Dell PowerEdge T130**
  - Intel Xeon E3-1200 (Quad Core)
  - 64 GB RAM
  - ESXi 6.7 Hypervisor

### Virtual Machines

- **FortiManager** - Free trial license
- **FortiAnalyzer** - Free trial license
- **EMS Server** - Free Trial
- **VyOS Stream** - Virtual Router
- **Windows Server 2016** – Domain Controller + PKI
- **Windows Server 2016** – IIS Web Server
- **Windows 10** – Domain-joined workstation
- **Linux Mint VMs** – for traffic generation and testing

## Physical Topology

![](media/fortinet-lab-physical.png)

## Physical Topology

![](media/fortinet-lab-physical.png)

The internal switch on the FGT100 provides Layer 2 connectivity across all physical and virtual lab components, eliminating the need for a separate physical switch. This switch also connects to a non-Fortinet wireless access point, which bridges the lab environment to the home LAN and internet.

Combined with virtual networking on the ESXi host, this setup offers significant flexibility for modifying the logical topology as needed — ideal for experimenting with routing, segmentation, or SD-WAN scenarios.

The direct WAN-to-WAN connections between the two FortiGates are used for ad hoc scenarios, such as quickly spinning up IPsec VPNs.


## Logical Topology

![](media/fortinet-lab-logical.png)




