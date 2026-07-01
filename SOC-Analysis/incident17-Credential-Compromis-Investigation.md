Incident 17 – Credential Compromise Investigation
Summary
An attacker performed repeated login attempts against an administrator account and successfully gained access. Additional reconnaissance activity was also identified from separate systems.
Indicators:
Attacker IP:

192.168.1.10

Scanning IPs:

192.168.1.30
192.168.1.40

False Positive:

192.168.1.50

MITRE ATT&CK:

Brute Force
Valid Accounts
Active Scanning

Findings:
The attack originated from IP 192.168.1.10 and resulted in successful authentication. Separate hosts generated repeated 404 requests consistent with scanning activity. Internal users received 403 responses while accessing administrative resources, which was determined to be legitimate behavior.
Conclusion:
A successful credential compromise occurred, followed by access to sensitive resources. Immediate containment and credential reset actions are recommended.
