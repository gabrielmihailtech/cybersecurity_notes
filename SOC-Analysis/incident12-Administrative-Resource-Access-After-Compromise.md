Incident 12 - Administrative Resource Access After Compromise
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise
Post-Exploitation

Findings:

Scanning activity targeting administrative resources
Multiple failed login attempts against admin
Successful compromise of the admin account
Access to:

/dashboard
/config
/backup
/logs
/download



Timeline:

Scanning activity detected
Failed authentication attempts
Successful admin login
Access to privileged resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
An attacker successfully compromised the admin account following multiple failed authentication attempts. Sensitive administrative resources were accessed, increasing the likelihood of system compromise.
