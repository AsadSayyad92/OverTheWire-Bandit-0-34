# OverTheWire Bandit — Level 6 → Level 7

🎯 **Objective**
Retrieve the password for the next level by locating a file somewhere on the system that matches **specific ownership and size conditions**.

---

🧠 **Our Hint**
When files are not located in the home directory, the `find` command can be used with **filters like owner, group, and size** to locate the correct file.

---

🛠️ **Approach**
In this level, the password file is **not located inside the home directory**.
Instead, it exists somewhere on the system.

To solve this, I followed these steps:

* Performed a system-wide search using `find`
* Applied filters to reduce the search results
* Suppressed permission errors
* Opened the discovered file

---

🧾 **Commands Used**

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```

---

📝 **Explanation**

* The `find /` command searched the entire filesystem.
* Filters were applied to find files that:

  * Are owned by user `bandit7`
  * Belong to group `bandit6`
  * Have a size of exactly `33 bytes`
* `2>/dev/null` was used to hide permission-denied errors.
* The command returned the file path:
  `/var/lib/dpkg/info/bandit7.password`
* The file was opened using `cat`, revealing the password for the next level.

---

🔎 **Result**
✔ Successfully obtained the password for **Bandit Level 7**

---

📸 **Screenshots**
Screenshots related to this level are stored in the `screenshots/` directory.

> Screenshots do **not** expose passwords.

---

🧠 **Concepts Learned**

* System-wide searching using `find`
* Filtering files by user, group, and size
* Suppressing error output using `2>/dev/null`
* Efficient enumeration techniques in Linux

---

✅ **Status**
✔ Level 6 → Level 7 completed
