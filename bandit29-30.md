# OverTheWire Bandit — Level 29 → Level 30

## 🎯 Objective

Retrieve the password for the next level by **exploring different Git branches** in a repository.

---

## 🧠 Our Hint

Sometimes sensitive information is not in the main branch.  
Checking **all available branches** can reveal hidden or unfinished work.

---

## 🛠️ Approach

The Git repository cloned in the previous level does not contain the password in the current branch.

To solve this level:

- List all available Git branches
- Switch to other branches
- Inspect files in each branch
- Locate the password

---

## 🧾 Commands Used

```bash
cd repo
git branch -a
git checkout <branch-name>
cat README

---

📝 Explanation

git branch -a was used to list all local and remote branches.

Besides the default branch, other branches were available.

Each branch was checked out one by one using git checkout.

One of the branches contained a README file with the password.

This password was used to proceed to the next Bandit level.

---

🧠 Concepts Learned

Git branches and their purpose

Switching between branches

Risks of storing secrets in non-main branches

Repository enumeration techniques
