Incident 54 - Incomplete Evidence Administrative Access Investigation

---
Suspicious IPs:

192.168.1.150

---
Attack Type:

Potential Account Compromise
Privileged Access Abuse
Potential Data Collection
Incomplete Evidence Investigation

---
Findings:

User finance_user normally logged in from internal IP 10.0.0.22.
The same account later logged in from 192.168.1.150.
Resources accessed from 192.168.1.150:
/reports
/finance
/export
The admin account was subsequently accessed from the same IP address.
Administrative resources accessed:
/config
The connection from 192.168.1.150 was lost shortly after administrative access.
Later, an internal administrator session from 10.0.0.5 accessed:
/logs
/reports

---
Timeline:

08:15 – Normal finance_user login observed from internal IP 10.0.0.22.
08:20 – finance_user logged in from 192.168.1.150.
08:21 - 08:25 – Finance-related resources and export functionality were accessed.
08:30 - 08:31 – The admin account accessed configuration resources from the same IP.
08:35 – Connection from 192.168.1.150 was lost.
11:00 - 11:02 – Internal administrator reviewed logs and reports.

---
MITRE ATT&CK:

Valid Accounts
Data Collection
Account Discovery
Potential Privilege Escalation
Potential Data Exfiltration

---
Conclusion

The activity from 192.168.1.150 raises concern due to access to finance-related resources, export functionality, and subsequent administrative account usage from the same IP address.
However, the available evidence is incomplete because the connection was lost shortly after administrative access and no download, backup, or additional post-compromise actions were observed.
While the activity is consistent with a potential account compromise and unauthorized data collection, the logs do not provide sufficient evidence to confirm that sensitive data was successfully exfiltrated. 
Further investigation should focus on determining what data was included in the export operation and the reason for the unexpected connection loss. 👊
