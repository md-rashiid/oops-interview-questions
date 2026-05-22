# Git & GitHub Commands - Complete Guide

## What is Git?
Git = Version control system jo code ka history track karta hai
GitHub = Cloud platform jaha pe code upload karte ho

---

## IMPORTANT: SSH Setup Done ✅
Password nahi chahiye! SSH automatically authenticate karti hai!

---

## All Commands Explained

### 1. Navigate to Folder
**Command:**
```bash
cd ~/Desktop/folder-name
```

**Meaning:** Apne project folder mein jao
**When to use:** Shuru mein, jab kaam start karo
**Example:**
```bash
cd ~/Desktop/oops-interview-questions
```

---

### 2. Check What Changed
**Command:**
```bash
git status
```

**Meaning:** Dekho kaunsi files change hui
**When to use:** Code likho, phir check kar
**Output Example:**
```
modified: README.md
new file: interview-questions.txt
```

---

### 3. Prepare Files for Upload
**Command:**
```bash
git add .
```

**Meaning:** Sab files ko upload ke liye ready kar
**When to use:** `git status` ke baad
**Notes:**
- `.` = sab files
- `git add filename` = specific file ke liye

---

### 4. Save Changes with Message
**Command:**
```bash
git commit -m "message likho"
```

**Meaning:** Files ko SAVE kar message ke saath
**When to use:** `git add` ke baad
**Good Messages:**
```
✅ "Add OOP interview questions"
✅ "Fix inheritance example in README"
❌ "changes"
❌ "update"
```

---

### 5. Upload to GitHub
**Command:**
```bash
git push origin main
```

**Meaning:** Local folder ka content GitHub par upload kar
**When to use:** `git commit` ke baad
**Output Expected:**
```
To github.com:md-rashiid/repo-name.git
   abc123..def456  main -> main
```

---

### 6. See Commit History
**Command:**
```bash
git log --oneline
```

**Meaning:** Sab previous commits dekho
**When to use:** Jab previous work dekh sakte ho
**Output Example:**
```
abc1234 Add OOP questions
def5678 Add README
```

---

### 7. Check Remote Connection
**Command:**
```bash
git remote -v
```

**Meaning:** Dekho GitHub se connected hai ya nahi
**When to use:** Troubleshooting ke time
**Expected Output:**
```
origin git@github.com:md-rashiid/repo-name.git (fetch)
origin git@github.com:md-rashiid/repo-name.git (push)
```

---

## WORKFLOW - Har Din Ye 4 Commands

### Daily Upload Process:

**Step 1:** Code likho aur save kar
```bash
cd ~/Desktop/oops-interview-questions
```

**Step 2:** Check kya change hua
```bash
git status
```

**Step 3:** Prepare kar upload ke liye
```bash
git add .
```

**Step 4:** Save kar message ke saath
```bash
git commit -m "Descriptive message likho"
```

**Step 5:** GitHub par upload kar
```bash
git push origin main
```

---

## Common Scenarios

### Scenario 1: README.md edit karna

```bash
# Folder mein jao
cd ~/Desktop/oops-interview-questions

# README.md edit karo (text editor mein)
[Open README.md, add content]

# Files prepare kar
git add .

# Save kar message ke saath
git commit -m "Add interview questions about OOP"

# GitHub par upload kar
git push origin main
```

---

### Scenario 2: Naya file add karna

```bash
# Naya file create kar
[Create notes.txt in folder]

# Check status
git status

# Prepare kar
git add .

# Save kar
git commit -m "Add study notes for OOP concepts"

# Upload kar
git push origin main
```

---

### Scenario 3: Multiple files change

```bash
# Multiple files edit kar

# Check status
git status

# Sab prepare kar
git add .

# Ek message mein sab save kar
git commit -m "Update OOP notes and interview questions"

# Upload kar
git push origin main
```

---

## Important Points - Yaad Rakho!

✅ **Always do in THIS order:**
1. `git add .`
2. `git commit -m "..."`
3. `git push origin main`

❌ **Don't forget message in commit!**
- Bad: `git commit -m ""`
- Good: `git commit -m "Add inheritance example"`

✅ **Message likho jo bataye KYA kiya:**
- "Add Q1 about Inheritance"
- "Fix typo in README"
- "Add code example for Polymorphism"

---

## Quick Reference Card

```
cd folder          → Navigate to folder
git status         → Check what changed
git add .          → Prepare files
git commit -m ""   → Save with message
git push           → Upload to GitHub
git log            → See history
git remote -v      → Check GitHub connection
```

---

## Remember This Flow

```
📝 Code likho
📦 git add .
💾 git commit -m "message"
📤 git push origin main
✅ GitHub par visible!
```

---

Made by Md Rashid | May 2026
