# OverTheWire Bandit — Level 28 → Level 29

## 🎯 Objective

Retrieve the password for the next level by **analyzing Git commit history** to uncover sensitive information removed from the latest version.

---

## 🧠 Our Hint

Even if sensitive data is deleted from a file, **version control history still remembers it**.  
Reviewing commits can reveal previously exposed secrets.

---

## 🛠️ Approach

The repository cloned in the previous level does not show the password in the latest version.

To solve this level:

- Inspect the Git commit history
- Identify earlier commits
- View file contents from previous commits
- Extract the password from the commit history

---

## 🧾 Commands Used

```bash
cd repo

---

📝 Explanation

git log was used to list all commits in the repository.

An earlier commit message indicated changes related to sensitive information.

git show was used to inspect the contents of that commit.

The password for the next level was present in the file content of a previous commit.

This demonstrates how secrets can remain accessible even after being removed.

---

🧠 Concepts Learned

Git commit history analysis

Recovering deleted data from version control

Importance of secret management

Risks of committing sensitive data


