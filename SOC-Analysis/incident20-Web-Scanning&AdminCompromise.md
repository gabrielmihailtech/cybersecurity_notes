Incident 20-Web Scanning and Admin Compromise
Suspicious IPs:

192.168.1.50
192.168.1.60

Attack Type:

Brute Force
Web Scanning

Findings:

Repeated 404 requests from 192.168.1.60
Multiple failed logins from 192.168.1.50
Successful admin login
Access to privileged endpoints

Timeline:

Web scanning activity observed
Multiple failed login attempts
Successful authentication
Access to sensitive resources

MITRE ATT&CK:

Brute Force
Valid Accounts
Active Scanning

Conclusion:
The primary threat originated from 192.168.1.50, which successfully compromised the admin account. Scanning activity from 192.168.1.60 may have supported reconnaissance efforts.
