# exam2
1) Create Repo Locally → Push to GitHub
✅ Step 1: Create project folder
mkdir my-project
cd my-project
✅ Step 2: Initialize Git
git init
✅ Step 3: Create files

Example:

echo "Hello World" > index.html
✅ Step 4: Add files to staging
git add .
✅ Step 5: Commit
git commit -m "Initial commit"
✅ Step 6: Create repo on GitHub
Go to GitHub
Click New Repository
Name: my-project
Click Create Repository
✅ Step 7: Connect local repo to GitHub
git remote add origin https://github.com/username/my-project.git
✅ Step 8: Push to GitHub
git branch -M main
git push -u origin main

✔️ Done — your code is now on GitHub.

🔹 2) Clone Repo → Make Changes → Push
✅ Step 1: Copy repo URL from GitHub
✅ Step 2: Clone
git clone https://github.com/username/my-project.git
cd my-project
✅ Step 3: Make changes

Edit files in VS Code

✅ Step 4: Check status
git status
✅ Step 5: Add changes
git add .
✅ Step 6: Commit
git commit -m "Updated file"
✅ Step 7: Push
git push origin main
🔹 3) Merge Conflict (VERY IMPORTANT 🔥)
💡 When does conflict happen?

When same line edited in two branches

✅ Step 1: Create branches
git branch feature1
git branch feature2
✅ Step 2: Switch & edit
git checkout feature1
# edit file
git commit -am "feature1 change"
git checkout feature2
# edit same line
git commit -am "feature2 change"
✅ Step 3: Merge
git checkout main
git merge feature1
git merge feature2

🚨 Conflict appears like:

<<<<<<< HEAD
code from feature1
=======
code from feature2
>>>>>>> feature2
✅ Step 4: Resolve conflict manually

Edit file → remove markers → keep correct code

Example:

final correct code
✅ Step 5: Mark resolved
git add .
git commit -m "Resolved merge conflict"
✅ Step 6: Push
git push origin main
🔹 4) Pull Request (PR) – From Scratch
💡 Used when working with branches (team work)
✅ Step 1: Create new branch
git checkout -b feature-branch
✅ Step 2: Make changes
git add .
git commit -m "Added new feature"
✅ Step 3: Push branch
git push origin feature-branch
✅ Step 4: Create PR on GitHub
Go to repo
Click Compare & Pull Request
Add title + description
Click Create Pull Request
✅ Step 5: Merge PR
Click Merge Pull Request
Confirm merge
✅ Step 6: Update local main
git checkout main
git pull origin main
🔹 5) Forking Workflow (Open Source Style)
✅ Step 1: Fork repo
Click Fork on GitHub
Repo copied to your account
✅ Step 2: Clone your fork
git clone https://github.com/your-username/repo-name.git
cd repo-name
✅ Step 3: Add original repo (upstream)
git remote add upstream https://github.com/original-owner/repo-name.git
✅ Step 4: Create branch
git checkout -b my-feature
✅ Step 5: Make changes
git add .
git commit -m "My contribution"
✅ Step 6: Push to your fork
git push origin my-feature
✅ Step 7: Create PR to original repo
Go to your fork on GitHub
Click Compare & Pull Request
Ensure:
Base repo = original repo
Head repo = your fork
Click Create PR
✅ Step 8: Sync fork with original
git checkout main
git pull upstream main
git push origin main
🔥 Important Commands Summary
git init
git clone <url>
git add .
git commit -m "msg"
git push origin main
git pull origin main
git branch
git checkout -b branch-name
git merge branch-name
git remote add origin <url>
💡 Pro Tips (Exam + Practical)
Always check:
git status
Use:
git log