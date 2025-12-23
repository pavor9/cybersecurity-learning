#TryHackMe Learning Journey

Documenting my path from zero to cybersecurity analyst.

## Progress Summary
- **Days active:** 4
- **Rooms completed:** 4 (1 review session)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 1 - November 30th, 2025
**Room:** Offensive Security Intro

What I learned:
- Offensive security = attacking systems to find vulnerabilities (red team)
- Defensive security = defending systems and detecting attacks (blue team)
- dirb = directory brute-forcing tool, finds hidden directories on websites
- In tool output, lines starting with + show discovered results

**Key takeaway:** Security requires understanding both attack and defense perspectives

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 2 - December 1st, 2025
**Room:** Careers in Cyber

**What I learned:**
- Security Analyst: monitors systems and analyzes threats
- Security Engineer: builds and maintains security infrastructure
- Incident Responder: handles active security breaches
- Digital Forensics Examiner: investigates security incidents and collects evidence
- Malware Analyst: reverse engineers malicious software
- Penetration Tester: ethically hacks systems to find vulnerabilities
- Red Teamer: simulates real-world attacks to test defenses
- Defensive security areas: monitoring, detection, incident response, threat intelligence, vulnerability management
- SOC (Security Operations Centre): centralized team monitoring security 24/7
- SIEM systems: act as "defensive radar" collecting and analyzing security logs
- Linux commands: ls, cd, cat, la (list files including hidden)
- Windows commands: dir, dir /a (list all files including hidden)
- HTTP logs: records of web traffic useful for detecting attacks

**Created:** Anki cards for security roles and defensive concepts

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 3 - December 3rd, 2025
**Rooms:** What is Networking, Intro to LAN

**What I learned:**
- Network fundamentals: devices connected together to communicate
- IP addresses (like home addresses) vs MAC addresses (like serial numbers)
- Private addresses identify devices on local network, public addresses identify devices on internet
- Octet: group of 8 bits in an IP address
- ARP (Address Resolution Protocol): maps IP addresses to MAC addresses on local networks
- DHCP (Dynamic Host Configuration Protocol): automatically assigns IP addresses to devices
- DHCP process: Discover → Offer → Request → ACK
- Network topologies: bus, star, ring
- Router: connects different networks together
- Switch: connects devices within the same network
- Subnetting: dividing larger networks into smaller sub-networks
- Subnet mask: defines which part of IP is network vs host
- Default gateway: device that routes traffic to other networks
- ping command: tests connectivity using ICMP protocol

**Created:** 56 Anki flashcards covering networking concepts, protocols, and terminology

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 4 - December 5th, 2025
**Room:** Review of "What is Networking" and "Intro to LAN"

**What I learned:**
- Re-learned networking fundamentals for better retention
- Clarified ARP vs DHCP (was confusing them initially)
- ARP specifically maps IP addresses to MAC addresses
- DHCP process: Discover → Offer → Request → ACK
- Solidified understanding of network addressing and subnetting

**Progress:** Reviewed 56 Anki cards from Day 3, concepts clicking better on second pass

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 5 - December 9th, 2025
**Room:** OSI Model

**What I learned:**
- OSI Model: 7-layer framework for network communication (Application → Presentation → Session → Transport → Network → Data Link → Physical)
- Encapsulation: data wraps with headers as it moves down layers when sending
- Physical layer: transmits raw bits as electrical/light signals
- Data Link layer: handles MAC addresses and node-to-node transfer (NIC operates here)
- Network layer: handles IP addressing and routing between networks (routers operate here)
- Routing protocols: OSPF (link-state) and RIP (distance-vector)
- Transport layer: manages end-to-end communication
- TCP: reliable, connection-oriented (guarantees delivery, slower)
- UDP: fast, connectionless (no delivery guarantee, used for streaming/gaming)
- Session layer: establishes and manages connections between applications
- Presentation layer: translator for data formatting, encryption, compression
- Application layer: user-facing services (DNS, HTTP, FTP, email)
- DNS: translates domain names to IP addresses

**Key insight:** Data flows DOWN through encapsulation when sending, UP through de-encapsulation when receiving. Each layer adds/removes its own header.

