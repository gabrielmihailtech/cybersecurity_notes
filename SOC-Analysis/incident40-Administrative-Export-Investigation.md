Incident 40 - Administrative Export Investigation

Suspicious IPs:

192.168.1.210
192.168.1.70

Attack Type:

Account Compromise
Internal Reconnaissance
Privilege Escalation
Potential Data Export

Findings:

User lisa accessed from an external IP address.
Resources accessed:
/users
/departments
/reports
Admin account accessed from the same IP.
Administrative resources accessed:
/config
/backup
/logs
Export functionality accessed twice.
Additional 404 activity observed from 192.168.1.70.

Timeline:

Normal activity observed from lisa.
Lisa account accessed from an external IP.
User and department information collected.
Admin account accessed.
Backup and export functionality accessed.

MITRE ATT&CK:

Valid Accounts
Discovery
Privilege Escalation
Data Staged

Conclusion:

The activity indicates unauthorized access to both lisa and admin accounts.
Access to organizational information, backup resources and repeated export operations suggests potential preparation for data extraction, 
although successful exfiltration cannot be confirmed from the available logs.
