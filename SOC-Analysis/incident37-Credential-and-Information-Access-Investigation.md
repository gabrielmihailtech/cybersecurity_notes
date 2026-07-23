Incident 37 - Credential and Information Access Investigation

Suspicious IPs:

192.168.1.150
192.168.1.80

Attack Type:

Account Compromise
Credential Access
Internal Reconnaissance
Privilege Escalation

Findings:

User peter accessed from an external IP.
Access observed to:
/users
/servers
/passwords
Admin account accessed from the same IP.
Additional resources accessed:
/network
/secrets
/export
Re-access to the peter account observed.
404 reconnaissance activity observed from 192.168.1.80.

Timeline:

Peter account accessed from an external IP.
User and server information accessed.
Password-related resources accessed.
Admin account accessed.
Secret and export resources accessed.

MITRE ATT&CK:

Valid Accounts
Credential Access
Discovery
Privilege Escalation

Conclusion:

The attacker demonstrated interest in credential-related resources and internal infrastructure information.
Subsequent access to secrets and export functionality may indicate preparation for further compromise or potential data extraction.
