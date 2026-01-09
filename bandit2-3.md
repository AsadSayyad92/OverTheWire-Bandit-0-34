# OverTheWire Bandit — Level 2 → Level 3

## 🎯 Objective

Retrieve the password for the next level from a file whose name contains **spaces**.

---

## 🧠 Hint

Files with spaces in their names must be handled carefully, either by **escaping spaces** or **wrapping the filename in quotes**.

---

## 🛠️ Approach

The challenge in this level is that the filename contains spaces, which can break commands if not handled correctly.

To solve this:

* Identify the file with spaces in its name
* Use a proper method to read such a file without errors

---

## 🧾 Commands Used

```bash
ls
cat "spaces in this filename"
```

---

## 📝 Explanation

* `ls` was used to list all files in the directory.
* A file named `spaces in this filename` was identified.
* Because the filename contains spaces, it was enclosed in double quotes.
* Quoting the filename ensures the shell treats it as a single argument.
* The `cat` command then displayed the contents of the file.
* The output revealed the password for the next level.

---

## 🔎 Result

✔ Successfully obtained the password for **Bandit Level 3**

---

## 📸 Screenshots

Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

## 🧠 Concepts Learned

* Handling filenames with spaces
* Proper use of quotes in Linux commands
* Understanding how the shell parses command arguments

---

## ✅ Status

✔ Level 2 → Level 3 completed

