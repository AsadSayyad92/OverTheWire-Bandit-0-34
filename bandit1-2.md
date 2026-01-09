# OverTheWire Bandit — Level 1 → Level 2

## 🎯 Objective

Retrieve the password for the next level from a file that has a **special character in its name**.

---

## 🧠 Hint Provided by Bandit

> The password for the next level is stored in a file called **-** located in the home directory.

---

## 🛠️ Approach

The challenge here is that the filename starts with a hyphen (`-`), which is normally interpreted as an option by Linux commands.

To handle this safely:

* Identify the file in the directory
* Use a method that allows reading files with special names

---


## 📝 Explanation

* `ls` was used to list the files in the home directory.
* The file named `-` was identified.
* Using `cat -` would not work directly because `-` is treated as an option.
* Prefixing the filename with `./` explicitly tells the shell to treat it as a file.
* `cat ./-` successfully displayed the contents of the file.
* The output contained the password for the next level.

---

## 🔎 Result

✔ Successfully obtained the password for **Bandit Level 2**

---

## 📸 Screenshots

Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

## 🧠 Concepts Learned

* Handling filenames that start with special characters
* Understanding how Linux commands interpret options
* Using relative paths to avoid command-line ambiguity

---

## ✅ Status

✔ Level 1 → Level 2 completed

---

