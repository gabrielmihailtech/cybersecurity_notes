Incident 36 - Internal Reconnaissance and Potential Data Export

Suspicious IPs:

192.168.1.240
192.168.1.70

Attack Type:

Account Compromise
Internal Reconnaissance
Privilege Escalation
Potential Data Export

Findings:

User anna was accessed from an external IP address.
The same IP accessed:
/users
/servers
/network
/inventory
The same IP subsequently accessed the admin account.
Access to:
/backup
/export
The same IP later returned to the anna account.
Additional 404 activity observed from 192.168.1.70.

Timeline:

Normal activity observed from the anna account.
Anna account accessed from an external IP.
Internal resources and infrastructure information accessed.
Access escalated to the admin account.
Backup and export resources accessed.

MITRE ATT&CK:

Valid Accounts
Discovery
Privilege Escalation
Data Staged

Conclusion:

The activity indicates unauthorized access to the anna and admin accounts. 
The attacker gathered information about internal resources and later accessed backup and export functionality, suggesting preparation for potential data exfiltration.