**Created:** 32 Anki flashcards covering OSI model concepts, layers, and protocols

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 5 - December 10th, 2024
**Rooms:** OSI Model, Packets and Frames

**What I learned:**

**OSI Model:**
- 7-layer framework for network communication (Application → Presentation → Session → Transport → Network → Data Link → Physical)
- Encapsulation: data wraps with headers as it moves down layers when sending
- Each layer has specific function and protocols
- TCP/UDP operate at Transport layer, IP at Network layer
- Key insight: Data flows DOWN through encapsulation (sending), UP through de-encapsulation (receiving)

**Packets and Frames:**
- Packet = the data/information (like a letter)
- Frame = envelope that wraps packet for transmission (includes MAC addresses)
- TCP headers contain: source/destination ports, IPs, sequence numbers, acknowledgement, checksum, flags, TTL
- TCP three-way handshake: SYN (request connection) → SYN/ACK (acknowledge) → ACK (confirm) → data flows
- TCP = reliable, connection-oriented (file transfers, web browsing)
- UDP = fast, connectionless (gaming, streaming)
- TCP flags: SYN (start), ACK (acknowledge), FIN (finish), RST (reset/abort)
- Ports = numbered endpoints directing traffic to specific services (Port 80=HTTP, 443=HTTPS, 22=SSH)

**Key breakthrough:** Speed-running rooms (30-45 min each) with 85% understanding on first pass, then letting review/practice deepen comprehension over time. Less stress, more progress.

**Created:** 38 Anki flashcards (32 OSI + 6 Packets/Frames)

**Next:** Hands-on Wireshark practice to see packets/headers in action

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 6 - December 12th, 2025
**Focus:** Revisiting Network Fundamentals + Video Creation System

**What I did:**
- Went back to first completed room (Network Fundamentals) to create explanatory video
- Tested new workflow: TryHackMe notes → NotebookLM mindmap → voiceover recording
- Published first video explaining basic networking concepts

**Why go back:**
Creating videos revealed gaps in my understanding. Concepts I thought I knew became fuzzy when explaining out loud. Going back to fundamentals before continuing forward ensures solid foundation.

**Key concepts covered in video:**
- Networks vs Internet (devices connected vs global network)
- Public vs Private networks
- IP addresses (4 octets, logical addressing)
- MAC addresses (physical hardware addressing)
- Ping and ICMP protocol

**Video creation process established:**
- NotebookLM generates mindmap structure from notes
- Screen record + voiceover explanation
- Light editing for clarity
- Upload + publish

**New insight:** Teaching forces understanding. Can't fake comprehension on camera. The Feynman Technique in practice.

**Next:** Continue creating videos for completed rooms (Days 1-5) to establish complete coverage and workflow consistency before adding new material.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Day 8 - December 23rd, 2025
**Room:** Extending Your Network

**What I learned:**

**Port Forwarding:**
- Opens specific ports on router to allow external access to internal devices
- Router maps external port to internal device IP:port
- Essential for hosting services (web servers, game servers) on home network

**Firewalls:**
- Stateful: Inspects entire connection (understands context, tracks connection state)
- Stateless: Inspects individual packets independently (no context awareness)
- Stateful more secure but requires more resources

**VPN (Virtual Private Network):**
- Creates encrypted tunnel between devices over public internet
- Forms new private network
- Two main protocols:
  * PPTP: Easy setup, weak security (outdated)
  * IPSec: Difficult setup, strong encryption (preferred)

**VLAN (Virtual LAN):**
- Logically separates network into segments using routers/switches
- Improves security and management without physical separation
- Example: Guest network vs internal network on same hardware

**Network Simulator Key Insight:**
Watched complete packet journey from Computer1 to Computer3 across networks:
1. Routing decision (destination not local → send to gateway)
2. First ARP (Computer1 gets router MAC address)
3. Second ARP (Router gets Computer3 MAC address)
4. TCP handshake across network (SYN → SYN/ACK → ACK)
5. Data transmission with acknowledgement

Understanding: Communication between different networks requires:
- Router (gateway between networks)
- Multiple ARP requests (one per network hop)
- TCP connection maintained end-to-end despite routing

**Created:** 6 Anki flashcards covering network extension concepts

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
