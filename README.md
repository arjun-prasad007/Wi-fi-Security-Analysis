# Wi-Fi Network Security & Vulnerability Analysis 🛡️
This project focuses on analyzing local network traffic to identify active devices, monitor communication patterns, and demonstrate the risks of unencrypted data transmission using Wireshark.
🎯 Project Objectives
Monitor and map devices in a local Wi-Fi network using ARP (Address Resolution Protocol).
Analyze DNS queries to understand domain name resolutions.
Detect network anomalies and malformed packets using Wireshark’s Expert Information.
Demonstrate the vulnerability of HTTP by capturing plain-text credentials.
🛠️ Tools Used
Wireshark: Primary tool for packet sniffing and analysis.
VulnWeb: A deliberate-vulnerable web application used for legal testing of HTTP credential sniffing.
🔍 Key Findings
1. ARP & Network Mapping![](/assets/Arp-filtering.png)
By filtering for arp traffic, I was able to identify the Gateway (Router) and several connected devices (Mobile, Laptop) by their IP and MAC addresses. No ARP spoofing (duplicate IP) was detected during the session.
2. Expert Info & Anomaly Detection ![](/assets/Http.png)
Using the Expert Info tool, I identified several Malformed Packets and TCP Retransmissions, which indicate either signal interference or potential packet injection attempts in the network.
3. Credential Sniffing ![](/assets/Hrithik.png)
I analyzed an insecure HTTP POST request. The result showed that sensitive data like usernames and passwords were transmitted in plain text, making them easily visible to anyone sniffing the network.
Captured Username: hrithik roshan
Captured Password: krish
✅ Conclusion
This analysis highlights the critical importance of using HTTPS and secure protocols. Without encryption, any data sent over the network can be intercepted and read using simple packet analysis tools.
