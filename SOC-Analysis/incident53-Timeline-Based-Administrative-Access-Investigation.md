Incident 53 - Timeline-Based Administrative Access Investigation

Suspicious IPs:

192.168.1.175
192.168.1.80

Attack Type:

Account Compromise
Privileged Access Abuse
Data Collection
Potential Data Exfiltration

Findings:

User support_user normally logged in from internal IP 10.0.0.50.
The same account was later accessed from 192.168.1.175.
Resources accessed from 192.168.1.175:
/tickets
/customers
/export
The same IP later accessed the admin account.
Administrative resources accessed:
/config
/download
/logs
Additional reconnaissance activity was observed from 192.168.1.80.

Timeline:

09:00 – Normal support_user login observed from internal IP 10.0.0.50.
09:05-09:07 – support_user accessed ticket and customer-related resources from 192.168.1.175.
11:20 – Export functionality was used from the same IP.
14:45-14:46 – Administrative access and configuration resources were accessed.
16:10-16:12 – Download and log resources were accessed from the same session.

MITRE ATT&CK:

Valid Accounts
Account Discovery
Data Collection
Data Staged
Potential Data Exfiltration

Conclusion:

The activity observed from 192.168.1.175 developed gradually throughout the day, beginning with access to support-related resources, followed by export activity, administrative access,
and later download operations. While the available logs do not confirm data exfiltration, the sequence of customer data access, export functionality usage, privileged account access,
and download activity indicates a significant risk of unauthorized data collection. 
Further investigation should focus on identifying the contents of the exported and downloaded files and determining whether the administrative access was authorized.
