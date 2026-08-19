Incident 46 - Elevated Risk of Data Exfiltration

Suspicious IPs:

192.168.1.180
192.168.1.60

Attack Type:

Account Activity Review
Potential Data Collection
Potential Data Exfiltration

Findings:

User sales_manager normally accessed the system from internal IP 10.0.0.20.
The same account was later used from 192.168.1.180.
Resources accessed:
/customers
/sales
/reports
/backup
/logs
Export functionality was used twice.
Download functionality was used twice.
Additional scanning activity observed from 192.168.1.60.

Timeline:

Sales manager logged in from an internal IP address.
The account was later accessed from a secondary IP.
Customer and sales-related resources were accessed.
Export and download operations were repeatedly performed.
Backup and log resources were reviewed.

MITRE ATT&CK:

Valid Accounts
Data Staged
Exfiltration Over Web Services (Potential)

Conclusion:

The observed activity is more suspicious than previous sales manager activity due to repeated export and download operations combined with access to backup resources. While data exfiltration cannot be confirmed from the available logs, the evidence suggests a higher risk of unauthorized data collection and potential export of sensitive business information.
Further investigation should focus on determining the contents of the exported and downloaded data.
