Incident 34 - Potential Data Exfiltration Activity

Suspicious IPs:

192.168.1.210
192.168.1.60

Attack Type:

Account Compromise
Privilege Escalation
Data Collection
Potential Data Exfiltration

Findings:

User sarah account accessed from an external IP.
Access to:
/customers
/reports
Administrative access observed from the same IP.
Access to:
/backup
/export
/download
Return access to the sarah account was observed.
Logs were subsequently accessed.

Timeline:

Sarah account accessed from external IP.
Customer and reporting resources accessed.
Administrative account accessed.
Backup, export and download functionality used.
Continued activity observed on the compromised account.

MITRE ATT&CK:

Valid Accounts
Data from Information Repositories
Data Staged
Exfiltration

Conclusion:

The observed activity is consistent with data collection and potential data exfiltration. 
Access to export and download functionality following administrative access represents the highest risk observed during the investigation.
