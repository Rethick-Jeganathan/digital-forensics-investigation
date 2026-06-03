# Hash and Artifact Notes

## Forensic Image Verification

| Hash Type | Value | Status |
|---|---|---|
| MD5 | `9a737b6a21ecbe979126c5661ca7b8db` | Verified in source presentation |
| SHA1 | `ebef2bdc6329563ccf85769c3e5b8ceca852992b` | Verified in source presentation |

## Suspicious Executable

| Artifact | Value |
|---|---|
| File | `Magnify.exe` |
| Suspected identity | `cmd.exe` / command interpreter substitution |
| SHA-256 | `0B9BC863E2807B6886760480083E51BA8A66118659F4FF274E7B73944D2219F5` |
| VirusTotal result | Identified as `Cmd.Exe`; project screenshot showed no malicious detections |
| Forensic significance | File substitution / masquerading evidence, not malware detection by itself |

## Important Limitation

The project materials do not retain every artifact export hash, source media identifier, or full chain-of-custody log. The report records this as a limitation and avoids unsupported claims about initial access vector, attacker identity, or exfiltration.
