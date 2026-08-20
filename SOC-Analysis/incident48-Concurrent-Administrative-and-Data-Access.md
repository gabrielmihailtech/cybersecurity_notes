Incident 48 - Concurrent Administrative Compromise And Data Access

Suspicious IPs:
192.168.1.40
192.168.1.70
192.168.1.90
192.168.1.210

Attack Type:

Active Scanning
Brute Force
Account Compromise
Potential Data Collection
Potential Data Exfiltration

Findings:

Reconnaissance activity observed from:
192.168.1.40
192.168.1.70
Multiple failed login attempts against the admin account from 192.168.1.90.
Successful authentication to the admin account from 192.168.1.90.
User engineering_user was accessed from 192.168.1.210.
Resources accessed from 192.168.1.210:
/projects
/designs
/export
The same IP later accessed the admin account and used:
/backup
/download
Administrative resources were also accessed from 192.168.1.90:
/admins
/config

Timeline:

Normal engineering user activity observed.
Reconnaissance activity detected from multiple external IPs.
Repeated failed authentication attempts targeted the admin account.
Administrative access was obtained from 192.168.1.90.
Sensitive engineering and administrative resources were accessed, including export, backup and download functions.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Data Collection
Potential Data Exfiltration

Conclusion:

This incident contains two significant investigative tracks: an administrative account compromise originating from 192.168.1.90 and access to engineering resources from 192.168.1.210. While the brute-force activity is clearly malicious, the greatest potential impact may stem from the export, backup and download operations performed through 192.168.1.210. 
Additional investigation is required to determine whether these activities are related and whether sensitive engineering data was exported or downloaded.
