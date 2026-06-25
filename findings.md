# Findings

## DNS
- Observed DNS queries and responses for domain resolution
- Identified A record responses returning IPv4 addresses for `chatgpt.com`
- Also observed AAAA and HTTPS DNS record lookups

## ICMP
- Captured ICMP echo request and echo reply packets generated using ping
- Verified successful reachability between the local system and destination host

## TCP
- Observed the TCP 3-way handshake: SYN -> SYN, ACK -> ACK
- Verified that TCP establishes a reliable connection before data transfer begins

## HTTPS / TLS
- Captured encrypted traffic over port 443
- Observed TLS handshake packets such as Client Hello and Server Hello
- Saw encrypted application data exchanged after the handshake

## Troubleshooting Value
- DNS packets help diagnose name resolution issues
- ICMP helps verify host reachability
- TCP analysis helps understand connection establishment and failures
- TLS traffic analysis helps identify secure communication over HTTPS