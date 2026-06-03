# Digital Forensics Investigation: Unauthorized System Access

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Type](https://img.shields.io/badge/type-DFIR%20Investigation-blue)
![Platform](https://img.shields.io/badge/platform-Windows%208.1-lightgrey)
![Tools](https://img.shields.io/badge/tools-FTK%20Imager%20%7C%20Registry%20Explorer%20%7C%20VirusTotal-orange)

Professional digital forensics investigation project analyzing unauthorized access and suspicious system modification on a Windows 8.1 Enterprise image. The investigation focuses on file-system evidence, Windows registry artifacts, user activity reconstruction, ShimCache/AppCompatCache analysis, and suspicious executable verification.

> Portfolio note: this is an academic DFIR project rebuilt as a professional investigation package. The repository intentionally presents only evidence supported by the report and presentation materials.

## Executive Summary

The investigation examined a Windows 8.1 Enterprise system named **SENSEI** after a suspicious message file was discovered. Analysis of file-system artifacts, registry hives, UserAssist, RecentDocs, SAM account metadata, ShimCache/AppCompatCache, and executable hash evidence indicated suspicious activity around **2015-12-12 03:24** and supported the hypothesis that `Magnify.exe` was likely replaced or renamed with `cmd.exe`.

The investigation documented image verification data, key artifacts, timeline reconstruction, account activity, suspicious executable comparison, and remediation recommendations.

## Repository Contents

| Path | Description |
|---|---|
| [`artifacts/report/Digital_Forensic_Investigation_Report.pdf`](artifacts/report/Digital_Forensic_Investigation_Report.pdf) | Final polished DFIR report. |
| [`artifacts/report/Digital_Forensic_Investigation_Report.docx`](artifacts/report/Digital_Forensic_Investigation_Report.docx) | Editable report version. |
| [`artifacts/presentation/Digital_Forensics_Case_Presentation.pdf`](artifacts/presentation/Digital_Forensics_Case_Presentation.pdf) | Case presentation PDF. |
| [`artifacts/presentation/Digital_Forensics_Case_Presentation.pptx`](artifacts/presentation/Digital_Forensics_Case_Presentation.pptx) | Editable case presentation. |
| [`data/timeline.csv`](data/timeline.csv) | Timeline extract from report and presentation artifacts. |
| [`data/evidence-register.csv`](data/evidence-register.csv) | Evidence register for major artifacts. |
| [`docs/findings-summary.md`](docs/findings-summary.md) | Key findings and confidence levels. |
| [`docs/methodology.md`](docs/methodology.md) | Investigation methodology and tools. |
| [`docs/hash-and-artifact-notes.md`](docs/hash-and-artifact-notes.md) | Hash values and suspicious executable notes. |
| [`docs/remediation-recommendations.md`](docs/remediation-recommendations.md) | Containment and hardening recommendations. |

## Tools Used

| Tool | Purpose |
|---|---|
| FTK Imager | Mounted/reviewed forensic image, file listings, timestamps, and exported suspicious artifacts. |
| Registry Explorer | Reviewed SYSTEM, SAM, NTUSER.DAT, RecentDocs, UserAssist, and AppCompatCache/ShimCache artifacts. |
| PowerShell `Get-FileHash` | Computed SHA-256 hash for suspicious executable evidence. |
| VirusTotal | Reviewed reputation/identity result for the suspicious executable hash. |
| Sandbox VM | Compared extracted executable behavior/metadata in a controlled environment. |

## Key Findings

- Suspicious `README.txt` message file was identified at `root/tools/README.txt`.
- SYSTEM hive identified the host as `SENSEI`.
- SAM and user activity artifacts supported Administrator-related activity near the event window.
- UserAssist showed `NOTEPAD.EXE` access at `2015-12-12 03:24:08`.
- AppCompatCache/ShimCache identified `Magnify.exe` as relevant near the attack window.
- The suspicious `Magnify.exe` was consistent with `cmd.exe` based on size/icon comparison and VirusTotal identification.
- Correct suspicious executable SHA-256:
  `0B9BC863E2807B6886760480083E51BA8A66118659F4FF274E7B73944D2219F5`

## Image Verification Data

| Hash Type | Value | Status |
|---|---|---|
| MD5 | `9a737b6a21ecbe979126c5661ca7b8db` | Verified in source presentation |
| SHA1 | `ebef2bdc6329563ccf85769c3e5b8ceca852992b` | Verified in source presentation |

## Skills Demonstrated

`Digital Forensics` `DFIR` `Incident Response` `Windows Registry Forensics` `FTK Imager` `Registry Explorer` `ShimCache` `UserAssist` `Timeline Reconstruction` `Hash Analysis` `Evidence Handling`

## Resume / LinkedIn Project Description

Conducted a Windows digital forensics investigation of unauthorized system access and suspicious executable modification. Analyzed file-system evidence, registry hives, SAM account data, UserAssist, RecentDocs, ShimCache/AppCompatCache, and executable hash results to reconstruct a timeline, identify likely `Magnify.exe`/`cmd.exe` substitution, and produce a professional investigation report with findings, limitations, and remediation recommendations.

## Author

Rethick Jeganathan  
M.S. Cybersecurity & Information Assurance, Roosevelt University  
LinkedIn: <https://linkedin.com/in/rethick>
