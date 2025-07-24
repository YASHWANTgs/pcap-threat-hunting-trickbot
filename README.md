# PCAP Threat Hunting: TrickBot & Cobalt Strike Detection

This Project demonstrates uses a real world PCAP dataset and its used to network level threat hunting. DNS and HTTP Traffic are analysed to identify indicatord ot Trickbo ans Cobalt Strike command-and-control(C2) with the help of Wireshark.

# Project Summary
To identify if there is any malicious behaviour in thr PCAP traffic Through DNS,HTTP and IP.


# Methodology
DNS- To specificaly identify suspicious domain with high entropy and uncmmon TLDs.
HTTP inspection -It is mainly used to filter unsual user-agent strings and known C2 paatterns. Invistigaet mainly for POST requests or encrypted Pyloads
IP Pivoting - We have extracted IPs and move between HTTP layers where known malware infrastructure are assiocated with falgged IPs.



4. # MITRE Mapping: 
   - Mapped observed behavior to MITRE techniques:  
     - T1071.004: Application Layer Protocol - DNS  
     - T1071.001: Application Layer Protocol - HTTP  
     - T1090: Proxy Communication

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

This project shows real-world SOC actions , especially Tier 1–2 which require network forensics and IOC triage. It shows real world ability to hunt threats in raw traffic using open-source tools.
 

# Screenshots are provided as evidence

# Key screenshots are included in the repo:
- DNS anomalies  
- HTTP C2 traffic  
- IP extraction  


This was a short but practical blue-team project which focuses on extracting PCAP data—an essential skill for modern SOC and threat intel roles.
