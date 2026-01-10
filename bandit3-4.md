# OverTheWire Bandit — Level 3 → Level 4

## 🎯 Objective

Retrieve the password for the next level from a **hidden file** inside a directory.

---

## 🧠 Hint

Hidden files in Linux start with a **dot (`.`)** and are not shown by default.
You need to explicitly tell the system to display them.

---

## 🛠️ Approach

In this level, the password is not directly visible because it is stored in a hidden file.

To solve this:

* Navigate into the given directory
* List all files including hidden ones
* Identify and read the hidden file

---

## 🧾 Commands Used

```bash
ls
cd inhere
ls -a
cat .hidden
```

---

## 📝 Explanation

* `ls` was used to view the contents of the home directory.
* The directory named `inhere` was identified and entered using `cd`.
* `ls -a` was used to list all files, including hidden ones.
* A hidden file named `.hidden` was found.
* The `cat` command was used to display the contents of the hidden file.
* The output revealed the password for the next level.

---

## 🔎 Result

✔ Successfully obtained the password for **Bandit Level 4**

---

## 📸 Screenshots

Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

## 🧠 Concepts Learned

* Understanding hidden files in Linux
* Using `ls -a` to display hidden content
* Navigating directories efficiently using the terminal

---

## ✅ Status

✔ Level 3 → Level 4 completed

