# PCAP Threat Hunting: TrickBot & Cobalt Strike Detection

This project showcases network-level threat hunting using a real-world PCAP dataset. We analyzed DNS and HTTP traffic to identify indicators of TrickBot and Cobalt Strike command-and-control (C2) activity using Wireshark.

## 🕵️ Project Summary

- **Objective:** Detect malicious behavior in captured PCAP traffic through DNS, HTTP, and IP pattern analysis.
- **Tools Used:**  
  - Wireshark  
  - MITRE ATT&CK Mapping


# Methodology

1. **DNS Analysis:**  
   - Identified suspicious domain lookups with high entropy and uncommon TLDs.
   - Cross-referenced domains with VirusTotal.

2. **HTTP Inspection:**  
   - Filtered for unusual user-agent strings and known C2 patterns.
   - Looked for large POST requests or encrypted payloads.

3. **IP Pivoting:**  
   - Extracted IPs and pivoted between DNS and HTTP layers.
   - Flagged IPs associated with known malware infrastructure.

4. **MITRE Mapping:**  
   - Mapped observed behavior to MITRE techniques:  
     - `T1071.004`: Application Layer Protocol - DNS  
     - `T1071.001`: Application Layer Protocol - HTTP  
     - `T1090`: Proxy Communication

# Findings

- Cobalt Strike beaconing behavior through DNS (high-frequency TXT queries).
- TrickBot activity disguised via HTTP POSTs with encrypted blobs.
- Malicious domains linked to multiple suspicious IPs.
- Patterns matched known IOCs from open threat feeds.

# Skills Demonstrated

- Packet-level threat detection
- IOC extraction and correlation
- DNS tunneling analysis
- MITRE ATT&CK mapping
- SOC-style investigation workflow

# Relevance

This project reflects real-world SOC responsibilities, especially Tier 1–2 roles requiring network forensics and IOC triage. It demonstrates hands-on ability to hunt threats in raw traffic using open-source tools.

---

#Screenshots

# Key screenshots are included in the repo:
- DNS anomalies  
- HTTP C2 traffic  
- IP extraction  
- MITRE mapping references


---

> This was a short but practical blue-team project focused on extracting actionable insights from PCAP data—an essential skill for modern SOC and threat intel roles.
