# OverTheWire Bandit — Level 9 → Level 10

🎯 **Objective**  
Retrieve the password for the next level from a file that contains mostly **non-readable (binary) data**, where the password is hidden among human-readable strings.

---

🧠 **Our Hint**  
When a file is not human-readable, the `strings` command can be used to extract readable text from binary data.

---

🛠️ **Approach**  
This level provides a file that appears unreadable when opened normally, making it difficult to manually inspect.

To solve this, I followed these steps:

- Identified the file provided in the directory  
- Used `strings` to extract readable text  
- Filtered the output to locate the password  

---

🧾 **Commands Used**
```bash
ls
strings data.txt
strings data.txt | grep =

---

🧠 Concepts Learned

Extracting readable text from binary files using strings

Filtering output using grep

Efficiently analyzing unknown file formats

---

✅ Status
✔ Level 9 → Level 10 completed
