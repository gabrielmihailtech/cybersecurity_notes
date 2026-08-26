Incident 50 - Correlated Administrative And Data Access Activity

Suspicious IPs:

192.168.1.40
192.168.1.60
192.168.1.90
192.168.1.220

Attack Type:

Active Scanning
Brute Force
Account Compromise
Potential Data Collection
Potential Data Exfiltration

Findings:

Scanning activity observed from:
192.168.1.40
192.168.1.60
Multiple failed admin authentication attempts originated from 192.168.1.90.
Successful admin authentication was later observed from the same IP.
User analyst was accessed from 192.168.1.220.
Resources accessed from 192.168.1.220:
/projects
/reports
/export
/download
The same IP later accessed the admin account and visited:
/backup
/logs
Administrative resources were also accessed from 192.168.1.90:
/config

Timeline:

Normal analyst activity observed.
Reconnaissance activity detected from multiple external IPs.
Repeated failed authentication attempts targeted the admin account.
Administrative access was successfully obtained.
Export, download, backup and log resources were accessed through privileged accounts.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Data Collection
Potential Data Exfiltration

Conclusion:

The incident contains two significant investigative tracks: a successful administrative account compromise originating from 192.168.1.90 and access to sensitive project resources from 192.168.1.220.
While data exfiltration cannot be confirmed from the available logs, export, download and backup activity performed after privileged access increases concern regarding potential unauthorized access 
to sensitive information. Additional investigation should focus on determining whether exported or downloaded data contained critical organizational assets.


