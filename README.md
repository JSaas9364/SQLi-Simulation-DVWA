# SQLi-Simulation-DVWA

This project demonstrates SQL Injection exploitation against a vulnerable web application running DVWA (Damn Vulnerable Web App).  
It walks through enumeration of database metadata and extraction of sensitive user information using UNION-based SQLi techniques.

---

## 📁 Project Structure

SQLi-Simulation-DVWA/<br/>
├── README.md<br/>
├── lamp.png<br/>
├── lampgrep.png<br/>
├── Sqli.png<br/>
├── sqli2.png<br/>

---

## 🛠️ Tools Used

- **DVWA** (target application)
- **Kali Linux** (attacker machine)
- **Burp Suite** / Firefox for crafting payloads
- **Apache2** logs for confirmation

---

## 💥 Attack Walkthrough

### 🔹 Target URL:
```http
http://dvwa.structreuality.com/vulnerabilities/sqli/?id=#
