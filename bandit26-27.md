# OverTheWire Bandit — Level 26 → Level 27

## 🎯 Objective

Retrieve the password for the next level by **exploiting a setuid binary** and executing commands with elevated privileges.

---

## 🧠 Our Hint

When a binary has the **setuid bit** enabled and runs as another user, it can sometimes be abused to execute commands with higher privileges.

---

## 🛠️ Approach

In this level, after escaping into a proper shell as `bandit26`, a setuid binary is available that runs commands as `bandit27`.

To solve this level:

- Identify the setuid binary
- Use it to execute a command as `bandit27`
- Read the password file for the next level

---

## 🧾 Commands Used

```bash
ls -l

---

📝 Explanation

The ls -l command was used to inspect file permissions.

A binary named bandit27-do was found with the setuid bit enabled.

This binary allows execution of arbitrary commands as user bandit27.

By using the binary to run cat on the password file, access to the restricted password was obtained.

The output contained the password for the next level.

---

🧠 Concepts Learned

Setuid binaries and privilege escalation

Executing commands as another user

Inspecting file permissions

Security risks of misconfigured executables


