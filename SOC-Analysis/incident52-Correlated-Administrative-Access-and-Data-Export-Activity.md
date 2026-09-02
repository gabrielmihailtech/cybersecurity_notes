Incident 52 - Correlated Administrative Access and Data Export Activity

Suspicious IPs:

192.168.1.55
192.168.1.60
192.168.1.85
192.168.1.240

Attack Type:

Active Scanning
Brute Force
Account Compromise
Privileged Access Abuse
Potential Data Collection
Potential Data Exfiltration

Findings:

Reconnaissance activity was observed from:
192.168.1.55
192.168.1.60
Multiple failed authentication attempts against the admin account originated from 192.168.1.85.
Successful authentication to the admin account was later observed from the same IP.
Administrative resources accessed from 192.168.1.85:
/admins
/config
User operations_user was accessed from 192.168.1.240.
Resources accessed from 192.168.1.240:
/tasks
/clients
/export
The same IP later accessed the admin account and visited:
/backup
/download

Timeline:

Normal operations user activity was observed from an internal IP address.
Reconnaissance activity targeted administrative resources.
The operations_user account was accessed from 192.168.1.240.
Operational and client-related resources were accessed and export functionality was used.
A successful brute-force attack against the admin account occurred from 192.168.1.85.
Administrative resources were accessed from both 192.168.1.85 and 192.168.1.240.
Backup and download operations were performed through privileged access.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Account Discovery
Data Collection
Potential Data Exfiltration

Conclusion:

The incident contains multiple suspicious activities occurring simultaneously. While 192.168.1.85 successfully compromised the admin account through brute-force authentication attempts,
the highest-risk activity originated from 192.168.1.240, where operational and client-related resources were accessed, export functionality was used, and privileged administrative resources were later accessed.
Although unauthorized data exfiltration cannot be confirmed from the available logs, the combination of export, download,
backup and administrative access significantly increases the risk of unauthorized data collection.
Further investigation should focus on identifying the contents of the exported and downloaded files and determining whether the activities from 192.168.1.85 and 192.168.1.240 are related. 👊
