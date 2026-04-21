# Git Rebase Conflict Lab

##  Overview

This project demonstrates a real-world Git rebase conflict and how it was resolved step by step while maintaining a clean commit history.

---

##  Scenario

A feature branch `feature-login` was created to update a login button color:

* Original (main branch): **red**
* Feature change: **green**

To update the branch, a rebase was performed:

```bash
git switch feature-login
git rebase main
```

---

## ⚠️ The Conflict

Git paused due to a conflict in `login.txt`:

```txt
<<<<<<< HEAD
Login button is red
=======
Login button is green
>>>>>>> Change login button to green
```

---

## 🧠 Why This Happened

Both branches modified the same line.

Git cannot decide automatically, so it requires **developer input**.

---

## 🛠️ Resolution

The correct version based on feature intent:

```txt
Login button is green
```

Commands used:

```bash
git add login.txt
git rebase --continue
```

---

## ✅ Final Result

* Rebase completed successfully
* Clean and linear commit history
* Feature applied correctly

```bash
git log --oneline --graph
```

Example:

```txt
* Change login button to green
* Change login button to red
* Add login file
```

---

## 🔢 5-Step Conflict Resolution Framework

1. Identify the conflict
2. Understand both versions
3. Decide based on intent
4. Clean the file
5. Continue the rebase

---

## 💡 Key Takeaway

> Merge conflicts are not errors — they are decision points.

---

## 🧰 Skills Demonstrated

* Git branching
* Git rebase
* Conflict resolution
* Version control workflows
* Debugging and decision-making

---

## 🌍 Why This Matters

In real-world development:

* Multiple developers modify the same files
* Conflicts are unavoidable
* Knowing how to resolve them is essential

---

## 👤 Author

Built as part of my journey to mastering Git and real-world development workflows.
