Incident 07 - Post-Compromise Administrative Access
Suspicious IPs:

192.168.1.10
192.168.1.30

Attack Type:

Active Scanning
Brute Force
Account Compromise
Post-Exploitation

Findings:

Repeated scanning activity observed from 192.168.1.30
Successful compromise of admin account by 192.168.1.10
Access to:

/dashboard
/config
/logs


Failed login attempt against root account from 192.168.1.20

Timeline:

Scanning activity targeting application resources
Multiple failed login attempts against admin
Successful admin authentication
Access to administrative and logging resources

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts

Conclusion:
An attacker successfully compromised the admin account after multiple authentication failures. 
Following compromise, access to logging resources suggests system enumeration and potential investigation of system activity.
