# GitHub Repository Setup Guide

This guide will help you upload the Quran Video Creator to GitHub properly.

## Before You Start

Ensure you have:
- Git installed on your computer
- A GitHub account
- The project folder ready

## Step-by-Step GitHub Upload

### 1. Initialize Git Repository

Open terminal/command prompt in the project folder:

```bash
cd /path/to/quran-video-creator

# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Quran Video Creator v29.15"
```

### 2. Create GitHub Repository

1. Go to https://github.com
2. Click the **"+"** icon (top right)
3. Select **"New repository"**
4. Fill in details:
   - **Repository name:** `quran-video-creator`
   - **Description:** "AI-powered tool to create professional Quran videos with perfect audio sync and multi-language support"
   - **Visibility:** Public (recommended) or Private
   - **DO NOT** initialize with README (we already have one)
5. Click **"Create repository"**

### 3. Connect Local Repo to GitHub

GitHub will show you commands. Use these:

```bash
# Add remote repository
git remote add origin https://github.com/YOUR_USERNAME/quran-video-creator.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### 4. Verify Upload

1. Go to your repository on GitHub
2. You should see all files:
   - ✅ README.md
   - ✅ LICENSE
   - ✅ requirements.txt
   - ✅ .gitignore
   - ✅ quran_video_creator.py
   - ✅ And other files

3. **Important:** Check that `.env` file is NOT visible (it should be ignored)

### 5. Add Repository Topics

Make your repo discoverable:

1. Click **"About"** ⚙️ (top right of repo page)
2. Add topics:
   ```
   quran, islamic, video-creator, python, ai, moviepy,
   text-to-speech, instagram, social-media, tiktok,
   youtube-shorts, islamic-app, quran-app
   ```
3. Add website if you have one
4. Save changes

### 6. Enable Discussions (Optional)

1. Go to **Settings** tab
2. Scroll to **Features** section
3. Check **"Discussions"**
4. This allows community Q&A

### 7. Create First Release

1. Click **"Releases"** (right sidebar)
2. Click **"Create a new release"**
3. Fill in:
   - **Tag:** `v1.0.0`
   - **Release title:** `Version 1.0.0 - Initial Release`
   - **Description:**
     ```markdown
     # Quran Video Creator v1.0.0

     First official release! 🎉

     ## Features
     - ✅ Perfect audio synchronization
     - ✅ AI-powered backgrounds
     - ✅ 8+ language support
     - ✅ Professional typography
     - ✅ Batch processing
     - ✅ Social media ready

     ## Installation
     ```bash
     pip install -r requirements.txt
     python quran_video_creator.py
     ```

     See README.md for full documentation.
     ```
4. Click **"Publish release"**

## Repository Settings

### Recommended Settings

1. **Settings → General:**
   - ✅ Allow issues
   - ✅ Allow discussions
   - ✅ Preserve this repository
   - ✅ Allow pull requests

2. **Settings → Branches:**
   - Add branch protection rule for `main`:
     - ✅ Require pull request before merging
     - ✅ Require status checks to pass

3. **Settings → Security:**
   - ✅ Enable Dependabot alerts
   - ✅ Enable security fixes

## Adding a Repository Banner

Create an attractive banner for your README:

1. Use a tool like [Canva](https://www.canva.com) or Figma
2. Suggested size: 1280x640 pixels
3. Include:
   - Project name
   - Brief tagline
   - Islamic imagery (mosque, geometric patterns)
4. Upload to repository as `assets/banner.png`
5. Add to README.md:
   ```markdown
   ![Banner](assets/banner.png)
   ```

## Sample Repository Description

**About section:**
```
🕌 Create stunning Quran videos with AI-powered backgrounds, perfect
audio sync, and multi-language support. Perfect for Instagram, TikTok,
and YouTube Shorts. Features 8+ languages, beautiful Arabic calligraphy,
and professional video quality.
```

## Badges for README

Add these badges to your README (update your username):

```markdown
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![GitHub stars](https://img.shields.io/github/stars/YOUR_USERNAME/quran-video-creator?style=social)
![GitHub forks](https://img.shields.io/github/forks/YOUR_USERNAME/quran-video-creator?style=social)
![GitHub issues](https://img.shields.io/github/issues/YOUR_USERNAME/quran-video-creator)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)
```

## Security Checklist

Before pushing to GitHub, verify:

- [ ] `.env` file is in `.gitignore` and NOT uploaded
- [ ] No API keys in `config.json` (should be empty strings)
- [ ] No API keys in the Python code
- [ ] No personal information in commit history
- [ ] `.env.example` has only placeholder text

**Double-check:**
```bash
# Search for potential API keys
git grep -i "api"
git grep "sk-"
git grep "sb-api"

# Should only show empty values and example files
```

## After Upload - Next Steps

### 1. Share Your Project

- Post on Reddit: r/islam, r/python, r/sidehustle
- Tweet about it
- Share in Islamic developer communities
- Post on LinkedIn

### 2. Set Up GitHub Pages (Optional)

Create a project website:

1. **Settings → Pages**
2. **Source:** Deploy from branch `main`
3. **Folder:** `/docs` or `/` (root)
4. Create `docs/index.html` with project info

### 3. Add Contributing Guidelines

Already done! You have `CONTRIBUTING.md`

### 4. Create Issue Templates

In `.github/ISSUE_TEMPLATE/`:

**bug_report.md:**
```markdown
---
name: Bug Report
about: Report a bug
title: '[BUG] '
labels: bug
---

**Describe the bug**
A clear description of the bug.

**To Reproduce**
Steps to reproduce:
1. Go to '...'
2. Click on '...'
3. See error

**Expected behavior**
What should happen.

**Environment:**
- OS: [e.g., Windows 11]
- Python version: [e.g., 3.10.5]
- FFmpeg version: [e.g., 5.1.2]
```

### 5. Set Up CI/CD (Advanced)

Create `.github/workflows/test.yml`:
```yaml
name: Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: 3.8
      - run: pip install -r requirements.txt
      - run: python -m pytest tests/
```

## Managing Issues

When users report issues:

1. **Label them appropriately:**
   - `bug` - Something broken
   - `enhancement` - New feature request
   - `question` - User question
   - `documentation` - Docs improvement
   - `good first issue` - Easy for newcomers

2. **Respond promptly** (within 24-48 hours)

3. **Use issue templates** for consistency

4. **Close resolved issues** with a comment explaining the fix

## Growing Your Community

1. **Be welcoming** to new contributors
2. **Document everything** clearly
3. **Respond to issues** and PRs quickly
4. **Thank contributors** publicly
5. **Share updates** in discussions
6. **Create milestones** for future versions

## Useful GitHub Commands

```bash
# Check remote
git remote -v

# Update from GitHub
git pull origin main

# Create new branch
git checkout -b feature/new-feature

# Push branch
git push origin feature/new-feature

# Delete local branch
git branch -d branch-name

# Delete remote branch
git push origin --delete branch-name

# View commit history
git log --oneline

# Undo last commit (keep changes)
git reset --soft HEAD~1
```

## Need Help?

- GitHub Docs: https://docs.github.com
- GitHub Community: https://github.community
- Git Handbook: https://guides.github.com/introduction/git-handbook/

---

**Congratulations!** Your project is now on GitHub and ready to help the Muslim community worldwide create beautiful Quran content!

May Allah accept this work and make it a source of ongoing charity (Sadaqah Jariyah) for you.
