1. Introduction / Abstract

When I first heard about Wireshark, people described it as “x-ray vision for the network,” but I never understood how literal that was. I’d used commands like ping or nmap before, but they always felt like black-box tools—silent, invisible processes happening underneath the surface. That changed when I built a small virtual lab and watched my first packet capture appear in Wireshark. Suddenly, every click, ping, request, and response became something I could see and understand in real time.

In this article, I walk through how I set up a controlled lab using Kali Linux and Metasploitable 2, how I captured ICMP packets using Wireshark, and what I learned about packet structure, network communication, and cybersecurity fundamentals. This project took me from “I know how to use ping” to “I understand what ping actually looks like on the wire.”

By the end of this article, you’ll see how Wireshark reveals the hidden conversations happening inside your network—and why packet analysis is one of the most important skills in cybersecurity.

2. Purpose and Background

I chose Wireshark for this project because almost every cybersecurity job requires understanding network traffic. Whether you’re doing network defense, digital forensics, penetration testing, malware analysis, or incident response, packet-level visibility is essential. Logs can be incomplete, alerts can be misleading, but packets never lie. They are the ground truth.

For this project, my goal was to:

Learn how two virtual machines communicate over a NAT network

Capture ICMP echo request/reply traffic

Break down packets into their component layers

Understand how Wireshark is used in real investigations

Troubleshoot realistic networking issues

My environment consisted of:

Kali Linux (10.0.2.3) — attacker/analysis machine

Metasploitable 2 (10.0.2.4) — vulnerable target

VirtualBox NAT Network — isolated network for safe experimentation

Going into the lab, I expected the setup to be simple but the packet interpretation to be confusing. Instead, the opposite happened: the packet analysis made perfect sense once I saw the structure, but configuring the network correctly was the real challenge. Those troubleshooting moments ended up teaching me more than I expected.

3. Installation and Setup Tutorial

This section recreates my exact steps so any student can follow them.

Prerequisites

You’ll need:

VirtualBox installed

Kali Linux VM

Metasploitable 2 VM

At least 8GB RAM recommended

Wireshark (preinstalled in Kali)

Step-by-Step Setup
Step 1: Create a NAT Network

in VirtualBox:

Tools → Network → NAT Networks → Add New NAT Network
Set IPv4 Range: 10.0.2.0/24
Enable DHCP


Step 2: Attach Kali VM to NAT Network

VirtualBox → Kali → Settings → Network

Attached to: NAT Network

Name: NatNetwork

Adapter Type: Intel PRO/1000 MT Desktop

Promiscuous Mode: Deny


Step 3: Attach Metasploitable VM to the Same Network


Step 4: Verify IP Addresses

In Kali:

ip a


In Metasploitable:

ifconfig


Expected results:

Kali → 10.0.2.3

Metasploitable → 10.0.2.4


Step 5: Test Connectivity

From Kali:

ping 10.0.2.4


Should show replies.


Step 6: Start Wireshark
sudo wireshark


Select interface: eth0

4. Using the Software – Practical Example

To generate ICMP traffic, I kept Wireshark running on eth0 and executed:

ping 10.0.2.4


Wireshark immediately displayed:

Echo request (Type 8)

Echo reply (Type 0)

Sequence numbers

TTL values

IP and MAC addresses

I applied a display filter:

icmp


Breaking down one ICMP Echo Request in Wireshark, I learned:

Frame Layer → metadata, length, interface

Ethernet Layer → MAC addresses

IP Layer → source/destination IP, TTL

ICMP Layer → type, code, checksum, identifier, sequence

The corresponding ICMP Echo Reply matched exactly, proving how ping confirms host reachability.


This hands-on example made me appreciate Wireshark as both a teaching tool and a professional tool for investigations.

5. Research Insights

6. Challenges and Problem-Solving

My biggest challenges were:

Issue 1 — Wrong Network Mode

I accidentally used Bridged mode at first, causing unstable connectivity and potential exposure to my home network.

Switched both VMs to the same NAT Network.

Issue 2 — Wrong Wireshark Interface

Wireshark showed only IPv6 multicast traffic at first.

Capturing on eth0 inside Kali solved the issue.

Issue 3 — Permissions

Wireshark required root privileges.


sudo wireshark

7. Conclusion and Future Applications

This project completely changed how I view network communication. I realized that even simple tools like ping reveal far more information than most people expect. By analyzing ICMP packets, I gained experience with how real defenders interpret traffic during investigations.

Skills I developed:

Network configuration in VirtualBox

Packet capture and filtering

Layer-by-layer analysis

Troubleshooting connectivity issues

In the future, I plan to analyze:

DNS traffic

TCP 3-way handshake

Nmap scan packets

Credential transmissions over insecure protocols

Packet analysis is now one of my strongest cybersecurity skills.

8. Resources & Links


9. Self-Assessment Reflection

I am proud of how much troubleshooting I completed on my own. Before this lab, I did not understand how NAT networking worked or why Wireshark sometimes shows no traffic. After several errors and fixing them, I now understand how virtual networks behave and how to capture packets correctly.

The section I am most proud of is the Practical Example because it clearly walks through the ICMP analysis. I would like feedback on whether my technical explanations were clear enough for a Medium audience. I believe this article demonstrates my ability to learn tools independently, document technical processes, and apply academic research to hands-on cybersecurity work.
