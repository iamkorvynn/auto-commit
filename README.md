# Daily Auto-Commit GitHub Actions Bot

This repository is set up with a GitHub Actions workflow that automatically commits to this repository once a day. This helps keep your GitHub contribution graph active even when you don't open your laptop.

## Setup Instructions

### 1. Set Workspace
To work on this project in your IDE, please set this directory as your active workspace:
`C:\Users\numaa\.gemini\antigravity-ide\scratch\github-auto-commit-bot`

### 2. Initialize and Push to GitHub
Run the following commands in your terminal to initialize git and push to your GitHub:

```bash
# 1. Initialize git (if not already done)
git init

# 2. Add files
git add .
git commit -m "Initial commit with GitHub Actions bot"

# 3. Rename branch to main
git branch -M main

# 4. Link to a new repository on GitHub (replace with your repository URL)
git remote add origin https://github.com/your-username/your-repo-name.git

# 5. Push to GitHub
git push -u origin main
```

### 3. Enable Write Permissions for Actions on GitHub
For the GitHub Actions workflow to successfully commit back to your repository:
1. Go to your repository on GitHub.
2. Click **Settings** (gear icon) -> **Actions** -> **General**.
3. Scroll down to **Workflow permissions**.
4. Select **Read and write permissions**.
5. Click **Save**.

## How It Works
* The workflow is defined in [.github/workflows/daily-commit.yml](file:///.github/workflows/daily-commit.yml).
* It runs every day at 09:00 UTC (runs in GitHub's cloud, no laptop required).
* It updates [last_commit.txt](file:///last_commit.txt) with the current timestamp and pushes it back.
* You can also run it manually anytime by going to your repository's **Actions** tab on GitHub, selecting **Daily Auto Commit**, and clicking **Run workflow**.
