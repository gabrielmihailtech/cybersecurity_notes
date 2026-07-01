Incident 24- Compromised User Account (John)
Compromised User:
john
Suspicious IP:
192.168.1.50
Attack Type:

Account Compromise

Findings:

Normal login observed from internal IP
Same user later authenticated from external IP
Access to:

/dashboard
/config
/backup
/logs



Timeline:

Normal user activity
Login from unusual external IP
Access to sensitive endpoints
Possible account abuse

MITRE ATT&CK:

Valid Accounts

Conclusion:
The account was likely compromised and used from an unusual location. Sensitive resources were subsequently accessed.
