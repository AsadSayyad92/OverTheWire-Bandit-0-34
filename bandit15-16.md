# OverTheWire Bandit — Level 15 → Level 16

## 🎯 Objective

Retrieve the password for the next level by **sending the current password to a service that uses SSL/TLS encryption**.

---

## 🧠 Our Hint

When a service uses encryption, tools like `nc` are not enough.  
You must use a client that understands **SSL/TLS** communication.

---

## 🛠️ Approach

In this level, the password is not stored in a file.  
Instead, a service is running on **port 30001** that expects an **encrypted connection**.

To solve this level:

- Establish a secure SSL/TLS connection to the service
- Send the current level’s password
- Read the encrypted response returned by the server

---

## 🧾 Commands Used

```bash
openssl s_client -connect localhost:30001

---

📝 Explanation

openssl s_client was used to establish a secure SSL/TLS connection.

The -connect option specifies the target host and port.

Once the connection was established, the current password was manually entered.

The server responded with a string.

This string is the password for the next Bandit level.


---

🧠 Concepts Learned

Secure communication using SSL/TLS

Difference between encrypted and unencrypted services

Using OpenSSL as a client

Manual interaction with secure network services


