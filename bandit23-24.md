# OverTheWire Bandit — Level 23 → Level 24

## 🎯 Objective

Retrieve the password for the next level by **injecting a script into a cron job directory** that executes with higher privileges.

---

## 🧠 Our Hint

If a cron job executes **every script from a writable directory**, placing your own script there can allow you to run commands as another user.

---

## 🛠️ Approach

A cron job running as `bandit24` executes scripts placed inside a specific directory.

To solve this level:

- Identify the cron job configuration
- Locate the directory where scripts are executed
- Create a malicious script to extract the password
- Place the script in the execution directory
- Wait for the cron job to run

---

## 🧾 Commands Used

```bash
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
nano /tmp/getpass.sh
chmod +x /tmp/getpass.sh
cp /tmp/getpass.sh /var/spool/bandit24/foo/
cat /tmp/b24pass

---

📝 Explanation

The cron job configuration showed that scripts placed in /var/spool/bandit24/foo/ are executed every minute.

A custom shell script was created to read the password file of bandit24.

The script redirected the output to a file in /tmp.

After copying the script into the execution directory, the cron job executed it automatically.

The password for the next level was retrieved from the output file.

---

🧠 Concepts Learned

Cron job exploitation

Script injection via writable directories

Privilege escalation through automation

Risks of insecure cron configurations
