# OverTheWire Bandit — Level 27 → Level 28

## 🎯 Objective

Retrieve the password for the next level by **cloning a Git repository over SSH** and inspecting its contents.

---

## 🧠 Our Hint

Sensitive information is sometimes stored in **version control systems**.  
Cloning a repository and reviewing its files can reveal exposed credentials.

---

## 🛠️ Approach

In this level, access is provided to a Git repository hosted on the Bandit server.

To solve this level:

- Clone the Git repository using SSH
- Navigate into the repository
- Inspect files to locate the password for the next level

---

## 🧾 Commands Used

```bash
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
cd repo
cat README

---

📝 Explanation

The git clone command was used to clone the remote repository over SSH.

Port 2220 was explicitly specified, as Bandit does not use the default SSH port.

After cloning, the repository contents were inspected.

The README file contained the password for the next level in plain text.

This exposed password was used to proceed to the next Bandit level.

---

🧠 Concepts Learned

Using Git over SSH

Working with non-standard SSH ports

Inspecting repositories for sensitive information

Risks of storing credentials in version control systems


