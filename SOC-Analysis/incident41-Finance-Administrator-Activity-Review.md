Incident 41 - Finance Administrator Activity Review

Suspicious IPs:

192.168.1.50

Attack Type:

Administrative Activity Review
Potential False Positive

Findings:

User finance_admin logged in from internal IP address 10.0.0.5.
Access observed to:
/dashboard
/reports
/customers
/export
The same user later accessed:
/backup
/logs
/export
Additional 404 requests observed from 192.168.1.50.

Timeline:

Finance administrator logged in from an internal IP address.
Reporting and customer resources were accessed.
Export functionality was used.
Backup and logging resources were accessed.
Export functionality was used again.

MITRE ATT&CK:

Valid Accounts
Data Staged

Conclusion:

Although export and backup resources were accessed, all activity originated from a known internal account and IP address.
The observed behavior is consistent with legitimate administrative activity, although verification of exported data would be recommended to rule out misuse.
