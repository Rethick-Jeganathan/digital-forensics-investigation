# Digital Forensics Investigation & Memory Analysis

![Status](https://img.shields.io/badge/Status-Completed-brightgreen) ![Tools](https://img.shields.io/badge/Tools-FTK%20Imager%20%7C%20Autopsy%20%7C%20Volatility%20%7C%20Wireshark-blue) ![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey)

## Overview

A hands-on digital forensics investigation conducted on a compromised Windows and Linux environment. The investigation identified unauthorized access, suspicious file activity, and attacker behavior through systematic analysis of disk images, memory dumps, registry artifacts, and network traffic.

## Project Files

| File | Description |
|------|-------------|
| `Digital_Forensic_Investigation_Report.pdf` | Full investigation report with findings, timeline, and IOCs |
| `DFIR_Presentation.pptx` | Case presentation summarizing investigation workflow and evidence |

## Investigation Scope

- **Disk Forensics** — Acquired and analyzed disk images using FTK Imager and Autopsy; recovered deleted files, browser history, and user activity logs
- - **Memory Analysis** — Used Volatility to extract process trees, network connections, registry hives, and injected code from memory dumps
  - - **Registry Analysis** — Examined UserAssist, ShimCache, and MRU keys via Registry Explorer to reconstruct attacker footprint
    - - **Network Traffic** — Analyzed PCAP files in Wireshark to identify C2 communication patterns and data exfiltration indicators
      - - **Timeline Reconstruction** — Built a full attack timeline mapping attacker actions to MITRE ATT&CK techniques
       
        - ## Tools Used
       
        - | Tool | Purpose |
        - |------|---------|
        - | FTK Imager | Disk image acquisition |
        - | Autopsy | File system and artifact analysis |
        - | Volatility | Memory forensics |
        - | Registry Explorer | Windows registry analysis |
        - | Wireshark | Network traffic analysis |
        - | MITRE ATT&CK | Technique mapping |
       
        - ## Key Findings
       
        - - Identified unauthorized system access via credential misuse
          - - Recovered suspicious executable artifacts in user temp directories
            - - Mapped attacker behavior to MITRE ATT&CK T1078 (Valid Accounts), T1059 (Command Execution), and T1041 (Exfiltration)
              - - Produced containment and remediation recommendations
               
                - ## Skills Demonstrated
               
                - `Digital Forensics` `Incident Response` `Memory Analysis` `Registry Forensics` `Network Analysis` `MITRE ATT&CK` `Wireshark` `Volatility` `FTK Imager` `Autopsy`
               
                - ---

                **Associated with:** Roosevelt University — M.S. Cybersecurity & Information Assurance
                **Period:** Sep 2024 – Nov 2024
                **Author:** [Rethick Jeganathan](https://linkedin.com/in/rethick)
