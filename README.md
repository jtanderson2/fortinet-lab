# Fortinet Home Lab Setup

## Contents
- [Introduction](#introduction)
- [Lab Components](#lab-components)
  - [Hardware](#hardware)
  - [Virtual Machines](#virtual-machines)

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
- **EMS Server** - coming soon!
- **VyOS Stream** - Virtual routing
- **Windows Server 2016** – Domain Controller + PKI
- **Windows Server 2016** – IIS Web Server
- **Windows 10** – Domain-joined workstation
- **Linux Mint VMs** – for traffic generation and testing

## Physical Topology

![](media/fortinet-lab-physical.png)


## Logical Topology

![](media/fortinet-lab-logical.png)




