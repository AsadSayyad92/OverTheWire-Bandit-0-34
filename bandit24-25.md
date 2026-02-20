# OverTheWire Bandit — Level 24 → Level 25

## 🎯 Objective

Retrieve the password for the next level by **brute-forcing a 4-digit PIN** required by a network service running on a local port.

---

## 🧠 Our Hint

If a service validates authentication using a **short numeric PIN**, automation can be used to systematically test all possible combinations.

---

## 🛠️ Approach

A service is running on `localhost` and expects input in the following format:


The service responds with:
- `Wrong!` for incorrect PINs
- The next level’s password when the correct PIN is provided

To solve this level:

- Identify the service port
- Automate PIN attempts from `0000` to `9999`
- Capture the successful response

---

## 🧾 Commands Used

```bash
nc localhost 30002
for i in {0..9999}; do
  pin=$(printf "%04d" $i)
  echo "<bandit24_password> $pin" | nc localhost 30002
done

---

📝 Explanation

A service listening on port 30002 validates a password and PIN combination.

The PIN consists of exactly four digits, including leading zeros.

A loop was used to generate all possible PIN combinations from 0000 to 9999.

Each attempt sent the current password along with a PIN to the service.

When the correct PIN was used, the service returned the password for the next level.

---

🧠 Concepts Learned

Brute-force attacks

Automating network interactions

PIN-based authentication weaknesses

Using loops and formatting in shell scripting

Service enumeration on localhost

