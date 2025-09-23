Module 3 — GitHub Project Analysis
CSN 190 – Research Notes

---

Topic 1: Ransomware Evolution & Defense Strategies

GitHub Project 1: Raccine
- Citation: Neo23x0. (2025). Raccine — A Simple Ransomware Vaccine. GitHub. https://github.com/Neo23x0/Raccine
- Type: Security Tool
- Synopsis: Raccine is a Windows tool that tries to stop ransomware before it can delete backups. It looks for dangerous commands like “delete shadows” and kills the program that is trying to run them. It’s very lightweight and doesn’t need an agent, which makes it easy to test. The downside is that it hasn’t been updated recently, and sometimes it interferes with backup software. Stats: around 969 stars, 125 forks.
- Relevance: 4/5. It shows a clear way to block part of a ransomware attack, but it’s not a full solution.

GitHub Project 2: Velociraptor
- Citation: Velocidex. (2025). Velociraptor — Endpoint Visibility and DFIR Collection. GitHub. https://github.com/Velocidex/velociraptor
- Type: DFIR Tool (Digital Forensics and Incident Response)
- Synopsis: Velociraptor is a big tool for investigating and responding to incidents like ransomware. It lets investigators collect evidence from many computers at once, check for suspicious files, and see how attackers moved through a system. It runs on Windows, Linux, and macOS. It has strong documentation and is still being updated. Stats: about 3.5k stars, 555 forks.
- Relevance: 5/5. This tool is very relevant because it covers the response side of ransomware. It helps show what to do after an attack happens.

---

Topic 2: IoT Device Security & Government Surveillance Risks

GitHub Project 1: IoTGoat
- Citation: OWASP. (2025). IoTGoat — Deliberately Insecure IoT Firmware (OpenWrt). GitHub. https://github.com/OWASP/IoTGoat
- Type: Educational Repository
- Synopsis: IoTGoat is a teaching tool that is built to be insecure on purpose. It runs like an IoT device with common vulnerabilities based on the OWASP Top 10 list. Students and researchers can test attacks against it and then practice fixing them. This makes it safe to learn how hackers can target IoT devices without breaking a real one. Stats: about 816 stars, 144 forks.
- Relevance: 5/5. Very relevant because it is made to teach IoT security issues, which connects directly to my topic.

GitHub Project 2: RouterSploit
- Citation: threat9. (2025). RouterSploit — Exploitation Framework for Embedded Devices. GitHub. https://github.com/threat9/routersploit
- Type: Security Tool / Exploitation Framework
- Synopsis: RouterSploit is like Metasploit but focused on routers and IoT devices. It has modules for scanning, exploiting, and testing passwords on many different brands of hardware. It’s useful for showing how weak IoT security can be in real life. The project has a lot of stars but has not had a big release in a while. Stats: about 12.8k stars, 2.4k forks.
- Relevance: 4/5. It shows the attack side of IoT insecurity and is good for demonstrations, but it’s not always up to date.

---

Comparison Notes
- Ransomware: Raccine is simple and focuses on prevention, while Velociraptor is much bigger and focuses on investigation after the fact. Together, they show both sides of defense.
- IoT: IoTGoat is a safe playground for learning IoT security, while RouterSploit is an actual attack toolkit. Using both gives a full picture of the problem.
