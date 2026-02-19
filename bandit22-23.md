# OverTheWire Bandit — Level 22 → Level 23

## 🎯 Objective

Retrieve the password for the next level by **reverse-engineering a cron job script** that dynamically generates a filename.

---

## 🧠 Our Hint

When a script uses hashing or transformations, recreating the same logic manually can reveal where sensitive data is stored.

---

## 🛠️ Approach

A cron job running as `bandit23` executes a script every minute.

To solve this level:

- Locate the cron job configuration
- Inspect the script being executed
- Understand how the output filename is generated
- Reproduce the filename locally
- Read the generated file to obtain the password

---

## 🧾 Commands Used

```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo "I am user bandit23" | md5sum
cat /tmp/<generated_hash>

---

📝 Explanation

The cron job for bandit23 was identified in /etc/cron.d/.

The script executed by the cron job dynamically creates a filename using an MD5 hash.

The hash is generated from the string I am user bandit23.

By recreating this hash manually, the exact filename used by the script was identified.

The password for the next level was written to this file in /tmp.

Reading this file revealed the password for Bandit Level 23.

---

🧠 Concepts Learned

Cron job analysis

Predictable hashing vulnerabilities

MD5 hash generation

Reverse-engineering automation scripts

Secure handling of scheduled tasks


