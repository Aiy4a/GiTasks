# Git Lab 1

This lab demonstrates working with commits, reset, amend, and revert in Git.

---

## Steps

### 1. Create 4 commits
```bash
echo "Hello world" > test.txt
git add test.txt
git commit -m "hello world"

echo "hello 2" >> test.txt
git commit -am "second edit"

echo "hello 3" >> test.txt
git commit -am "third edit"

echo "hello 4" >> test.txt
git commit -am "fourth edit"
```

---

### 2. Delete the last two commits
```bash
git reset --hard HEAD^^
```

---

### 3. Add a new commit after deletion
```bash
echo "new line after deletion" >> test.txt
git commit -am "commit after deletion"
```

---

### 4. Amend the last commit
```bash
echo "lab Done" >> test.txt
git add test.txt
git commit --amend -m "finish"
```

---

### 5. Self-study: What is `git revert`?
- `git revert` creates a new commit that undoes the changes of a previous commit.
- Unlike `reset`, it does not delete history. It’s safe for shared repositories.

---

### 6. Revert commit back
```bash
git revert HEAD
```

This creates a new commit that reverses the last commit.

---

