## Table of Contents 
- [Project Overview](#project-overview) 
- [Objectives](#objectives) 
- [Requirements](#requirements) 
- [Planning](#planning) 
- [Design](#design) 
- [Implementation](#implementation) 
- [Testing](#testing) 
- [Troubleshooting & Lessons Learned](#troubleshooting--lessons-learned) 
- [Conclusion](#conclusion) 
- [References](#references)
## Project Overview:

Design and implement a secure, segmented network for GreenTech Solutions, a small environmental consulting company with 30 employees in a single, two floor building . The company requires a secure, reliable, and easily manageable network to support daily business operations, departmental collaboration, and guest access. This project involves designing and implementing a segmented, scalable network  in Cisco Packet Tracer, focusing on best practices for security and documentation. 

## Objectives:
- Build hands-on networking skills with VLANs, inter-VLAN routing, DHCP, NAT, and ACLs
- Provide reliable  wired and wireless connectivity for all users and devices
- Ensure network segmentation for security and performance
- Isolate guest users from internal resources
- Document the process for portfolio and interview preparation
- Practice troubleshooting and validation of network configurations

## Requirements 

### Functional 
- Wired and wireless access for all employees and authorized devices
- VLAN segmentation by department: Administration, Engineering, Sales & Marketing, Guests
- Guest Wi-Fi with internet-only access, no internal resource visibility 
- Shared printer and file server accessible to staff but not guests
- Internet access for all users

### Non-Functional
- Scalable and simple star topology
- Use of industry-standard security practices (segmentation, ACLs, strong passwords)
- Comprehensive documentation for handover and audit purposes
- Easy management and troubleshooting

### Constraints
- **Budget**: Limited; must use existing hardware where possible
- **IT Staff**: Only one dedicated IT administrator
- **Expansion**: Network should support up to 20% growth in users/devices
- **Compliance:** Must follow basic data privacy and security best practices
- **Downtime:** Minimal downtime allowed during business hours
- **Guest Policy:** Guests may only access the internet, not internal resources

## Planning

### Company Profile
- **Name:** GreenTech Solutions
- **Industry:** Environmental Consulting
- **Location:** Single building, two floors
- **Employees:** 30
- **Departments:** Administration, Engineering, Sales & Marketing, Guest/Visitors
	- Administration (6 users)
	- Engineering (12 users)
	- Sales & Marketing (8 users)
	- Guest/Visitors (Wi-Fi/ 4 Devices)
### Project Scope
- Design a star topology with central switches and router
- Assign VLANs and subnets for each department and guest network
- Configure inter-VLAN routing, DHCP, NAT, and ACLs
- Set up wireless access with separate SSIDs for employees and guests
- Ensure shared printer and file server are accessible only to internal staff
- Document all steps, configurations, and decisions

## Design

### Subnet/VLAN Table
| VLAN ID | Department        | Subnet          | Devices/Users            | Switch Location |
| ------- | ----------------- | --------------- | ------------------------ | --------------- |
| 10      | Administration    | 192.168.10.0/24 | 6 PCs                    | Floor 1 (S1)    |
| 20      | Engineering       | 192.168.20.0/24 | 12 PCs                   | Floor 1 (S1)    |
| 30      | Sales & Marketing | 192.168.30.0/24 | 8 PCs                    | Floor 2 (S2)    |
| 40      | Guest Wi-Fi       | 192.168.40.0/24 | 4 Devices                | Wireless (AP)   |
| 50      | Servers/Printers  | 192.168.50.0/24 | 1 Printer, 1 File Server | Floor 1 (S1)    |
**Gateway IPs:**
- VLAN 10: 192.168.10.1
- VLAN 20: 192.168.20.1
- VLAN 30: 192.168.30.1
- VLAN 40: 192.168.40.1
- VLAN 50: 192.168.50.1
### Network Diagram

![brave_screenshot_drive.google.com](../Networking%20and%20Security/Images/brave_screenshot_drive.google.com.png)
## Implementation
