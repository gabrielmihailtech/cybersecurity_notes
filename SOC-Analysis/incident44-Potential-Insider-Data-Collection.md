Incident 44 - Potential Insider Data Collection

Suspicious IPs:

None identified

Attack Type:

Insider Activity Review
Potential Insider Misuse

Findings:

User hr_manager logged in from internal IP 10.0.0.15.
Access observed to:
/employees
/payroll
/customers
/finance
/logs
Export functionality was used multiple times.
Resources outside typical HR-related datasets may have been accessed.

Timeline:

HR manager logged into the system.
Employee and payroll resources were accessed.
Multiple export operations were performed.
Customer and finance resources were accessed.
Log resources were reviewed.

MITRE ATT&CK:

Valid Accounts
Data Staged
Potential Collection Activity

Conclusion:

The activity may represent legitimate business operations; however, access to customer and finance resources combined with repeated export activity raises concern regarding potential insider misuse.
Additional investigation is required to determine whether the user was authorized to access and export this information and to identify the contents of the exported data.
