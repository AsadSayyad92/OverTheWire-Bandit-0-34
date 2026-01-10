# OverTheWire Bandit — Level 4 → Level 5

## 🎯 Objective

Retrieve the password for the next level from a file that is **human-readable**, located among many files.

---

## 🧠 Hint

When multiple files exist, checking the **file type** can help identify which one contains readable text instead of binary data.

---

## 🛠️ Approach

This level contains several files, but only one of them is readable and contains meaningful text.

To solve this:

* Navigate to the given directory
* Inspect each file’s type
* Identify the file that contains readable ASCII text
* Read its contents

---

## 🧾 Commands Used

```bash
ls
cd inhere
file ./*
cat ./-file07
```

---

## 📝 Explanation

* `ls` was used to list files in the home directory.
* The `inhere` directory was entered using `cd`.
* The `file` command was used on all files to determine their types.
* Among the files, only one was identified as ASCII text.
* The readable file was then opened using `cat`.
* The contents of that file revealed the password for the next level.

---

## 🔎 Result

✔ Successfully obtained the password for **Bandit Level 5**

---

## 📸 Screenshots

Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

## 🧠 Concepts Learned

* Using the `file` command to identify file types
* Distinguishing between binary and text files
* Systematic enumeration of files in a directory

---

## ✅ Status

✔ Level 4 → Level 5 completed
