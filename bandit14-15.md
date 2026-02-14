# OverTheWire Bandit — Level 14 → Level 15

## 🎯 Objective

Retrieve the password for the next level by **sending the current level’s password to a service running on a specific port**.

---

## 🧠 Our Hint

Sometimes passwords are not stored in files.  
They may be obtained by **communicating with a network service** running on a local or remote port.

---

## 🛠️ Approach

This level requires interacting with a service running on **port 30000**.

To solve this level:

- Connect to the service using a networking tool
- Observe the server’s response
- Extract the password returned by the service

---

## 🧾 Commands Used

```bash
nc bandit.labs.overthewire.org 30000

---

📝 Explanation

nc (netcat) was used to connect to a TCP service running on port 30000.

Upon connecting, the server immediately returned a string.

This string is the password for the next Bandit level.

The connection closed automatically after sending the response.

---

🧠 Concepts Learned

Communicating with services over TCP

Using netcat as a client

Understanding how services can expose sensitive data

Basic client–server interaction
