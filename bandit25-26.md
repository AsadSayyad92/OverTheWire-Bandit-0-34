# OverTheWire Bandit — Level 25 → Level 26

## 🎯 Objective

Retrieve the password for the next level by **escaping a restricted shell** using a pager-based environment.

---

## 🧠 Our Hint

Restricted shells often rely on tools like `more`, `less`, or `vi`.  
These tools can sometimes be **abused to spawn an interactive shell**.

---

## 🛠️ Approach

In this level, a private SSH key for `bandit26` is provided.  
However, logging in using this key drops the user into a restricted environment that immediately exits or prevents command execution.

To solve this level:

- Use the provided SSH private key to log in as `bandit26`
- Force the output to open in a pager (`more`)
- Escape from the pager into an interactive shell
- Read the password for the next level

---

## 🧾 Commands Used

```bash
ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220

---

📝 Explanation

The file bandit26.sshkey contains a private SSH key for the next user.

Logging in normally triggers a restricted shell that prevents interaction.

By resizing the terminal window to a very small size, the login output is forced into a pager (more).

Pressing v opens the content in the vi editor.

From within vi, a new shell is spawned using :shell.

This provides a fully interactive shell as bandit26.

The password for the next level can now be read normally.

---

🧠 Concepts Learned

Escaping restricted shells

Pager abuse (more, vi)

SSH key-based authentication

Living-off-the-land techniques

Real-world privilege escalation methods
