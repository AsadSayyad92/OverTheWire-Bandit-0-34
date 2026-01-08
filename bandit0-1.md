# OverTheWire Bandit — Level 0 → Level 1

## 🎯 Objective

Retrieve the password for the next level by exploring files in the home directory using basic Linux commands.

---

## 🧠 Hint Provided by Bandit

> The password for the next level is stored in a file called **readme** located in the home directory.

---

## 🛠️ Approach

Based on the hint:

* List files in the home directory
* Identify the file mentioned in the hint
* Read the contents of that file

---

## 🧾 Commands Used

```bash
ls
cat readme
```

---

## 📝 Explanation

* `ls` was used to list all files in the current directory.
* The file named `readme` was identified.
* `cat readme` displayed the contents of the file.
* The output contained the password for the next level.

---

## 🔎 Result

✔ Successfully obtained the password for **Bandit Level 1**
---

## 📸 Screenshots

Screenshots are stored in the `screenshots/` directory:


> Screenshots do **not** expose passwords.

---

## 🧠 Concepts Learned

* Navigating Linux directories
* Reading files using `cat`
* Following problem hints effectively

---

## ✅ Status

✔ Level 0 → Level 1 completed

---

## ⚠️ Disclaimer

This write-up is for **educational purposes only**.
Sensitive data such as passwords and credentials are intentionally excluded.
