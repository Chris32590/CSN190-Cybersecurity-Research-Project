Cracking Open the Network: What I Learned by Analyzing Traffic
With Wireshark
By Christopher Perez
CSN 190 – Cybersecurity
December 18, 2025

Introduction
When I first heard about Wireshark, people described it as “x-ray vision for the network,” but I never fully
understood how literal that description was. I had used commands like ping and nmap before, but they felt
like black-box tools—processes running silently in the background. That changed when I built a small
virtual lab and captured my first packet in Wireshark. Suddenly, every request and response became
visible, and network communication finally made sense.
In this article, I explain how I set up a controlled cybersecurity lab using Kali Linux and Metasploitable 2,
how I captured ICMP traffic using Wireshark, and what I learned about packet structure and network
behavior. This project took me from simply using networking tools to truly understanding what happens on
the wire.
Purpose and Background

Wireshark is one of the most important tools in cybersecurity because it provides packet-level visibility.
Logs and alerts can be incomplete or misleading, but packets represent the raw truth of what is happening
on a network. Professionals in digital forensics, incident response, penetration testing, and network
defense rely on packet analysis every day.
The purpose of this project was to build an isolated lab environment, generate real ICMP traffic, analyze
packet structure, and understand how Wireshark is used in real-world investigations. ICMP was chosen
because it is simple, easy to generate, and commonly used for reconnaissance.
Lab Environment Overview

I created a controlled virtual lab using VirtualBox. Kali Linux was used as the analysis machine, while
Metasploitable 2 served as a vulnerable target. Both systems were connected to the same NAT Network,
allowing safe communication without exposing my home network. This setup allowed me to generate traffic
and capture it in a realistic but secure environment.
ICMP Traffic Analysis with Wireshark
With Wireshark running on Kali, I generated ICMP traffic by pinging the Metasploitable machine. Wireshark
immediately displayed echo request and echo reply packets. By applying an ICMP display filter, I was able
to isolate and analyze only the relevant traffic.
Breaking down each packet revealed multiple OSI layers, including frame metadata, Ethernet MAC
addresses, IP addressing information, and ICMP-specific fields such as type, sequence number, and
identifier. This analysis helped me understand that ping is not just a simple connectivity test, but a
structured protocol with detailed information.
Research Insights

Industry research reinforces the importance of packet analysis. NIST Special Publication 800-94 explains
that protocols like ICMP are often used during reconnaissance and early attack stages. Similarly, the
Verizon 2024 Data Breach Investigations Report highlights reconnaissance as a common first step in
real-world attacks. RFC 792 defines the ICMP standard exactly as Wireshark displays it, confirming that the
packet structures observed in my lab follow global protocol standards.
Challenges and Problem-Solving

This project required significant troubleshooting. Early issues included incorrect network modes, capturing
on the wrong interface, and permission errors when launching Wireshark. Resolving these problems taught
me how virtual networks behave and how important correct configuration is for successful packet capture.
Conclusion and Future Applications

This project transformed my understanding of networking and cybersecurity. By analyzing ICMP traffic, I
gained practical experience with packet capture, protocol analysis, and troubleshooting. In the future, I plan
to analyze more advanced protocols such as DNS, TCP handshakes, and Nmap scans. Packet analysis
has become one of my strongest and most valuable cybersecurity skills.
Resources and Links

GitHub Repository: https://github.com/Chris32590/CSN190-Cybersecurity-Research-Project
Wireshark: https://www.wireshark.org
NIST SP 800-94, Verizon DBIR 2024, RFC 792
