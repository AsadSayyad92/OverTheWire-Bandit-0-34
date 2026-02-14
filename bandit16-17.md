# OverTheWire Bandit — Level 16 → Level 17

## 🎯 Objective

Identify the correct service among multiple open ports and retrieve the password for the next level by establishing a **secure SSL connection**.

---

## 🧠 Our Hint

When multiple services are running, **port scanning** helps identify which ports are open and what type of services they provide.

---

## 🛠️ Approach

In this level, multiple ports are listening on localhost, but only **one port** provides the correct password using **SSL/TLS**.

To solve this level:

- Scan the given port range to identify open ports
- Determine which ports use SSL/TLS
- Connect securely to the correct port
- Submit the current level’s password and capture the response

---

## 🧾 Commands Used

```bash
nmap -p 31000-32000 localhost

---

📝 Explanation

nmap was used to scan ports from 31000 to 32000 on localhost.

The scan revealed multiple open ports.

Each open port was tested using openssl s_client to identify which service used SSL/TLS.

Upon connecting to the correct SSL-enabled port, the current password was entered.

The server responded with a private SSH key.

This SSH key is required to log in to the next Bandit level.

---

🧠 Concepts Learned

Port scanning using nmap

Identifying SSL-enabled services

Secure client-server communication

Extracting sensitive data from network services

Understanding why private keys must be protected

