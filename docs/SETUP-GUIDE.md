# SETUP-GUIDE
This guide explains how to set up the cybersecurity lab used in this project, including Kali Linux, Metasploitable 2, VirtualBox networking, and Wireshark.

---

## Requirements
Before starting, install and download the following:

- **VirtualBox**
- **Kali Linux VM**
- **Metasploitable 2 VM**
- Minimum **8 GB RAM**
- Basic command-line familiarity

---

## Step 1: Create a NAT Network in VirtualBox
1. Open VirtualBox
2. Click **Tools** on the left
3. Select **Network**
4. Choose **NAT Networks**
5. Click the **+ (Plus)** button to add a new NAT Network
6. Leave defaults as-is
7. Make sure **Enable** is checked

This network will allow both VMs to talk to each other.

---

## Step 2: Attach VMs to the NAT Network
For **Kali Linux VM**:
1. Click **Settings**
2. Go to **Network**
3. Adapter 1 → Attached To: **NAT Network**
4. Choose the NAT Network you created

Repeat the same steps for **Metasploitable 2**.

---

## Step 3: Boot VMs and Check IP Addresses
Inside each VM, run:


Look for an IP like:


If both VMs show a similar range, they are on the same network.

---

## Step 4: Test Connectivity Between VMs
From **Kali**, ping the Metasploitable host:



You should see replies.

If not, check:
- The VM network settings
- VirtualBox NAT Network settings

---

## Step 5: Install Wireshark on Kali
Run:




If asked whether non-root users can capture packets, select **Yes**.

---

## Step 6: Begin Traffic Capture
1. Open Wireshark
2. Select your active network interface (usually `eth0`)
3. Type this filter:


4. In Kali Terminal, run:



Now you will see ICMP (ping) packets appear in Wireshark.

---

## Conclusion
Your virtual cybersecurity lab is now fully set up. You can use this environment for packet analysis, security testing, and understanding how network traffic behaves.
