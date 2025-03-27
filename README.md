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

🔹 Steps Performed:
Initial Request:

Confirmed SQLi injection point on id parameter

Database Enumeration:

Used UNION SELECT to extract:

table_schema, table_name from information_schema.tables

column_name from information_schema.columns

Credential Dump:

Retrieved usernames and password hashes:
' UNION SELECT CONCAT(user, ' ', avatar), password FROM users#


### 🔹 Target URL:
```http
http://dvwa.structreuality.com/vulnerabilities/sqli/?id=#
