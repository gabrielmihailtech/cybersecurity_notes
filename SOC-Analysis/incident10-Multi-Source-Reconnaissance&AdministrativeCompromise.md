Incident 10 - Multi-Source Reconnaissance and Administrative Compromise
Suspicious IPs:

192.168.1.10
192.168.1.30
192.168.1.40

Attack Type:

Active Scanning
Brute Force
Account Compromise
Post-Exploitation

Findings:

Multiple scanners identified:

192.168.1.30
192.168.1.40


Multiple failed login attempts targeting the admin account
Successful admin authentication from 192.168.1.10
Access to:

/dashboard
/config
/backup
/logs
/download


Failed root authentication attempt from 192.168.1.20

Timeline:

Scanning activity detected from multiple IP addresses
Repeated authentication failures against admin
Successful administrative compromise
Access to privileged resources
Download functionality accessed

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Multiple reconnaissance activities were identified alongside a successful brute-force attack against the admin account.
The attacker proceeded to access several sensitive resources, including download functionality, indicating potential data collection or exfiltration activity.
