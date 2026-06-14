# Domain Controller Setup Documentation

## Overview

This document outlines the process of configuring a Windows Server 2022 virtual machine as an Active Directory Domain Controller.

The Domain Controller serves as the foundation of the identity infrastructure by providing centralized authentication, authorization, and directory management.

This configuration establishes the Active Directory environment used throughout this lab.

---

# Domain Controller Purpose

A Domain Controller (DC) is a Windows Server system responsible for managing authentication and identity within an Active Directory domain.

In an enterprise environment, Domain Controllers provide:

- User authentication
- Computer authentication
- Directory services
- Group management
- Access control
- Policy enforcement


For this lab, the Domain Controller provides the core identity services for:

lab.local


---

# Server Preparation

Before installing Active Directory Domain Services, the Windows Server VM was configured with the required network settings.

## Network Configuration

The Domain Controller was assigned:

```
Static Private IP Address
Static DNS:
127.0.0.1
```
Reason:

Active Directory relies heavily on DNS for:

- Domain discovery
- Authentication services
- Locating domain resources
- Service communication


---

# Installing Required Server Roles

The following Windows Server roles were installed:

| Role | Purpose |
|---|---|
| Active Directory Domain Services | Provides centralized identity management |
| DNS Server | Provides domain name resolution |
| DHCP Server | Provides IP address management |
| IIS | Web service testing and administration practice |


---

# Installing Active Directory Domain Services

Active Directory Domain Services (AD DS) was installed through Server Manager.

Installation process:
```
Server Manager
|
|
Add Roles and Features
|
|
Active Directory Domain Services
```

After installation, the server was promoted to a Domain Controller.

---

# Domain Controller Promotion

The server was promoted using the Active Directory Domain Services configuration wizard.
```
Configuration:
Deployment Type:
New Forest

Domain Nmae:
lab.local
```

This created a new Active Directory forest and domain.

---

# Active Directory Structure

After promotion, the server became responsible for maintaining the directory database.

The initial directory structure contains:

```
lab.local
|
|---Users
|
|---Computers
|
|---Domain Controllers
```
---

Future improvements:

- Organizational Units
- Security Groups
- Department-based structure
- Group Policy management

---

# Domain Controller Responsibilities

The Domain Controller now provides:

## Authentication

Verifies user identity when logging into the domain.

Example:
```
User Login
|
|
Domain Controller
|
|
Credential Validation
|
|
Access Granted
```


---

## Authorization

Determines what authenticated users are allowed to access.

Example:
```
User
|
|
Group Membership
|
|
Permissions
|
|
Resource Access
```


---

## Directory Management

Stores and manages:

- User accounts
- Computers
- Groups
- Security information
- Domain configuration


---

# User Provisioning

After Active Directory was configured, approximately 1,000 test user accounts were created.

Purpose:

Simulate an enterprise environment where administrators manage large numbers of identities.


Tasks performed:

- User account creation
- Identity organization
- Account management
- Directory administration


Future improvements:

- Automated provisioning with PowerShell
- Naming conventions
- Organizational Units
- Group assignments


---

# Verification

The Domain Controller configuration was verified through:

## Active Directory Users and Computers

Used to confirm:

- Domain creation
- User accounts
- Directory objects


## DNS Manager

Verified:

- Domain DNS records
- Server resolution


## Server Manager

Confirmed:

- Installed roles
- Server health


---

# Administrative Skills Practiced

This section represents skills commonly used in System Administrator and IAM roles.

## Windows Server Administration

- Installing server roles
- Configuring Domain Controllers
- Managing server services
- Maintaining infrastructure


## Identity Administration

- User provisioning
- Directory management
- Authentication concepts
- Access control fundamentals


## Infrastructure Troubleshooting

Practiced understanding of:

- DNS dependencies
- Domain connectivity
- Server networking
- Role configuration


---

# Future Improvements

Planned additions:

- Create Organizational Units (OUs)
- Implement Group Policy Objects (GPOs)
- Configure password policies
- Deploy domain-joined Windows clients
- Create security groups
- Implement role-based access control
- Integrate Microsoft Entra ID
- Practice hybrid identity management
