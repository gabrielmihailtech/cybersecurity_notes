Incident 35 - Internal Reconnaissance and Environment Discovery

Suspicious IPs:

192.168.1.200
192.168.1.50

Attack Type:

Internal Reconnaissance
Account Compromise
Privilege Escalation
Discovery

Findings:

User michael account accessed from an external IP.
Access to organizational resources:
/users
/departments
/servers
/inventory
The same IP later accessed the admin account.
Additional access to:
/config
/network
/logs
Scanning activity observed from 192.168.1.50.

Timeline:

Michael account accessed from external IP.
Information gathering activity observed.
Administrative access obtained.
Network and configuration resources accessed.
Continued environment enumeration observed.

MITRE ATT&CK:

Discovery
Valid Accounts
Privilege Escalation
Active Scanning

Conclusion:

The attacker demonstrated behavior consistent with internal reconnaissance and environment discovery.
Access to users, servers, network and inventory resources suggests an effort to understand the environment and identify additional targets for future activity.
