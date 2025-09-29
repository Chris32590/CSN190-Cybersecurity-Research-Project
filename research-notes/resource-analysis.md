Topics:
1) Ransomware Evolution & Defense Strategies
2) IoT Device Security & Government Surveillance Risks

Topic 1: Ransomware Evolution & Defense Strategies
Resource 1
Citation: Cen, M., Zhang, X., & Sun, Z. (2024). Ransomware early detection: A survey. Computer Networks, 240, 110137. https://www.sciencedirect.com/science/article/pii/S1389128623005832
Type: Academic Article
Synopsis: This survey explains how researchers try to catch ransomware early. It compares behavior analysis, system calls, entropy features, and machine learning approaches, and lists common datasets and metrics. 
It’s useful because it gives me a big picture of what works and where the gaps are (like detecting brand new families before encryption).
Limitation: full text is behind a paywall and some datasets are older.
Link: https://www.sciencedirect.com/science/article/pii/S1389128623005832 (Available through library databases)
Relevance: 5/5 -  Directly supports my focus on evolving defenses and early detection.

Resource 2
Citation: Aljabri, M., Alqahtani, A., & Al-Sarem, M. (2024). Ransomware detection based on machine learning using memory forensics. Alexandria Engineering Journal, 73, 1–14. https://www.sciencedirect.com/science/article/pii/S1110866524000082
Type: Academic Article
Synopsis: This paper uses memory forensics plus ML to find ransomware in RAM, aiming to detect unknown variants quickly. It explains feature extraction from memory images and shows promising accuracy in lab tests.
I like it because it looks beyond files on disk and tries to spot attacks while they’re running. 
Limitation: tested mainly in controlled setups; real-world performance needs more proof.
Link: https://www.sciencedirect.com/science/article/pii/S1110866524000082 (Available through library databases)
Relevance: 4/5 - Adds a practical, technical angle on pre-encryption detection.

Resource 3
Citation: Chainalysis. (2024, February 7). Ransomware payments exceed $1 billion in 2023, hitting record high after 2022 decline. https://www.chainalysis.com/blog/ransomware-2024/
Type: Industry Blog / Data Report
Synopsis: This report shows how big the ransomware problem has become using blockchain data.
It says 2023 set a record for ransom payments greater than $1 Billion, explains attacker trends, and mentions major cases. 
It’s valuable because it gives current numbers and shows the “why it matters” side.
Limitation: it tracks crypto payments, so it might miss some costs or methods.
Link: https://www.chainalysis.com/blog/ransomware-2024/
Relevance: 5/5 — Strong, up-to-date context for the “evolution” part of my topic.

Resource 4
Citation: Casas, P., Blancas, J., & Villanueva, A. (2025, May 21). Ransomware Report 2023: Targets, motives, and trends. Outpost24 KrakenLabs. https://outpost24.com/blog/ransomware-report-2023-targets-motives-and-trends/
Type: Industry Research Report
Synopsis: A threat intel overview of active groups, victim sectors, and double extortion tactics. It tracks leak-site activity, highlights top gangs, and shows how operations changed across 2022–2023.
It helps me tie technical defenses to real attacker behavior.
Limitation: relies on public leaks, so hidden incidents aren’t counted.
Link: https://outpost24.com/blog/ransomware-report-2023-targets-motives-and-trends/
Relevance: 5/5 Directly useful for understanding modern ransomware TTPs and planning defenses.


Topic 2: IoT Device Security & Government Surveillance Risks
Resource 1
Citation: Sun, K., Chen, C., & Zhang, X. (2020). “Alexa, stop spying on me!”: Speech privacy protection against voice assistants. In Proceedings of ACM SenSys 2020.
Type: Academic Conference Paper
Synopsis: This study focuses on smart speakers like Alexa and Google Home. It highlights how these devices sometimes record private conversations, even without being triggered. 
The authors warn that such devices can become perfect listening posts. They propose fixes, but the bigger message is clear, technology designed to assist us could also be quietly observing.
Limitation: full text requires ACM access.
Link: Available through ACM Digital Library
Relevance: 5/5 Direct tie to hidden surveillance potential in everyday devices.

Resource 2
Citation: Domazet, S., Marković, D., & Skakavac, T. (2024). Privacy under threat: The intersection of IoT and mass surveillance. Pravo – Teorija i Praksa, 41(3), 109–124.
Type: Academic Article
Synopsis: This article explores how IoT and surveillance blend into a powerful tool for monitoring entire populations. It notes that without strong laws, the line between safety and control blurs. 
The paper suggests IoT networks can enable unseen monitoring at a scale never before possible. It also connects to GDPR, which requires consent and transparency making secret surveillance through IoT a direct legal violation. 
Limitation: it’s more theory and law based, less about specific technical hacks.
Link: Open access via ResearchGate
Relevance: 5/5 Focuses directly on IoT mass surveillance risks.

Resource 3
Citation: Díaz, Á. (2020, December 16). When police surveillance meets the “Internet of Things.” Brennan Center for Justice.
Type: Think-Tank Policy Brief
Synopsis: This report explains how police already tap into IoT data like Ring cameras, Fitbits, and smart assistants. It shows real cases where IoT evidence solved crimes but raises questions about what else might be quietly collected. 
The piece hints that IoT is becoming a surveillance net woven into our daily lives, often without our awareness.
Limitation: doesn’t cover technical exploits, mostly legal and policy issues.
Link: https://www.brennancenter.org/our-work/research-reports/when-police-surveillance-meets-internet-things
Relevance: 5/5 Perfect for showing how government surveillance is already blending with IoT.

Resource 4
Citation: Tanz, J. (2017, March 8). The CIA leak exposes tech’s vulnerable future. WIRED.
Type: Professional/Industry Article
Synopsis: This article looks at WikiLeaks’ Vault 7 leaks, which exposed CIA tools for hacking IoT. It explains how smart TVs and even cars could be turned into surveillance tools.
It raises the possibility that if agencies can do this, we may never truly know when our devices are working for us or spying on us. 
Limitation: it’s from 2017, so not the newest source.
Link: https://www.wired.com/2017/03/cia-leak-exposes-techs-vulnerable-future/
Relevance: 4/5 Strong example of surveillance potential hidden in consumer devices.


Comparison Notes
Ransomware sources are focused on criminal groups, money, and technical defenses. IoT surveillance sources, on the other hand, suggest something more subtle how the very devices we depend on can become quiet informants.
Ransomware is visible when it strikes, but IoT surveillance may be happening without people even noticing. This makes ransomware a direct fight, while IoT surveillance feels like a hidden struggle between privacy and control.
It also raises legal questions: in the U.S., secret surveillance can clash with the Fourth Amendment, while in Europe, GDPR demands transparency and consent before personal data is collected. 
Together, these highlight the global tension between national security interests and personal freedom.

Questions That Emerged
1) What features and telemetry best catch ransomware before encryption without too many false positives?
2) How can incident response tools combine on host evidence with crypto payment intelligence to reduce impact?
3) Are backdoors being placed in IoT devices under the label of security features, giving governments secret access and could always on microphones in Alexa or Siri already serve this purpose?
4) If IoT gadgets can map our lives so precisely, will courts truly limit their use, or will laws bend quietly to allow broader monitoring?
5) Are tech companies quietly cooperating with governments by leaving “doors open” in IoT devices, blurring the line between corporate data collection and state surveillance?
6) If future homes, cars, and cities are built around IoT, are we locking ourselves into a world where surveillance becomes the default, and privacy the exception?
