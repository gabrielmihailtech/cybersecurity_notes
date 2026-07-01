Incident 05 - Reconnaissance Followed by Admin Compromise
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise

Findings:

192.168.1.30 performed repeated requests to administrative and test endpoints
Multiple failed login attempts were performed by 192.168.1.10
Successful admin authentication observed
Access to:

/dashboard
/config
/backup


Failed root login attempt from 192.168.1.20

Timeline:

Reconnaissance activity detected from 192.168.1.30
Repeated failed admin login attempts
Admin account compromise
Access to privileged resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
Reconnaissance activity was observed prior to a successful brute-force attack against the admin account.
Following compromise, the attacker accessed sensitive resources, creating a potential risk of data exposure and further system compromise.
