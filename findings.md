# Nessus Findings and Remediation

## Finding 1: ICMP Timestamp Request Remote Date Disclosure
- Severity: Low
- Plugin ID: 10114
- CVSS v2: 2.1
- Port: ICMP

**Risk:** May disclose information about the target's system clock.

**Remediation:** Filter unnecessary ICMP timestamp requests (type 13) and replies (type 14).

## Finding 2: SMB Service Information
- Severity: Informational
- Ports: TCP 139 and TCP 445

**Observation:** SMB services and related system information were detected.

**Remediation:** Restrict SMB access to trusted hosts, disable SMBv1 if enabled, and review share permissions.

## Finding 3: WMI Not Available
- Severity: Informational

**Observation:** Nessus could not access the remote WMI namespace.

**Remediation:** Review firewall rules and remote-management permissions if WMI assessment is required.

## Finding 4: OS Security Patch Assessment Failed
- Severity: Informational

**Observation:** Nessus could not complete patch checks because required remote registry and system information were unavailable.

**Remediation:** Configure authorized administrative credentials and the necessary remote access permissions, then repeat the scan.

## Finding 5: Administrative Share Access Denied
- Severity: Informational

**Observation:** Nessus authenticated through SMB but could not access the `ADMIN$` share.

**Remediation:** Verify that the authorized scan account has the required administrative privileges and remote access permissions.
