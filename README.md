# Computer-networks
Industry problems related to Computer Networks, employee website monitoring, web server monitoring and reading RFCs.

This repository is a combination of 4 small projects:

1. Employee Website Monitoring using Packet Analysis:

This project understands and demonstrates the technique which can be used to monitor the websites
accessed by employees based on IP and mac-address on a LAN network by analyzing appropriate
packets. Sniffer is combined with port mirroring feature on a switch to achieve the solution and
this is established using cisco packet tracer.

In the pkt file, open the command prompt at PC-0 and enter the commands:
ping 192.168.0.11 (pinging PC-1)
arp -a

and mention filters as ARP, ICMP in the sniffer.
The ARP packets are seen.

Now go to the switch and configure it by executing the following commands in the CLI:
> en
> conf t
> monitor session 1 source interface fa0/1
> monitor session 1 source interface fa0/2
> monitor session 1 destination interface fa0/24
> end

ping PC-1 again from the command prompt of PC-0 and the ICMP packets are now seen.

2. Web Server monitoring techniques:

An organization has deployed a Windows based web server on its network. The network
administrator has to identify the appropriate techniques for analyzing the below parameters.
1.TCP traffic (Incoming TCP Syn requests, TCP reset connections, TCP established connections,
TCP half open connections)
2.Technique to monitor specific application requests on Web server
3.Technique to monitor HTTP Get requests to on Web server
4.Server bandwidth
5.Port status of the web server
A combination of different types of tools like Wireshark, nmap, netstat is used with
appropriate commands and filters identified for achieving the required output.

3. RFC-1918: Private Network

A report prepared on RFC-1918. 
RFC-1918 allocates addresses for private networks. These private networks are an internet that is
just yours. To do this, you could set up your router to route public spaces internally or you could 
take your unused public IP addresses and treat them as an internal network, all specified under this
RFC report
