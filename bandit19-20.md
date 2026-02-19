# OverTheWire Bandit — Level 19 → Level 20

## 🎯 Objective

Retrieve the password for the next level by **abusing a setuid binary** that runs with higher privileges.

---

## 🧠 Our Hint

When a binary has the **setuid** bit set, it executes with the permissions of its owner.  
Such binaries can often be used to access restricted files.

---

## 🛠️ Approach

In this level, a binary named `bandit20-do` is present in the home directory.  
This binary runs commands **as another user**.

To solve this level:

- Identify the setuid binary
- Use it to execute a command as the next user
- Read the password file for the next level

---

## 🧾 Commands Used

```bash
ls -l

---

📝 Explanation

ls -l was used to inspect file permissions.

The binary bandit20-do has the setuid bit enabled.

When executed, it runs commands with the privileges of user bandit20.

By using the binary to run cat on the password file, access to the restricted file was granted.

The output contained the password for the next level.

---

🧠 Concepts Learned

Understanding setuid permissions

Privilege escalation via misconfigured binaries

Executing commands as another user

Linux file permission inspection

