Incident 51 - Multi-Source Administrative Access Investigation

Suspicious IPs:

192.168.1.50
192.168.1.70
192.168.1.90
192.168.1.230

Attack Type:

Active Scanning
Brute Force
Account Compromise
Privileged Access Abuse
Potential Data Collection
Potential Data Exfiltration

Findings:

Reconnaissance activity was observed from:
192.168.1.50
192.168.1.70
Multiple failed authentication attempts against the admin account originated from 192.168.1.90.
Successful authentication to the admin account was later observed from the same IP.
User project_manager was accessed from 192.168.1.230.
Resources accessed from 192.168.1.230:
/projects
/clients
/export
The same IP later accessed the admin account and visited:
/config
/backup
/download
/logs

Timeline:

Normal project manager activity was observed from an internal IP address.
Reconnaissance activity targeted administrative resources.
The project_manager account was accessed from 192.168.1.230.
Project and client-related resources were accessed and data export functionality was used.
Administrative resources, backups, downloads and logs were later accessed from the same IP address.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Account Discovery
Data Collection
Potential Data Exfiltration

Conclusion:

The incident contains multiple suspicious activities occurring simultaneously. While 192.168.1.90 successfully compromised the admin account through brute-force attempts,
the highest-risk activity originated from 192.168.1.230, where project and client resources were accessed, data export functionality was used,
and privileged administrative resources were later accessed. Although data exfiltration cannot be confirmed from the available logs, the combination of export, 
download and administrative access indicates a significant risk of unauthorized data collection. 
Further investigation should focus on identifying the contents of the exported and downloaded files and determining whether the administrative access was authorized.
