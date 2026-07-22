Incident 31 - Concurrent Account Compromise and Brute Force

Suspicious IPs:

192.168.1.60
192.168.1.90
192.168.1.180
192.168.1.220

Attack Type:

Active Scanning
Brute Force
Account Compromise
Lateral Movement
Persistence
Post-Exploitation

Findings:

192.168.1.60 performed reconnaissance activity through requests to test and admin resources.
192.168.1.90 successfully compromised the admin account through brute-force authentication attempts.
192.168.1.180 accessed the david account from an unusual external IP.
The same IP later accessed the admin account, indicating lateral movement.
The attacker returned to the david account, demonstrating persistence.
Sensitive resources accessed:
/dashboard
/config
/backup
/logs
/download

Timeline:

Normal activity observed from user david.
Scanning activity detected from 192.168.1.60.
David account accessed from external IP 192.168.1.180.
Successful brute-force compromise of the admin account by 192.168.1.90.
Lateral movement, persistence and access to sensitive resources observed from 192.168.1.180.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Lateral Movement
Persistence

Conclusion:

Multiple malicious activities were identified during the investigation. The most significant impact originated from 192.168.1.180, which demonstrated account compromise, lateral movement,
persistence and access to sensitive resources, creating a substantial risk of system compromise and data exposure.
