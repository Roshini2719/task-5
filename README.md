
📁 PCAP Overview
Description
This packet capture (PCAP) file records:

DNS Queries & Responses for the domain tryhackme.com

ICMP Echo Requests/Replies (Ping) to/from the IP 104.22.55.228 (a TryHackMe web server)

ARP Requests & Responses to resolve the local gateway IP (10.0.2.1)

PTR Lookup Attempts for reverse DNS resolution

📊 Key Observations
DNS Resolution

A record response: 104.22.55.228, 172.67.27.10, 104.22.54.228

AAAA record response: IPv6 address 2606:4700:9766:d299:d3fe:fd:ae35:d89c

Reverse DNS (PTR) failed: No such name

ICMP Echo (Ping) Behavior

Regular ICMP echo requests sent from 10.0.2.4 to 104.22.55.228

Responses received with average TTL=56 (indicating about 8 hops)

Continuous pings indicate network reachability testing

ARP Resolution

Standard ARP exchange between 10.0.2.4 and local gateway 10.0.2.1

🧪 Use Cases
This project is useful for:

Students learning network protocols like ICMP, DNS, ARP

Cybersecurity practitioners analyzing reconnaissance behavior

Penetration testers preparing CTF environments or understanding TryHackMe interactions

Anyone interested in understanding basic network communication patterns
DNS Resolution to tryhackme.com

The host 10.0.2.4 sent DNS queries to resolve tryhackme.com.

It received multiple A record responses:

104.22.55.228

104.22.54.228

172.67.27.10

Also received an AAAA record (IPv6): 2606:4700:9766:d299:d3fe:fd:ae35:d89c

Attempted a reverse DNS lookup (PTR) for IP 10.0.2.4, which failed: “No such name”.

ICMP Traffic (Ping Analysis)

The host 10.0.2.4 sent continuous ICMP echo requests to 104.22.55.228.

Corresponding ICMP echo replies were received successfully.

TTL values were around 56, suggesting ~8 network hops to the destination.

Indicates good network connectivity with the TryHackMe server.

ARP Communication

Before reaching the internet, the host resolved its default gateway (10.0.2.1) via ARP.

ARP request: “Who has 10.0.2.1?”

ARP reply: “10.0.2.1 is at 52:54:00:12:35:00”
