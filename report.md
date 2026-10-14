# Windows 11 Vulnerability Assessment Report

## 1. Scope
The assessment targeted a Windows 11 virtual machine at `192.168.100.4` using Nessus Essentials running on Kali Linux at `192.168.100.5`.

## 2. Methodology
1. Configured the Windows 11 target in Nessus.
2. Selected the Advanced Scan policy.
3. Executed the scan.
4. Reviewed severity ratings, plugin descriptions, output, and remediation guidance.
5. Recorded screenshots as evidence.

## 3. Findings Summary

| Finding | Severity | Result |
|---|---|---|
| ICMP Timestamp Request Remote Date Disclosure | Low | Detected |
| SMB service information | Informational | Detected |
| WMI Not Available | Informational | Detected |
| OS Security Patch Assessment Failed | Informational | Assessment limitation |
| Administrative share access denied | Informational | Authentication limitation |

## 4. Key Observation
The scan identified one Low-severity issue and several Informational results. The patch assessment could not be completed because Nessus lacked access to certain Windows resources.

## 5. Recommendations
- Restrict unnecessary ICMP timestamp traffic.
- Review SMB exposure and share permissions.
- Ensure Windows is fully updated.
- Configure authorized administrative credentials for authenticated scanning.
- Repeat the scan after resolving access limitations.

## 6. Conclusion
The lab demonstrated vulnerability scanning, service discovery, plugin analysis, severity classification, and remediation documentation. Results are preliminary because authenticated patch assessment was incomplete.

## 7. Evidence
See the `screenshots/` directory for scan results and finding details.
