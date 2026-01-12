# OverTheWire Bandit — Level 7 → Level 8

🎯 **Objective**
Retrieve the password for the next level by finding a **specific line inside a large text file**.

---

🧠 **Our Hint**
When a file is too large to read manually, tools like `grep` can be used to **search for specific words or patterns** inside files.

---

🛠️ **Approach**
This level provides a large file containing many lines of text, but only one line contains the useful information.

To solve this, I followed these steps:

* Identified the file present in the directory
* Used `grep` to search for a meaningful keyword
* Extracted the matching line containing the password

---

🧾 **Commands Used**

```bash
ls
grep millionth data.txt
```

---

📝 **Explanation**

* `ls` was used to confirm the presence of the file `data.txt`.
* The file was too large to inspect manually.
* The `grep` command was used to search for the keyword `millionth` inside the file.
* `grep` returned the exact line that contained the password.
* That output revealed the password for the next level.

---

🔎 **Result**
✔ Successfully obtained the password for **Bandit Level 8**

---

📸 **Screenshots**
Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

🧠 **Concepts Learned**

* Searching inside files using `grep`
* Efficient handling of large text files
* Pattern matching on the Linux command line

---

✅ **Status**
✔ Level 7 → Level 8 completed
