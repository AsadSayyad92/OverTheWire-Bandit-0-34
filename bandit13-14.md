# OverTheWire Bandit — Level 13 → Level 14

🎯 **Objective**  
Retrieve the password for the next level by using an **SSH private key** instead of a password to authenticate.

---

🧠 **Our Hint**  
SSH supports key-based authentication.  
If a private key is provided, it must be saved locally and given correct permissions before it can be used.

---

🛠️ **Approach**  
This level provides a private SSH key that must be used to log in as the next user instead of using a password.

To solve this, I followed these steps:

- Located the provided private key file  
- Copied the key content to my local machine  
- Saved it into a new file  
- Adjusted file permissions for security  
- Used the key with SSH to log in to the next level  

---

🧾 **Commands Used**

_On the Bandit server (bandit13):_
```bash
cat sshkey.private

nano bandit14key
chmod 600 bandit14key
ssh -p 2220 -i bandit14key bandit14@bandit.labs.overthewire.org

---

📝 Explanation

The file sshkey.private contained an SSH private key instead of a password.

The key was copied and saved locally into a new file (bandit14key).

chmod 600 was required because SSH refuses to use keys that are publicly readable.

The ssh -i option was used to specify the private key for authentication.

Successful login granted access to the bandit14 account without using a password.

---

🧠 Concepts Learned

Understanding SSH key-based authentication

Proper permission handling using chmod 600

Using private keys with the ssh -i option

Real-world secure login practices
