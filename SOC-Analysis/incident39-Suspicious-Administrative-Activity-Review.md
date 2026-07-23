Incident 39 - Suspicious Administrative Activity Review

Suspicious IPs:

192.168.1.200
192.168.1.70

Attack Type:

Account Compromise
Administrative Resource Access

Findings:

User david accessed from an external IP.
Access observed to:
/profile
/reports
/export
Admin account accessed from the same IP.
Access to:
/logs
/reports
Additional 404 activity observed from 192.168.1.70.

Timeline:

Normal activity observed from david.
David account accessed from an external IP.
Reporting resources accessed.
Export functionality accessed.
Admin account accessed from the same IP.

MITRE ATT&CK:

Valid Accounts
Discovery
Privilege Escalation

Conclusion:

The same external IP accessed both david and admin accounts and interacted with reporting and export resources. 
The activity may indicate unauthorized access and potential data collection, although further investigation is required to determine impact.
