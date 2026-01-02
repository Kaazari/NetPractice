# NetPractice

*This project has been created as part of the 42 curriculum by zdjitte.*

-----

## Description

NetPractice is a practical networking exercise designed to introduce students to fundamental TCP/IP addressing concepts. The project consists of 10 progressively challenging levels where you must configure small-scale networks to enable communication between devices.

Through hands-on practice with IP addresses, subnet masks, routing tables, and network topologies, NetPractice builds a solid foundation in network configuration without requiring any prior networking experience.

**Goal:** Successfully configure all 10 network levels by filling in missing IP addresses, subnet masks, and routing information to ensure proper communication between hosts, routers, and the Internet.

-----

## Instructions

### How to Run

1. **Launch the training interface:**
- Open `index.html` in a web browser
- Navigate through levels 1-10 using the interface
1. **Configure each level:**
- Fill in empty fields (IP addresses, subnet masks, routes)
- Click “Check again” to verify your configuration
- Fix any errors based on the feedback provided
- Click “Get my config” to download your solution once successful
1. **Export configurations:**
- Successfully complete all 10 levels
- Download each level’s configuration file (JSON format)
- Place all 10 files at the root of your repository

### Submission Requirements

- **10 configuration files** (level1.json through level10.json) must be present at the repository root
- Each file represents a successfully completed level
- Files are exported directly from the training interface

### Testing

- The training interface provides immediate feedback
- Green indicators show correct configurations
- Red indicators highlight errors with diagnostic messages
- Use the logs to debug routing and connectivity issues

-----

## Resources

### Networking Concepts Studied

This project covers fundamental networking concepts including:

- **TCP/IP Addressing:** Understanding IPv4 address structure and allocation
- **Subnet Masks:** Calculating network sizes and address ranges using CIDR notation
- **Subnetting:** Dividing networks into smaller subnetworks efficiently
- **Default Gateway:** Configuring routing paths for hosts to reach external networks
- **Routing Tables:** Understanding how routers forward packets based on destination addresses
- **Network Devices:**
  - **Switches:** Layer 2 devices that connect multiple devices in the same network
  - **Routers:** Layer 3 devices that connect different networks and route traffic
- **OSI Model:** Focus on Network Layer (Layer 3) operations
- **Private vs Public IP Addresses:** Understanding address space allocation

### Classic References

**Documentation:**

- [RFC 791 - Internet Protocol](https://tools.ietf.org/html/rfc791)
- [RFC 950 - Internet Standard Subnetting Procedure](https://tools.ietf.org/html/rfc950)
- [Cisco IP Addressing and Subnetting Guide](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)

**Tutorials & Learning Resources:**

- [Subnetting Mastery](https://subnetipv4.com/) - Interactive subnetting practice
- [Subnet Calculator](https://www.subnet-calculator.com/) - IP address and subnet calculation tool
- [Computer Networking: A Top-Down Approach](https://gaia.cs.umass.edu/kurose_ross/index.php) by Kurose & Ross

**Community Resources:**

- [42 NetPractice Guide by lpaube](https://github.com/lpaube/NetPractice) - Comprehensive visual guide
- [NetPractice Guide by caroldaniel](https://github.com/caroldaniel/42sp-cursus-netpractice) - Detailed walkthrough

### Use of AI

**AI was used for the following purposes:**

1. **Concept Clarification:**
- Understanding subnet mask calculations and CIDR notation
- Explaining the difference between switches and routers
- Clarifying routing table logic and next-hop selection
1. **Problem Solving Assistance:**
- Debugging network configuration errors
- Understanding error messages from the training interface
- Identifying network overlap and routing conflicts
1. **Learning Strategy:**
- Creating a systematic approach to solve progressively harder levels
- Developing quick calculation methods for subnet ranges
- Building a mental model of network hierarchy

**AI was NOT used for:**

- Directly solving level configurations
- Generating complete solutions without understanding
- Bypassing the learning process

The project was completed through hands-on practice, with AI serving as a learning aid to accelerate understanding of networking fundamentals.

-----

## Project Structure

```
netpractice/
├── index.html              # Training interface
├── level1.json             # Level 1 solution
├── level2.json             # Level 2 solution
├── level3.json             # Level 3 solution
├── level4.json             # Level 4 solution
├── level5.json             # Level 5 solution
├── level6.json             # Level 6 solution
├── level7.json             # Level 7 solution
├── level8.json             # Level 8 solution
├── level9.json             # Level 9 solution
├── level10.json            # Level 10 solution
└── README.md               # This file
```

-----

## Key Learnings

### Subnet Mask Quick Reference

|CIDR|Subnet Mask    |Block Size|Usable IPs|
|----|---------------|----------|----------|
|/30 |255.255.255.252|4         |2         |
|/29 |255.255.255.248|8         |6         |
|/28 |255.255.255.240|16        |14        |
|/27 |255.255.255.224|32        |30        |
|/26 |255.255.255.192|64        |62        |
|/25 |255.255.255.128|128       |126       |
|/24 |255.255.255.0  |256       |254       |

### Core Principles

1. **Same Cable/Switch = Same Network = Same Subnet Mask**
- Devices directly connected must share the same subnet
1. **Routing Logic**
- Hosts use default routes (`0.0.0.0/0`) to reach their gateway
- Routers use specific routes for known networks and default routes for everything else
- The next hop must always be in the same network as the sending interface
1. **Private vs Public IPs**
- Private ranges (10.x.x.x, 172.16-31.x.x, 192.168.x.x) cannot be routed over the Internet
- Use public IPs for any network that needs Internet connectivity
1. **Network Planning**
- Avoid overlapping subnets on the same router
- Reserve first IP (network address) and last IP (broadcast address) in each subnet
- Plan IP allocation to prevent conflicts and allow for future growth

-----

## Tips for Success

- Start with simple values (e.g., .1, .2, .3) when filling in IPs
- Use `/30` for point-to-point router connections (most efficient)
- Draw the network topology on paper before configuring
- Check logs carefully when configurations fail—they tell you exactly what’s wrong
- Practice subnet calculations until they become automatic

-----

## Author

**zdjitte** - 42 School

*Completed: January 2026*