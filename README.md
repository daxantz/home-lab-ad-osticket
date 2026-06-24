

# Home Lab: Active Directory + osTicket Help Desk Simulation

## Overview
Built a virtualized IT environment simulating a small business network. The lab includes a Windows Server 2019 domain controller, a Windows 10 client machine, and an Ubuntu Server running osTicket as a help desk ticketing system.

## Technologies Used
- Windows Server 2019 (Domain Controller)
- Active Directory Domain Services
- DNS & DHCP
- Group Policy (GPO)
- Windows 10 Client VM
- Ubuntu Server 22.04
- Apache, MySQL, PHP (LAMP Stack)
- osTicket v1.18.1
- Oracle VirtualBox

## Network Architecture
- Domain: mydomain.com
- DC/DNS/DHCP Server: Windows Server 2019
- Client Machine: Windows 10 joined to mydomain.com
- Web/Ticket Server: Ubuntu Server running osTicket

## Active Directory Configuration
- Created OUs: _USERS, _ADMINS, _IT, _HR, _COMPUTERS
- Created Security Groups: IT-Support, HR-Staff
- Created domain users: jsmith (IT-Support), sjones (HR-Staff)
- Applied GPO (IT-Password-Policy) to _IT OU enforcing 12 character minimum password length, complexity requirements, and 90 day expiration

## osTicket Setup
- Deployed osTicket on Ubuntu Server via LAMP stack
- Configured MySQL database for osTicket
- Created agent accounts to simulate help desk staff
- Created departments: IT Support
- Simulated end to end ticket workflow

## Ticket Workflow
1. End user submits ticket through client portal reporting inability to log into domain account
2. Agent receives ticket in SCP dashboard and assigns priority
3. Agent adds internal note documenting troubleshooting steps
4. Agent resets user password in Active Directory
5. Ticket closed with resolution summary sent to user

## Skills Demonstrated
- Active Directory user and group management
- Organizational Unit design
- Group Policy creation and linking
- Linux server administration
- LAMP stack deployment
- Help desk ticketing workflow
- VirtualBox network configuration
- SSH remote access
