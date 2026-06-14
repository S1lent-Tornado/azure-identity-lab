# Active Directory Management Documentation

## Overview

This document covers the administration and management of the Active Directory environment created in this lab.

After deploying the Domain Controller, Active Directory was used as the centralized identity platform for managing users, computers, groups, and access control.

This portion of the lab focuses on practical identity administration tasks commonly performed in System Administration and Identity & Access Management (IAM) roles.

---

# Active Directory Environment

The Active Directory domain created in this lab:

```text
Domain:
lab.local
```

The Domain Controller provides centralized management for:

- User accounts
- Security groups
- Computer accounts
- Authentication
- Authorization
- Directory objects


---

# Active Directory Components

Active Directory organizes resources into objects.

The main object types used in this lab include:

| Object | Purpose |
|---|---|
| Users | Represents individual identities |
| Groups | Provides permission management |
| Computers | Represents domain-connected devices |
| Organizational Units | Provides logical organization |


---

# Active Directory Users

User accounts represent identities that can authenticate to the domain.

User accounts are used for:

- Logging into domain-connected systems
- Accessing resources
- Receiving policies
- Assigning permissions


---

# User Provisioning

Approximately 1,000 test user accounts were created to simulate an enterprise environment.

The purpose of creating a large user base was to practice:

- Identity creation
- Account management
- Directory administration
- Enterprise-scale provisioning


Example structure:

```text
lab.local

Users

 |
 |--- User001
 |
 |--- User002
 |
 |--- User003
 |
 ...
 |
 |--- User1000
```

---

# Identity Lifecycle Management

Managing user identities throughout their lifecycle is a core IAM responsibility.

The lifecycle includes:

```
Create
  |
  |
Modify
  |
  |
Manage Access
  |
  |
Disable / Remove
```

This lab currently focuses on:

- Identity creation
- Account organization
- User administration


Future improvements:

- Account expiration
- Offboarding workflows
- Automated provisioning
- Access reviews


---

# Security Groups

Security groups are used to simplify permission management.

Instead of assigning permissions to individual users:

```
User
 |
 |
Group Membership
 |
 |
Permissions
```

Administrators can manage access through group membership.

Future implementations:

- Department groups
- Role-based access groups
- Resource access groups


Example:

```text
IT-Admins

Members:
User001
User002

Permissions:
Administrative Access
```

---

# Organizational Units (OUs)

Organizational Units provide logical organization inside Active Directory.

Future OU structure:

```text
lab.local

|
|--- Users
|      |
|      |--- IT
|      |--- HR
|      |--- Finance
|
|--- Computers
|
|--- Groups
```

OUs allow administrators to:

- Apply Group Policies
- Delegate permissions
- Organize resources


---

# Computer Management

Domain-connected computers are represented as computer objects.

Computer objects allow administrators to manage:

- Authentication
- Policies
- Device configuration


Future additions:

- Deploy Windows client VM
- Join client to domain
- Apply Group Policies


---

# Authentication Flow

When a user signs into a domain-connected machine:

```text
User Login Request

        |

Domain Controller

        |

Credential Verification

        |

Active Directory Lookup

        |

Access Granted / Denied
```

The Domain Controller verifies identity before allowing access.


---

# Authorization Flow

Authentication confirms identity.

Authorization determines access.

Example:

```text
User

 |

Group Membership

 |

Assigned Permissions

 |

Resource Access
```

This separation is a core concept in IAM.


---

# Administration Tools Used

## Active Directory Users and Computers

Used for managing:

- Users
- Groups
- Computers
- Organizational Units


## Server Manager

Used for:

- Role management
- Server administration
- Monitoring


---

# Administrative Skills Practiced

## System Administration

- Active Directory management
- User administration
- Domain management
- Directory organization


## Identity & Access Management

- User provisioning
- Identity lifecycle concepts
- Access control
- Authentication and authorization


## Enterprise Administration

- Managing large user environments
- Directory structure planning
- Preparing for policy deployment


---

# Future Improvements

Planned additions:

- Create OU hierarchy
- Implement Group Policy Objects
- Configure password policies
- Create security groups
- Automate user creation with PowerShell
- Deploy domain-joined clients
- Implement role-based access control
- Integrate Microsoft Entra ID
