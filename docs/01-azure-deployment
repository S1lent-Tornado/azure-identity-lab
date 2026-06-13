# Azure Deployment Documentation

## Overview

This document outlines the deployment of the Azure infrastructure used for the Windows Server identity lab.

The goal of this deployment was to create a cloud-hosted environment capable of supporting:

- Active Directory Domain Services
- DNS
- DHCP
- Identity management
- User provisioning
- Windows Server administration practice

The environment was designed to simulate a small enterprise identity infrastructure.


---

# Azure Resource Planning

## Resource Group

A dedicated Azure Resource Group was created to organize and manage all resources associated with the lab environment.

Purpose:

- Resource organization
- Simplified management
- Ability to remove or recreate the environment
- Logical separation from other Azure resources


Configuration:

```text
Resource Group:
rg-test-1

Region:
East US

Availability Zone:
Zone 2
```

---

# Virtual Machine Deployment

A Windows Server virtual machine was deployed to act as the central identity server and future domain controller.


Configuration:

| Setting | Value |
|---|---|
| Operating System | Windows Server 2022 |
| Deployment Type | Azure Virtual Machine |
| vCPU | 2 |
| Memory | 16GB |
| Purpose | Domain Controller / Infrastructure Server |


The VM was sized to support:

- Active Directory services
- DNS
- DHCP
- Testing with domain clients
- Administrative tasks


---

# Network Configuration

## Static IP Address

A static private IP address was configured for the server.

Reason:

Domain Controllers require predictable network addressing because services such as:

- DNS
- Active Directory authentication
- Domain discovery

depend on consistent connectivity.


Example:

```text
Server Role:
Domain Controller

IP Assignment:
Static Private IP
```

---

# DNS Configuration

DNS was configured to point back to the local server.

Configuration:
```text
DNS Server:
127.0.0.1
```

Reason:

After promotion to Domain Controller, the server hosts Active Directory-integrated DNS.

The Domain Controller must be able to resolve domain services locally.


---

# Deployment Steps

The deployment process consisted of:


## 1. Create Azure Resources

Created:

- Resource Group
- Virtual Network
- Network Interface
- Virtual Machine


## 2. Configure Networking

Configured:

- Private IP addressing
- Network security settings
- DNS configuration


## 3. Install Windows Server Roles

After deployment, the following roles were installed:

- Active Directory Domain Services
- DNS Server
- DHCP Server
- IIS


## 4. Promote Server to Domain Controller

The server was promoted to a Domain Controller.

This created:

```text
Domain:

lab.local
```

The Domain Controller became responsible for:

- Authentication
- Directory services
- DNS resolution
- Identity management


---

# Current Infrastructure State

Current environment:

```text
Azure
|
|
Windows Server 2022
|
|
Domain Controller
|
|------ Active Directory
|
|------ DNS
|
|------ DHCP
|
|------ IIS
|
|
lab.local Domain
```
---

# Skills Practiced

This deployment provided experience with:

- Azure resource management
- Cloud VM deployment
- Windows Server administration
- Network configuration
- Domain Controller setup
- DNS dependency within Active Directory
- Infrastructure documentation


---

## Design Decisions

The Domain Controller was configured with a static private IP because Active Directory infrastructure relies on consistent addressing for authentication and DNS resolution.

DNS was configured locally because Active Directory uses DNS for service discovery.

---

# Future Improvements

Planned additions:

- Configure DHCP scopes
- Create Organizational Units
- Implement Group Policy
- Deploy domain-joined client machines
- Automate user creation with PowerShell
- Integrate Microsoft Entra ID
- Practice hybrid identity management
