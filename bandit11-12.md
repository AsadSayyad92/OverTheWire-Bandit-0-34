# OverTheWire Bandit — Level 11 → Level 12

🎯 **Objective**  
Retrieve the password for the next level from a file that has been **encoded using ROT13**.

---

🧠 **Our Hint**  
ROT13 is a simple substitution cipher that shifts letters by 13 positions.  
The `tr` command can be used to **translate characters** and reverse this encoding.

---

🛠️ **Approach**  
This level provides a file where the content looks readable but the letters are scrambled.

To solve this, I followed these steps:

- Identified the file containing the encoded text  
- Used the `tr` command to rotate characters back to their original form  
- Read the decoded output to obtain the password  

---

🧾 **Commands Used**
```bash
ls
cat data.txt
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

---

📝 Explanation

ls was used to confirm the presence of the file data.txt.

The content appeared scrambled but still alphabetic, suggesting a simple cipher.

The tr command was used to rotate each letter by 13 positions.

This effectively decoded the ROT13 text back into readable form.

The decoded output revealed the password for the next level.

---

🧠 Concepts Learned

Understanding ROT13 encoding

Using tr for character translation

Simple cryptographic transformations on the command line

---

✅ Status
✔ Level 11 → Level 12 completed
