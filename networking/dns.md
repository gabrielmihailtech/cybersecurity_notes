# DNS - Domain Name System
DNS translates domain names into IP addresses, allowing users to access websites using human-readable names.

# Key concepts
- Domain- human-readable name (google.com)
- IP Address- numerical address of a server
- Resolver- finds the IP for a domain

# Domain hierarchy
- TLD(Top-level domain)- Ex: .com, .co.uk(Uk), .it(Italy), .ie(Ireland)
- Second-level domain- EX: google.com (the first part before .com is second-level)
- Subdomain- Ex: admin.google.com (that is the first part before the second-level)

# DNS record type
- A record- resolve IPv4
- AAAA record- resolve IPv6
- CNAME record- resolve to another domain name
- MX record- resolve where to send the email
- TXT record- list servers that have the authority to send emails for the current domain

## Security Relevance

- DNS spoofing attacks
- Malicious domains used in phishing

## SOC Perspective

- Monitor DNS queries
- Detect suspicious domains
