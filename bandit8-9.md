# OverTheWire Bandit — Level 8 → Level 9

🎯 **Objective**  
Retrieve the password for the next level by identifying the **only unique line** inside a file containing many duplicate entries.

---

🧠 **Our Hint**  
When a file contains repeated lines, commands like `sort` and `uniq` can be combined to **filter duplicates and reveal the unique entry**.

---

🛠️ **Approach**  
This level provides a file where most lines are duplicated, but only one line is different and contains the password.

To solve this, I followed these steps:

- Identified the file containing the data  
- Sorted the file content to group identical lines together  
- Used `uniq` to extract the line that appears only once  

---

🧾 **Commands Used**
```bash
ls
sort data.txt | uniq -u

---

🧠 Concepts Learned

Searching and organizing data using sort

Filtering unique lines using uniq -u

Using pipelines to combine multiple Linux commands effectively

---

✅ Status
✔ Level 8 → Level 9 completed
