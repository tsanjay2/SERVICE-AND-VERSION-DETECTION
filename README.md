					Setup Git (First Time Only)
# Check if Git is installed
git --version

# Set your username and email (used for commits)
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Optional: enable colored output
git config --global color.ui auto

					Create a New Local Repo

# Inside your project folder
git init

# Add all project files
git add .

# Make your first commit
git commit -m "Initial commit"

					Connect to GitHub


# Create a new EMPTY repo on GitHub (no README)
# Copy its HTTPS link, e.g.:
# https://github.com/username/repo-name.git

# Link your local repo to GitHub
git remote add origin https://github.com/username/repo-name.git

# Verify remote
git remote -v

					Upload (Push) Project to GitHub

# Push code to main branch (first time)
git branch -M main
git push -u origin main

After first upload: you only need

git add .
git commit -m "update message"
git push

					Update and Push Regularly
# Check repo status
git status

# Add changed files
git add .

# Commit changes with message
git commit -m "added new feature or bug fix"

# Push to GitHub
git push

					Clone (Reuse) an Existing Repo

git clone https://github.com/username/repo-name.git

cd repo-name

					Fix Common Git Errors

# Error: “fatal: remote origin already exists”

git remote remove origin
git remote add origin https://github.com/username/repo-name.git

# Error: “Updates were rejected because remote contains work that you do not have”

git pull --rebase origin main
git push origin main

# Error: “Permission denied (publickey)”
git remote set-url origin https://github.com/username/repo-name.git

					Useful Everyday Commands

git status        # Show changes
git log --oneline # Show commit history
git diff          # Show file differences
git branch        # List branches
git checkout -b dev   # Create & switch to new branch
git merge dev         # Merge a branch into main
git push origin dev   # Push dev branch to GitHub

					Undo / Rollback Commands

# Undo last commit (keep changes in files)
git reset --soft HEAD~1

# Discard all unstaged local changes
git checkout -- .

# Remove last commit completely (be careful!)
git reset --hard HEAD~1


