# Azure Identity & Windows Server Administration Lab

## Overview

This project documents the design, deployment, and administration of a cloud-based Windows Server identity infrastructure environment built in Microsoft Azure.

The purpose of this lab is to gain hands-on experience with core responsibilities commonly performed in System Administration, Identity and Access Management (IAM), and Infrastructure roles.

This environment simulates a small enterprise network by deploying and configuring Windows Server services responsible for identity management, authentication, networking, and user administration.

The lab focuses on practical experience with:

- Active Directory Domain Services (AD DS)
- Domain Controller administration
- DNS administration
- DHCP configuration
- User provisioning and lifecycle management
- Identity and access management concepts
- Windows Server role deployment
- PowerShell automation
- Infrastructure documentation
- Enterprise administration workflows


---

# Objectives

The goals of this lab are to develop practical experience with:

- Deploying Windows Server infrastructure in Microsoft Azure
- Creating and managing an Active Directory domain environment
- Understanding Domain Controller responsibilities
- Managing users, groups, and permissions
- Implementing organizational structure through Active Directory
- Automating administrative tasks
- Troubleshooting identity and network-related issues
- Practicing enterprise administration procedures


---

# Environment Overview

## Cloud Platform

Microsoft Azure

## Operating System

Windows Server 2022

## Region

East US

## Infrastructure Configuration

| Component | Configuration |
|---|---|
| Compute | Azure Virtual Machine |
| CPU | 2 vCPU |
| Memory | 16 GB RAM |
| Networking | Static Private IP Address |
| DNS | Domain Controller hosted DNS |
| Domain Services | Active Directory Domain Services |
| DHCP | Installed and configured |
| Web Services | IIS Installed |


---

# Architecture

The current environment consists of:

                Microsoft Azure

                      |
                      |

          Windows Server 2022 VM

                      |
    ---------------------------------

    Active Directory Domain Services
                  |
                  |
    -----------------------------
    |             |             |
    DNS          DHCP          IIS
                  |

           lab.local Domain

                  |

      Users / Groups / Computers
    
---

# Implemented Components

## Active Directory Domain Services

Configured Windows Server as a Domain Controller.

Implemented:

- Active Directory installation
- Domain promotion
- Domain creation
- User account management
- Identity organization


Active Directory provides the centralized identity platform used for:

- Authentication
- Authorization
- Resource access control
- User lifecycle management


---

## User Provisioning & Identity Management

Created approximately 1,000 Active Directory user accounts to simulate an enterprise environment.

Practiced:

- User account creation
- Account naming conventions
- Identity organization
- User lifecycle workflows
- Administrative management


Future improvements:

- Automated user creation through PowerShell
- Organizational Unit structure
- Security groups
- Role-based access control


---

## DNS Administration

Configured DNS services through Active Directory.

Practiced:

- DNS role installation
- Domain name resolution
- Understanding DNS dependency within Active Directory
- Domain Controller DNS configuration


DNS is critical within Active Directory environments because it enables:

- Domain discovery
- Authentication services
- Service location


---

## DHCP Administration

Installed and configured DHCP services.

Practiced:

- IP address management
- Network configuration concepts
- Client connectivity workflows


Future improvements:

- DHCP scopes
- Reservations
- Lease management
- Client testing


---

# Skills Demonstrated

## System Administration

- Windows Server deployment
- Server role installation
- Domain Controller administration
- User and group management
- Infrastructure troubleshooting
- Network service administration


## Identity & Access Management

- Identity lifecycle management
- Account provisioning
- Authentication concepts
- Access control fundamentals
- Directory services administration
- Enterprise identity architecture


## Automation

Planned implementation:

- PowerShell administration scripts
- Bulk user provisioning
- Configuration automation
- Reusable deployment workflows


---

# Planned Enhancements

This lab is actively being expanded.

Future additions include:

## Active Directory Improvements

- Organizational Unit design
- Group Policy Objects (GPO)
- Password policies
- Account lockout policies
- Security group management


## Client Administration

- Deploy Windows client VM
- Join clients to domain
- Test domain authentication
- Apply GPO policies


## Identity Expansion

- Microsoft Entra ID integration
- Hybrid identity configuration
- Conditional Access concepts
- MFA implementation


## Enterprise Administration

- File server implementation
- Shared folder permissions
- Role-based access control
- Monitoring and logging


---

# Documentation

Additional documentation includes:

- Deployment steps
- Configuration notes
- Troubleshooting documentation
- Architecture diagrams
- Administrative procedures


---

# Purpose

This project was created as a hands-on learning environment to build practical experience aligned with:

- Junior System Administrator roles
- Identity and Access Management roles
- Windows Server administration
- Cloud infrastructure support


The focus of this lab is developing practical skills through building, configuring, troubleshooting, and documenting enterprise-style infrastructure.
