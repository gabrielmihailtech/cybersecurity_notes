Incident 49 - Multi-Stage Account Activity Investigation

Suspicious IPs:

192.168.1.90
192.168.1.200
192.168.1.40
192.168.1.60

Attack Type:

Active Scanning
Brute Force
Account Compromise
Potential Data Collection

Findings:

Reconnaissance activity identified from:
192.168.1.40
192.168.1.60
Multiple failed login attempts against the admin account originated from 192.168.1.90.
Successful authentication to the admin account was later observed from the same IP.
User analyst was accessed from 192.168.1.200.
Resources accessed:
/projects
/reports
/export
The same IP later accessed administrative resources including:
/config
/download

Timeline:

Normal analyst activity observed.
Scanning activity detected from multiple IP addresses.
Repeated failed authentication attempts targeted the admin account.
Administrative access was successfully obtained.
Sensitive project and reporting resources were accessed, followed by export and download activity.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Data Collection
Potential Data Exfiltration

Conclusion:

Multiple suspicious activities were observed during the investigation.
While several IP addresses were involved in reconnaissance and credential attacks, the highest potential impact was associated with access to project and reporting resources, 
combined with export and download activity. Further investigation should determine whether sensitive data was exported or downloaded from the environment.
