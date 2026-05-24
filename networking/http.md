# HTTP (Hypertext Transfer Protocol)

## 🧠 Overview
HTTP is a protocol used for communication between a client (browser) and a web server. It is the foundation of data exchange on the web.

---

## 🔑 Key Concepts

- Client → sends request (browser)
- Server → responds with data (website)
- Request → message sent to server
- Response → server's reply

---

## 🌐 How HTTP Works

1. User enters a URL (example: google.com)
2. DNS resolves the domain → IP address
3. Browser sends HTTP request
4. Server processes the request
5. Server sends HTTP response
6. Browser displays the content

---

## 🔢 HTTP Status Codes

- 200 → OK (successful request)
- 404 → Not Found (page does not exist)
- 403 → Forbidden (access denied)
- 500 → Internal Server Error

---

## ⚠️ Security Relevance

- HTTP traffic can be analyzed to detect attacks
- Common attack indicators:
  - repeated failed requests (404)
  - unusual access patterns
  - scanning behavior (multiple URLs)

---

## 🛡️ SOC Perspective

- Monitor HTTP requests and response patterns
- Detect abnormal behavior:
  - high request rate
  - access to sensitive endpoints
- Investigate suspicious traffic for potential attacks

---

## 📝 Notes

- HTTP is not secure (data can be intercepted)
- HTTPS is the secure version (encrypted)
- Many attacks happen at the web layer (XSS, injection)

---

## ✅ Summary

HTTP is essential for web communication and plays a key role in traffic analysis and threat detection in cybersecurity.
