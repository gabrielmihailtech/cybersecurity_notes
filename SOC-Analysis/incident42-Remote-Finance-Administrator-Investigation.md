Incident 42 - Remote Finance Administrator Investigation

Suspicious IPs:

192.168.1.120
192.168.1.50

Attack Type:

Account Activity Review
Potential Account Compromise
Potential Data Export

Findings:

User finance_admin accessed resources from the internal IP 10.0.0.5.
The same account was later used from 192.168.1.120.
Resources accessed from the second IP:
/customers
/export
/backup
/logs
Additional 404 activity observed from 192.168.1.50.

Timeline:

Normal finance administrator activity observed from an internal IP.
The same account was later accessed from a different IP address.
Customer information resources were accessed.
Export and backup functionality were used.
Log resources were accessed from the same session.

MITRE ATT&CK:

Valid Accounts
Data Staged
Potential Account Abuse

Conclusion:

The observed activity may represent legitimate remote administration or unauthorized use of the finance administrator account.
Access to customer, export and backup resources from a secondary IP address increases suspicion, but further investigation is required to determine whether sensitive data was exported.
