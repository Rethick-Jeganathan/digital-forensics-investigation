# Remediation Recommendations

## Immediate Hardening

- Enforce MFA for privileged accounts.
- Review and reduce local administrator membership.
- Verify integrity of accessibility binaries such as `Magnify.exe`, `sethc.exe`, `utilman.exe`, and `osk.exe`.
- Compare core system executables against known-good hashes.
- Preserve suspicious files and executables with cryptographic hashes.

## Monitoring and Detection

- Alert on unexpected modification of files in `C:\Windows\System32`.
- Monitor use of command interpreters and renamed binaries.
- Centralize Windows event logs, process execution telemetry, and endpoint alerts.
- Track UserAssist, RecentDocs, ShimCache/AppCompatCache, Prefetch, and Amcache during forensic review.

## Incident Response Improvements

- Maintain evidence handling procedures and chain-of-custody records.
- Record acquisition hash, verification hash, source media identifier, and examiner details.
- Build a normalized timeline with confirmed timezone handling.
- Correlate registry findings with event logs, Prefetch, Amcache, SRUM, and network artifacts.
- Document all findings with source path, timestamp, hash, and confidence level.
