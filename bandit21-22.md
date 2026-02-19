# OverTheWire Bandit — Level 21 → Level 22

## 🎯 Objective

Retrieve the password for the next level by **analyzing a cron job** that runs automatically with higher privileges.

---

## 🧠 Our Hint

Scheduled tasks often execute scripts in the background.  
Inspecting **cron jobs** can reveal where sensitive information is being written.

---

## 🛠️ Approach

In this level, a cron job is running periodically as another user.

To solve this level:

- Identify cron jobs related to the next user
- Inspect the script executed by the cron job
- Determine where the script stores its output
- Read the generated file to obtain the password

---

## 🧾 Commands Used

```bash
ls /etc/cron.d/

---

📝 Explanation

The /etc/cron.d/ directory was inspected to locate scheduled jobs.

A cron job related to bandit22 was identified.

The cron job executes a shell script periodically.

The script copies the password of bandit22 into a file located in /tmp.

Reading this file reveals the password for the next level.

---

🧠 Concepts Learned

Understanding cron jobs

Locating scheduled task definitions

Analyzing shell scripts for sensitive operations

Risks of writing secrets to world-readable locations

