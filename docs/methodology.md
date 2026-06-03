# Investigation Methodology

## Scope

The investigation analyzed a Windows 8.1 Enterprise forensic image associated with unauthorized access and suspicious system modification. The main objectives were to identify the message file, reconstruct user activity, review registry artifacts, and assess whether a trusted system executable was modified or replaced.

## Process

1. Reviewed file-system artifacts in FTK Imager.
2. Located suspicious message files and relevant timestamps.
3. Extracted and reviewed Windows registry hives.
4. Analyzed SYSTEM hive for host identity.
5. Analyzed SAM hive for account activity.
6. Reviewed NTUSER.DAT artifacts including UserAssist and RecentDocs.
7. Reviewed ShimCache/AppCompatCache for executable activity.
8. Extracted suspicious `Magnify.exe` and compared against `cmd.exe` / legitimate `Magnify.exe` evidence.
9. Verified suspicious executable identity using SHA-256 and VirusTotal.
10. Built a timeline and documented findings, limitations, and remediation recommendations.

## Tools

- FTK Imager
- Registry Explorer
- Shellbag Explorer, listed in project material but not used as a primary documented finding source
- PowerShell `Get-FileHash`
- VirusTotal
- Sandbox VM
