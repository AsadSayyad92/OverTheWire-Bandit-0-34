# OverTheWire Bandit — Level 20 → Level 21

## 🎯 Objective

Retrieve the password for the next level by interacting with a **setuid network client** that communicates with a service over a local port.

---

## 🧠 Our Hint

When a program connects to a service and expects a response, you may need to **simulate the server side** to control the interaction.

---

## 🛠️ Approach

This level provides a setuid binary named `suconnect`.  
The binary:

- Runs with higher privileges
- Connects to a port on `localhost`
- Sends the current password
- Expects the same password in return

To solve this level:

- Start a listening service on a chosen port
- Execute the setuid binary to connect to that port
- Respond correctly to receive the next password

---

## 🧾 Commands Used

```bash
nc -lvp 4444

---

📝 Explanation

A netcat listener was started on port 4444 to act as the server.

The suconnect binary was executed with the same port number.

The binary connected to the listener and sent the current password.

The password was copied and sent back through the same connection.

Upon receiving the correct response, the binary returned the password for the next level.

---

🧠 Concepts Learned

Client–server interaction

Using netcat as a listener

Exploiting setuid binaries

Understanding authentication over sockets

