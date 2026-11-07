# Mininet lab: Snort and iptables

Small network lab where I got my hands dirty on two basic things of defensive security: intrusion detection and network filtering.

I used Mininet to simulate a full topology with user hosts, DMZ servers, routers, an attacker host and even a fake server hosting a malware. The goal was to understand how an IDS and a firewall work together when a real threat shows up.

First I triggered the download of a simulated malicious file from a client host. Snort, the IDS running on the router, matched the payload of the packet with a signature and raised an alert in the logs in real time.

Then I captured the traffic with tcpdump to get a proof of the transaction (a .pcap file), with the source and destination IPs and ports.

Finally I wrote an iptables rule on the FORWARD chain of the router to block all the traffic going to the server flagged as malicious. I tried to connect again and got a timeout, as expected.

What I liked is seeing the link between detection (IDS), proof (packet capture) and reaction (firewall). These are the same three steps you find in any SOC.

Tools used: Mininet, Snort, tcpdump, iptables.
