Incident 47 - Multi-Source Administrative Compromise

Suspicious IPs:

192.168.1.50
192.168.1.60
192.168.1.80
192.168.1.200

Attack Type:

Active Scanning
Brute Force
Account Compromise
Potential Data Collection

Findings:
Multiple reconnaissance attempts observed from:
192.168.1.50
192.168.1.60
Multiple failed authentication attempts against the admin account from 192.168.1.80.
Successful admin authentication observed from 192.168.1.80.
User marketing_user was accessed from 192.168.1.200.
Resources accessed from 192.168.1.200:
/customers
/reports
/export
The same IP later accessed the admin account and visited:
/config
/download

Timeline:

Normal marketing user activity observed.
Reconnaissance activity detected from multiple IP addresses.
Repeated failed admin authentication attempts occurred.
Administrative access was successfully obtained.
Sensitive resources and export/download functionality were accessed.

MITRE ATT&CK:

Active Scanning
Brute Force
Valid Accounts
Data Collection
Potential Data Exfiltration

Conclusion:

The incident involved multiple malicious activities occurring simultaneously. While several IP addresses were responsible for reconnaissance activity, the highest-risk behavior originated from accounts accessed through 192.168.1.200, where customer data, exports, downloads and administrative resources were accessed. 
Further investigation should focus on the relationship between the administrative compromise and the observed export/download activity.
