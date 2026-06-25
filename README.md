# Network Traffic Analysis using Wireshark

## Overview
This project demonstrates basic network traffic analysis using Wireshark in a lab environment. The objective was to capture and inspect common network protocols such as DNS, ICMP, TCP, and HTTPS/TLS in order to understand packet flow, IP addressing, port usage, and troubleshooting patterns.

## Objectives
- Capture live network traffic from a local machine
- Analyze DNS queries and responses
- Observe ICMP echo request/reply traffic using ping
- Identify the TCP 3-way handshake
- Inspect HTTPS/TLS traffic and port usage
- Understand packet-level details such as source/destination IP addresses, ports, and protocol behavior

## Tools Used
- Wireshark
- macOS / terminal
- Ping
- Web browser

## Protocols Analyzed
- DNS
- ICMP
- TCP
- HTTPS/TLS

## Lab Workflow
1. Started packet capture on the active network interface in Wireshark.
2. Generated ICMP traffic using the `ping` command.
3. Opened websites in the browser to generate DNS, TCP, and HTTPS traffic.
4. Applied protocol-specific filters in Wireshark to inspect packet behavior.
5. Analyzed packet details including IP addresses, ports, DNS resolution, TCP connection establishment, and encrypted HTTPS communication.

## Wireshark Filters Used
- `dns`
- `icmp`
- `tcp`
- `tcp.flags.syn == 1`
- `tcp.port == 443`

## Key Observations

### 1) DNS Analysis
Captured DNS query and response traffic and observed how a domain name is resolved into IP addresses. The capture showed DNS lookups for `chatgpt.com`, including an **A record** response that returned IPv4 addresses. Additional DNS record types such as **AAAA** and **HTTPS** were also observed.

### 2) ICMP Traffic
Used the `ping` command to generate ICMP echo request and echo reply packets. This demonstrated basic host reachability testing and how ICMP is used for connectivity checks.

### 3) TCP 3-Way Handshake
Observed a TCP three-way handshake during connection establishment. The sequence included:
- **SYN** from client to server
- **SYN, ACK** from server to client
- **ACK** from client to server

This shows how TCP establishes a reliable connection before application data is exchanged.

### 4) HTTPS / TLS Traffic
Captured encrypted traffic over port **443** and observed TLS handshake activity including **Client Hello**, **Server Hello**, and encrypted **Application Data**. This demonstrates how secure HTTPS communication is established and carried over TLS.

## Screenshots

### DNS Query and Response
![DNS Query and Response]

### ICMP Ping Traffic
![ICMP Ping]

### TCP 3-Way Handshake
![TCP Handshake]

### TLS / HTTPS Traffic
![TLS Traffic]

## What I Learned
- How to capture live network traffic using Wireshark
- How DNS resolution appears in packet captures
- How ICMP request/reply packets are used for connectivity testing
- How the TCP 3-way handshake establishes a connection
- How HTTPS/TLS traffic differs from plain network traffic
- How packet analysis helps in understanding communication flow and troubleshooting connectivity issues

## Conclusion
This lab helped strengthen my understanding of packet analysis, network protocols, and basic troubleshooting using Wireshark. It also provided hands-on exposure to DNS resolution, ICMP reachability testing, TCP connection establishment, and encrypted HTTPS communication.