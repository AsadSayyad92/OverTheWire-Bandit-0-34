
```md
# OverTheWire Bandit — Level 32 → Level 33

## 🎯 Objective

Retrieve the password for the next level by **escaping a restricted shell that only allows uppercase commands**.

---

## 🧠 Our Hint

If input is transformed or restricted, you may be able to **bypass it by executing commands indirectly**.

---

## 🛠️ Approach

In this level, the shell converts all input to uppercase, making normal command execution impossible.

To solve this level:

- Understand how the shell processes input
- Use command substitution to bypass the restriction
- Spawn a normal shell
- Read the password file

---

## 🧾 Commands Used

```bash
$0
/bin/bash
cat /etc/bandit_pass/bandit33

---

📝 Explanation

The shell transformed all typed commands into uppercase.

Typing $0 executed the current shell binary directly.

This bypassed the uppercase restriction and spawned a normal shell.

With a proper shell available, standard commands could be executed.

The password file for the next level was read successfully.

---

🧠 Concepts Learned

Restricted shell behavior

Command substitution and shell variables

Shell escaping techniques

Bypassing input sanitization


