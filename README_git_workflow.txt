===========================
HEP Project Git + VS Code Workflow
===========================

1️⃣ Initial Setup (One-time)
----------------------------
# Set your Git username/email
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

# Link local folder to GitHub repo
cd ~/research_projects/hep_project
git init                # if not already initialized
git remote add origin <your_github_repo_url>

# First push (if remote repo is empty)
git add .
git commit -m "Initial commit"
git push -u origin main

---

2️⃣ Daily Workflow
------------------
# Step 1: Pull latest changes from remote
git pull --rebase origin main
# OR simply `git pull` if you prefer merge commits

# Step 2: Work on your code
# Open VS Code:
code .
# Edit, save, run scripts, etc.

# Step 3: Check status
git status

# Step 4: Stage changes
git add <file1> <file2>   # or git add . to stage all

# Step 5: Commit changes
git commit -m "Descriptive message about changes"

# Step 6: Push changes to remote
git push origin main

---

3️⃣ Optional Useful Commands
----------------------------
# View commit history
git log --oneline

# Check difference between local and remote
git fetch origin
git log main..origin/main

# Switch to another branch
git checkout <branch_name>

# Create a new branch
git checkout -b <new_branch_name>

# Delete a local branch
git branch -d <branch_name>

# Undo local changes (careful!)
git checkout -- <file_name>

---

4️⃣ Notes
---------
- git pull updates the local folder; VS Code will automatically reflect changes.
- Use `git pull --rebase` to keep history linear.
- Always pull before pushing to avoid conflicts.
- Optional: Use tmux or screen for running long scripts on remote servers.

===========================
End of Workflow Guide
===========================

