Secure and Redundant Multi-Branch Enterprise Network Design
This project demonstrates the design and implementation of a secure, redundant, and monitorable multi-branch enterprise network. The architecture focuses on network security, centralized management, logging, monitoring, and operational resilience, following real-world enterprise networking principles.The primary goal of this project is to simulate a real-world enterprise network with strong security controls, centralized management, and operational visibility.

📌 Project Overview
The network is engineered to support a high-availability enterprise environment, consisting of:

Central Office (HQ): Featuring high-speed core switching and perimeter security.

Branch Offices: Connected via secure WAN links.

Perimeter Security: Cisco ASA 5506-X firewall managing inside/outside traffic flow.

Centralized Services: Unified DHCP, Syslog logging, and TFTP configuration backup.

Secure Connectivity: Site-to-Site IPsec VPN tunnels for encrypted inter-site communication.

🔐 Security Architecture
🔸 Firewall & Edge Security (Cisco ASA)
Strict Inside / Outside interface isolation.

Dynamic NAT (PAT) for secure outbound internet access.

Granular Access Control Lists (ACL) for multi-layer traffic filtering.

🔸 VPN Infrastructure
Technology: Site-to-Site IPsec VPN terminated on Cisco ASA.

Policy: Dedicated VPN ACLs to define and protect "interesting traffic" between sites.

⚠️ Technical Note on Simulation Constraints: While the IPsec VPN and NAT architecture are fully configured based on real-world standards, Cisco Packet Tracer has known limitations regarding IPsec state visualization and NAT exemption (NAT 0) commands on ASA devices. These configurations are optimized for production-grade hardware or advanced emulators like GNS3/EVE-NG.

📊 Monitoring & Logging
🔹 Centralized Logging (Syslog)
Core Switch and Cisco ASA are configured to stream logs to a central Syslog server.

Facilitates proactive troubleshooting and historical event analysis.

🔹 Traffic Analysis (SPAN)
Mechanism: Switched Port Analyzer (SPAN) configured on the Core Switch.

Visibility: Mirroring critical traffic to a monitoring interface for inspection.
This approach reflects passive monitoring techniques commonly used in SOC and network operations teams.

⚠️ Packet Inspection Note: Packet Tracer does not support direct Wireshark integration. Therefore, packet-level analysis is demonstrated using Simulation Mode, which provides the conceptual framework for real-world Pcap inspection.

💾 Disaster Recovery & Configuration Management
Backup Strategy: Automated/Manual backups of running configurations to a central TFTP server on Server2.

Resilience: Ensures configuration persistence and rapid recovery in case of hardware failure.

🎯 Key Takeaways
Deployment of enterprise-grade firewall policies and security zones.

Implementation of centralized visibility (SOC-oriented logging).

Robust VPN architecture design and subnet management.

Awareness of simulation vs. production environments.

🚀 Future Roadmap
Migration to GNS3/EVE-NG for full IPsec tunnel verification and Wireshark integration.

Integration with SIEM platforms for advanced threat detection. 
