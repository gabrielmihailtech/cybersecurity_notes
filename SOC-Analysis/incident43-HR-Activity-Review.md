Incident 43 - HR Activity Review

Suspicious IPs:

None identified

Attack Type:

Insider Activity Review
Potential False Positive

Findings:

User hr_manager logged in from internal IP 10.0.0.15.
Access observed to:
/employees
/payroll
/departments
/logs
Export functionality was used multiple times.
No external IP addresses or authentication anomalies were observed.

Timeline:

HR manager logged into the system.
Employee and payroll data were accessed.
Multiple export operations were performed.
Department information was accessed.
Log resources were reviewed.

MITRE ATT&CK:

Valid Accounts
Data Staged

Conclusion:

The observed activity is largely consistent with normal HR responsibilities. Multiple export operations were identified, but there is insufficient evidence to conclude malicious activity.
Verification of exported data would be required to assess whether any sensitive information was accessed outside of normal business operations.
