# OverTheWire Bandit — Level 10 → Level 11

🎯 **Objective**  
Retrieve the password for the next level from a file that is **encoded using Base64**.

---

🧠 **Our Hint**  
When data looks scrambled but structured, it may be encoded.  
The `base64` command can be used to **decode Base64-encoded content**.

---

🛠️ **Approach**  
This level provides a file that contains encoded text instead of plain readable content.

To solve this, I followed these steps:

- Identified the file containing the encoded data  
- Used `base64` to decode the content  
- Read the decoded output to obtain the password  

---

🧾 **Commands Used**
```bash
ls
cat data.txt
base64 -d data.txt

---

📝 Explanation

ls was used to confirm the presence of the file data.txt.

The content of the file appeared encoded rather than readable.

The base64 -d command was used to decode the encoded data.

The decoded output revealed the password for the next level.

---

🧠 Concepts Learned

Identifying encoded data

Decoding Base64 using the command line

Understanding basic data encoding concepts

---

✅ Status
✔ Level 10 → Level 11 completed
