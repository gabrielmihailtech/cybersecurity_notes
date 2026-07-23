Incident 38 - Potential Data Collection Activity

Suspicious IPs:

192.168.1.175
192.168.1.80

Attack Type:

Account Compromise
Potential Data Collection
Privilege Escalation

Findings:

User emily accessed from an external IP address.
Access observed to:
/users
/reports
/export
Admin account accessed from the same IP.
Access to:
/config
/logs
/export
Scanning activity observed from 192.168.1.80.

Timeline:

Emily account accessed from an external IP.
Reports and user-related resources accessed.
Export functionality used.
Admin account accessed.
Export functionality accessed again.

MITRE ATT&CK:

Valid Accounts
Discovery
Privilege Escalation
Data Staged

Conclusion:

The activity is consistent with information gathering and potential data collection.
Although export functionality was accessed multiple times, the available evidence is insufficient to confirm successful data exfiltration.
