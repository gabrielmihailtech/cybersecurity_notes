# Traffic Analysis Essentials

## 🧠 Overview
Traffic analysis involves monitoring and analyzing network activity to detect abnormal or malicious behavior.

---

## 🔑 Key Concepts

- Traffic → data moving between devices over a network
- Packet → small unit of data transmitted
- Source IP → sender of the traffic
- Destination IP → receiver of the traffic
- Destination Port → service being accessed

---

## 🚦 Normal vs Suspicious Traffic

### ✅ Normal Traffic
- Regular web browsing
- Limited number of requests
- Predictable patterns

### ❌ Suspicious Traffic
- High number of repeated requests
- Connections to unusual ports
- Random or non-existent URLs
- Traffic from flagged IP addresses

---

## 🔎 Traffic Analysis Process

1. Identify suspicious IP addresses
2. Correlate with alerts (IDS/IPS)
3. Analyze traffic patterns
4. Identify associated ports
5. Apply filtering or blocking

---

## 🚨 Practical Lab Insights

In this lab:
- Malicious IPs were identified using alerts and visual indicators
- Destination ports were analyzed from traffic logs
- Only ports linked to malicious activity were selected for filtering

---

## ⚠️ Security Relevance

- Attackers generate abnormal traffic patterns
- Monitoring network traffic helps detect:
  - brute force attacks
  - scanning activity
  - exploitation attempts

---

## 🛡️ SOC Perspective

- Monitor traffic logs and patterns
- Identify anomalies based on behavior
- Correlate alerts with network activity
- Apply filtering rules to mitigate threats

---

## 📝 Notes

- Not all suspicious traffic is malicious
- Prioritize confirmed threats (alerts, patterns)
- Visual indicators (like flags or alerts) are critical in analysis

---

## 🧪 Commands Used (Basic)

grep → search for patterns in logs  
cat → display file content  
tail → monitor logs in real time  

---

## ✅ Summary
Traffic analysis is critical for detecting and understanding cyber attacks. By analyzing patterns, identifying suspicious activity, and correlating data, SOC analysts can detect and respond to threats effectively.
