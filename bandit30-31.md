

```md
# OverTheWire Bandit — Level 30 → Level 31

## 🎯 Objective

Retrieve the password for the next level by **inspecting Git tags** in a repository.

---

## 🧠 Our Hint

Tags are often used to mark releases or important points in a project.  
Sensitive information may still exist inside **tagged snapshots**.

---

## 🛠️ Approach

The repository does not reveal the password in files or branches.

To solve this level:

- List all Git tags
- Inspect the contents of tagged commits
- Locate the password stored in a tag

---

## 🧾 Commands Used

```bash
cd repo
git show <tag-name>

---

📝 Explanation

git tag was used to list all tags in the repository.

One of the tags pointed to a commit containing sensitive information.

git show displayed the contents of the tagged commit.

The password for the next level was found inside the tag output.

This demonstrates that tags can expose historical data.

---

🧠 Concepts Learned

Git tags and their purpose

Inspecting tagged commits

Secret exposure through version control metadata

Importance of repository hygiene

