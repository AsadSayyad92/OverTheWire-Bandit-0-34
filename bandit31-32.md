# OverTheWire Bandit — Level 31 → Level 32

## 🎯 Objective

Retrieve the password for the next level by **pushing changes to a Git repository that enforces specific content rules**.

---

## 🧠 Our Hint

Sometimes repositories reject commits based on file content.  
Understanding **what the repository expects** is key to bypassing such restrictions.

---

## 🛠️ Approach

In this level, the repository contains instructions indicating that a specific file must be created and pushed, but with a restriction on its contents.

To solve this level:

- Read the repository instructions carefully
- Create the required file with the expected content
- Commit the changes
- Push them to the remote repository

---

## 🧾 Commands Used

```bash
ls
cat README
echo "May I come in?" > key.txt
git add key.txt
git commit -m "Add key file"
git push

---

📝 Explanation

The README file explained that a file named key.txt must be created.

The repository rejected pushes unless the file contained the exact required text.

The file was created with the correct content.

The changes were committed and pushed successfully.

After the push, the repository returned the password for the next level.

---

🧠 Concepts Learned

Git hooks and repository rules

Reading and following repository instructions

Creating and pushing commits

Content validation in version control systems
