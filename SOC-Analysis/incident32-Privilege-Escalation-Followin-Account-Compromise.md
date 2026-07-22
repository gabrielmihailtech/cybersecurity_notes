Incident 32 - Privilege Escalation Following Account Compromise

Suspicious IPs

192.168.1.150
192.168.1.60

Attack Type

Account Compromise
Privilege Escalation
Persistence
Internal Reconnaissance
Post-Exploitation

Findings

User mike account was accessed from an external IP address.
Access to:
/profile
/users
The same IP later authenticated as admin.
Access to:
/admin
/config
/backup
The attacker returned to the mike account.
Additional access to:
/logs
/download

Timeline

Normal activity observed from user mike.
Mike account accessed from external IP 192.168.1.150.
Internal resource enumeration observed.
Access to the admin account indicating privilege escalation.
Persistent access and post-exploitation activity observed.

MITRE ATT&CK

Valid Accounts
Privilege Escalation
Persistence
Discovery

Conclusion

An attacker used a compromised user account to gain access to administrative resources. The observed activity indicates privilege escalation, persistence and access to sensitive system resources.
