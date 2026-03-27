# Operation Blackout: Network Remediation & Protocol Audit

## 🛡️ Project Overview
This project involved identifying and resolving a DNS poisoning attack within a simulated enterprise environment. As part of a Cybersecurity Foundations Intensive, I acted as a Network Security Analyst to restore legitimate traffic flow to Titan Corp’s infrastructure and verify connection integrity using protocol analysis tools.

## 🛠️ Skills & Tools Demonstrated
* **Network Forensics:** Traffic auditing with tcpdump.
* **Version Control:** Professional documentation and repository management via Git/GitHub.
* **Network Troubleshooting:** Subnet calculation and CIDR alignment using ipcalc.
* **Security Remediation:** Resolving DNS hijacks and restoring secure communication paths.

## 📊 Technical Execution

### 1. Identifying the Attack
Traffic was being redirected to a malicious IP (10.99.99.99). Using ip route and diagnostic tools, I identified the compromised gateway and restored the legitimate path to the AWS Global Accelerator endpoint.

### 2. Protocol Verification (The TCP 3-Way Handshake)
To ensure the connection was secure and not intercepted, I performed a packet capture. The successful restoration was verified by identifying the standard TCP handshake flags:
* **[S] (SYN):** Initial connection request.
* **[S.] (SYN-ACK):** Server acknowledgment from the legitimate AWS IP (13.248.169.48).
* **[.] (ACK):** Final client confirmation.

### 3. Documentation
A full tlab_report.txt was generated, capturing terminal logs of the ipcalc results, successful pings, and the verified handshake sequence.
