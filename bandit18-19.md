# OverTheWire Bandit — Level 18 → Level 19

## 🎯 Objective

Log in to the server and retrieve the password for the next level **despite a forced logout command** that runs immediately after login.

---

## 🧠 Our Hint

When a shell executes a command automatically on login, you can often **override it by executing your own command directly via SSH**.

---

## 🛠️ Approach

In this level, logging in normally immediately logs the user out due to a command executed on login.

To solve this level:

- Bypass the default shell behavior
- Execute a command directly during the SSH login
- Read the password file for the next level

---

## 🧾 Commands Used

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat /etc/bandit_pass/bandit19

---

📝 Explanation

Normally, logging in as bandit18 immediately logs the user out.

SSH allows execution of a command directly during login.

By specifying cat /etc/bandit_pass/bandit19 in the SSH command, the server executes it before the forced logout.

The output of this command reveals the password for the next level.

---

🧠 Concepts Learned

Executing commands directly over SSH

Bypassing restricted login shells

Understanding login scripts and shell initialization

Remote command execution techniques
