# OverTheWire Bandit — Level 17 → Level 18

## 🎯 Objective

Retrieve the password for the next level by **comparing two files** and identifying the difference between them.

---

## 🧠 Our Hint

When two files look similar, tools like `diff` are useful to **compare files line by line** and highlight differences.

---

## 🛠️ Approach

In this level, two files are provided:

- `passwords.old`
- `passwords.new`

The password for the next level is the **only line that differs** between these two files.

To solve this level:

- Compare both files
- Identify the changed line
- Extract the new password

---

## 🧾 Commands Used

```bash
ls

---

📝 Explanation

ls was used to list the available files.

The diff command compared both files line by line.

The output showed a single line difference.

The line present only in passwords.new contained the password for the next level.

---

🧠 Concepts Learned

Comparing files using diff

Identifying changes between versions of files

Understanding how configuration or credential changes can be detected

Importance of file comparison in audits and forensics
