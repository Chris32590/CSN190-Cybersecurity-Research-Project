# Wireshark ICMP Traffic Analysis Tutorial  
CSN190 – Cybersecurity Project  
Author: Christopher Perez  
Semester: Fall 2024  

---

# 📘 Introduction

This tutorial walks through how to analyze ICMP (ping) traffic using Wireshark inside a controlled virtual environment. ICMP is one of the most common protocols used for network testing and is often leveraged during reconnaissance in cybersecurity. Understanding ICMP traffic is a foundational skill for packet analysis, intrusion detection, and network troubleshooting.

This guide is based on the hands-on work completed in my CSN190 project using:
- Kali Linux (attacker/analyst machine)
- Metasploitable2 (target VM)
- VirtualBox NAT Network
- Wireshark (traffic analyzer)

---

# 🖥️ Lab Environment Setup

Before starting the analysis, the following environment was configured:

### **Tools Used**
- **VirtualBox 7.x**
- **Kali Linux VM**
- **Metasploitable2 VM**
- **Wireshark 4.x**

### **Network Configuration**
Both VMs must be on the same NAT Network so they can communicate.

**Steps:**
1. Open VirtualBox.
2. Go to **Tools → Network → NAT Networks**.
3. Create a NAT Network (e.g., `CSN-NAT-Network`).
4. Attach Kali Linux and Metasploitable2 to this network.
5. Start both machines.

**Verify connectivity:**
On Kali:



---

# 🧪 Step 1: Start Wireshark & Select the Correct Interface

1. Open **Wireshark** in Kali Linux.
2. Select the network interface connected to the NAT Network (usually `eth0`).
3. Click **Start Capturing Packets**.

**[Screenshot: Wireshark capture interface selection]**

---

# 🟦 Step 2: Filter ICMP Traffic

To focus only on ping-related packets, apply this display filter:




This filter isolates all ICMP requests and replies.

**[Screenshot: Wireshark with icmp filter applied]**

---

# 🟢 Step 3: Send ICMP Echo Requests (Ping)

In Kali, open a terminal:


Example:

This sends EXACTLY four ICMP Echo Requests to the target machine.

**[Screenshot: Kali terminal showing ping results]**

---

# 📡 Step 4: Analyze ICMP Packets in Wireshark

After sending pings, return to Wireshark. You will now see:

- Echo (ping) requests  
- Echo replies  

Click on any ICMP packet and expand the middle panel sections:

### What to Look For:
---

### **1. Internet Protocol Version 4 (IPv4)**  
Shows:
- Source IP  
- Destination IP  
- TTL (Time To Live)

Meaning:
- TTL decreases by 1 every hop. Low TTL = further distance.

---

### **2. ICMP Layer**

Key fields:
- **Type:**  
  - 8 = Echo Request  
  - 0 = Echo Reply  
- **Code:**  
  - Usually 0 for normal ping traffic  
- **Identifier:**  
  - Matches requests & replies  
- **Sequence Number:**  
  - Increments with each ping  
- **Checksum:**  
  - Detects corrupted packets  

**[Screenshot: ICMP packet details expanded]**

---

# 🔍 Step 5: Understanding the Packet Flow

Wireshark shows the request–reply pattern like this:

| Packet | Meaning |
|--------|---------|
| Echo (request) | Kali → Metasploitable2 |
| Echo (reply)   | Metasploitable2 → Kali |

Each request should have a matching reply.

### Example Insights:

- **Latency:** Shown in `ping` command results.
- **TTL differences:** Indicate OS or hop count.
- **Packet loss:** Shows connectivity or firewall issues.

---

# 🛠️ Step 6: Filtering for Deeper Analysis

Here are additional useful filters:

### Only Echo Requests:



### Only Echo Replies:


### Show ICMP + Only from Metasploitable:


### Show ICMP + Only from Kali:



**[Screenshot: advanced Wireshark filters]**

---

# 🧩 Step 7: Exporting the Capture (Optional)

You can export the capture file for documentation:

Wireshark → **File → Export Specified Packets → .pcapng**

This is useful for reports or further analysis in other tools.

---

# 📘 Final Notes & Learning Outcomes

After completing this ICMP analysis, you should now understand:

### ✔️ How ICMP works  
### ✔️ How pings travel through the network  
### ✔️ How to read packet fields in Wireshark  
### ✔️ How to filter and inspect traffic  
### ✔️ How to match requests and replies  
### ✔️ How to interpret TTL, sequence numbers, identifiers, and checksums  

This hands-on experience builds a strong foundation for more advanced cybersecurity work such as:

- Intrusion detection  
- Traffic anomaly detection  
- Reconnaissance analysis  
- Malware communication behavior  
- Network troubleshooting  

---

# 📎 References

- Wireshark User Guide: https://www.wireshark.org/docs/
- RFC 792 – ICMP Protocol: https://datatracker.ietf.org/doc/html/rfc792
- VirtualBox Networking Manual: https://www.virtualbox.org/manual/ch06.html
- LiveOverflow / ICMP Breakdown Video: https://youtu.be/7vCw5vNhbbU

---

**End of Tutorial**
