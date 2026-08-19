Incident 45 - Potential Remote Data Export Activity

Suspicious IPs:

192.168.1.180
192.168.1.60

Attack Type:

Account Activity Review
Potential Data Collection
Potential Data Export

Findings:

User sales_manager normally accessed the system from internal IP 10.0.0.20.
The same account was later used from 192.168.1.180.
Resources accessed:
/customers
/sales
/reports
Export functionality was used three times.
Download functionality was accessed.
Log resources were reviewed.
Additional scanning activity observed from 192.168.1.60.

Timeline:

Normal sales manager activity observed from an internal IP.
The same account was accessed from a secondary IP address.
Customer, sales and reporting resources were accessed.
Multiple export operations were performed.
Download and log resources were accessed.

MITRE ATT&CK:

Valid Accounts
Data Staged
Potential Data Collection

Conclusion:

The activity may represent legitimate remote work by the sales manager; however, repeated export operations combined with download activity increase the likelihood of data collection.
Additional investigation is required to determine what data was exported and whether the activity was authorized.
