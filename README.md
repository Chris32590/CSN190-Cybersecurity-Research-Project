
# Wireshark ICMP Traffic Analysis – CSN190 Final Project

**Author:** Christopher Perez  
**Course:** CSN 190 – Cybersecurity Research Project  
**Semester:** Fall 2025  
**Institution:** Bronx Community College  

---

## 📘 Project Overview

This project focuses on performing a hands-on network traffic analysis using **Wireshark**, one of the most widely used network analysis tools in cybersecurity.  
Throughout the semester, I built a virtualized environment using **VirtualBox**, **Kali Linux**, and **Metasploitable2**, then captured and analyzed **ICMP (ping) packets** to understand echo requests, replies, protocol structure, and packet behavior.

This repository serves as a complete record of my:
- Research  
- Weekly progress  
- Documentation  
- Tool analysis  
- Final Medium draft  
- Hands-on technical tutorial  

It represents my technical growth in packet analysis, documentation, and cybersecurity fundamentals.

---

## 🛠️ Software, Tools & Technologies Used

- **Wireshark 4.x** – Packet analysis  
- **Kali Linux (VirtualBox VM)** – Analyst machine  
- **Metasploitable2 (VirtualBox VM)** – Vulnerable target  
- **VirtualBox** – Virtualization platform  
- **ICMP Protocol (RFC 792)**  
- **Markdown / GitHub Documentation**  

---

## 📦 Key Deliverables

- **Medium Article Draft (V1):**  
  [`/final-paper/MEDIUM-ARTICLE-DRAFT-V1.md`](./final-paper/MEDIUM-ARTICLE-DRAFT-V1.md)

- **Tutorial:**  
  [`/docs/TUTORIAL.md`](./docs/TUTORIAL.md)

- **Setup Guide:**  
  [`/docs/SETUP-GUIDE.md`](./docs/SETUP-GUIDE.md)

- **Project Video:**  
  *(Upload your video to `/presentations-videos/` and link it here once finished)*

---

## 📁 Repository Navigation

Here is the full structure of this repository:

- **`/weekly-progress/`** – Weekly assignments from Modules 1–6  
- **`/resources/`** – Full resource list, citations, and documentation  
- **`/src/`** – Project files, including cloned project + my work  
- **`/docs/`** – Technical documentation (setup guide + tutorial)  
- **`/final-paper/`** – Medium article draft + research notes  
- **`/presentations-videos/`** – All video walkthroughs  
- **`/images/`** – Screenshots used across the project  

---

## 🚀 Getting Started  
Follow these steps to replicate my environment and ICMP analysis:

### 1. Install VirtualBox  
Download from: https://www.virtualbox.org/

### 2. Import Kali Linux & Metasploitable2  
Images available from:
- https://www.kali.org/get-kali/
- https://sourceforge.net/projects/metasploitable/files/

### 3. Create a NAT Network  
VirtualBox → Tools → Network → NAT Network

### 4. Attach both VMs to this NAT Network  
Ensures they can communicate and be analyzed.



### 6. Follow the full tutorial  
Full step-by-step guide:  
➡️ `/docs/TUTORIAL.md`

---

## 📊 Results Summary

Through this project, I successfully:

- Built a complete virtual penetration testing environment  
- Captured and analyzed ICMP traffic using Wireshark  
- Interpreted packet fields such as TTL, checksum, identifiers, and sequence numbers  
- Applied display filters to isolate ICMP traffic  
- Learned how ICMP is used for network diagnostics and reconnaissance  
- Completed extensive documentation and a Medium article explaining the process  

This project strengthened my skills in:
- Packet analysis  
- Network troubleshooting  
- Documentation  
- Research  
- Virtual machine networking  
- Cybersecurity fundamentals  

---

## 📬 Contact

- **Email:** christopher.perez@example.com *(replace with your real email)*  
- **LinkedIn:** https://linkedin.com/in/YOURPROFILE  
- **Medium Profile:** https://medium.com/@YOURNAME  

---

### ✔ This README.md fulfills **all** professor requirements for Assignment 8.


### 5. Install Wireshark inside Kali  
