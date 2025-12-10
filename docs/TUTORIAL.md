# Wireshark ICMP Traffic Analysis Tutorial

This tutorial shows how to capture and analyze ICMP traffic (ping requests and replies) using Wireshark inside a VirtualBox network.

---

## Step 1: Open Wireshark
1. Launch Wireshark on your Kali VM
2. Select the main network interface (usually `eth0`)

---

## Step 2: Apply ICMP Filter
In the filter bar at the top, type:


Press Enter — Wireshark will now show only ICMP packets.

---

## Step 3: Generate ICMP Traffic Using Ping
From Kali Terminal:


Example:


You will see:

- **Echo Request** packets (Type 8)
- **Echo Reply** packets (Type 0)

These packets confirm communication between the machines.

---

## Step 4: Inspect an ICMP Packet
Click one packet and expand the layers:

### 🔹 Frame
Metadata (size, arrival time)

### 🔹 Ethernet II
Source and destination MAC addresses

### 🔹 IPv4
Source and destination IPs  
TTL (Time To Live)

### 🔹 ICMP
Important values:
- Type: 8 (Request) or 0 (Reply)
- Code: 0
- Identifier
- Sequence Number

---

## Step 5: Save the Capture
Go to:



Save the `.pcapng` file to your project folder.

---

## Step 6: Interpretation
Analyzing ICMP helps understand:

- Host discovery
- Network connectivity
- Latency (Response times)
- Possible packet loss
- Behavior of echo requests in network testing

---

## Conclusion
You have successfully performed an ICMP traffic analysis using Wireshark. This is a foundation for more advanced network forensics, packet inspection, and intrusion detection.

docs/
   SETUP-GUIDE.md
   TUTORIAL.md
