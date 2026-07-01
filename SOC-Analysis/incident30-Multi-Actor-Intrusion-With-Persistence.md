Incident 30 - Multi-Actor Intrusion With Persistence
Suspicious IPs:

192.168.1.30
192.168.1.100
192.168.1.150
192.168.1.220

Attack Type:

Active Scanning
Brute Force
Account Compromise
Lateral Movement
Persistence
Post-Exploitation

Findings:

192.168.1.30 performed reconnaissance activity through repeated requests to test endpoints.
192.168.1.100 successfully compromised the admin account through brute-force authentication attempts.
192.168.1.150 accessed the john account from an unusual external IP address.
The same IP later accessed the admin account, indicating lateral movement.
The attacker returned to the john account, demonstrating persistence.
Sensitive resources accessed:

/dashboard
/config
/backup
/logs
/download



Timeline:

Normal activity observed from user john.
Scanning activity detected from 192.168.1.30.
Successful brute-force compromise of the admin account by 192.168.1.100.
User john account accessed from external IP 192.168.1.150.
Lateral movement to the admin account followed by persistence and access to sensitive resources.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Lateral Movement
Persistence

Conclusion:
Multiple attackers were observed during the investigation. The highest impact was caused by 192.168.1.150, which performed account compromise, lateral movement,
persistence and access to sensitive resources, creating a significant risk of system compromise and potential data exfiltration.
