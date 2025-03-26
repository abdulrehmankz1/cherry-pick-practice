# Cherry-Pick Practice

## Project Overview
This project demonstrates how to use **cherry-pick** to merge specific commits from one branch to another without merging the entire branch.

## Steps Followed

### 1. Initial Setup in `main` Branch
Initially, the following sections were added to the `main` branch:
- **Navbar**
- **Hero Section**
- **Card Section**

Commits in `main` branch:
```
Added Bootstrap CSS and basic navigation bar to index.html
Added hero section with image and text below the navbar
Refactored index.html layout and added additional content
Updated container width in index.html from col-xxl-8 to col-xxl-12
Added Bootstrap 5 Footer to index.html
```

### 2. Creating a New Branch
A new branch named `feature-new-sections` was created:
```bash
git checkout -b feature-new-sections
```

In this branch, the following sections were added:
- **About Section**
- **Footer Section**

Commits in `feature-new-sections` branch:
```
Added new "About 1" section to index.html
Added Bootstrap 5 Footer to index.html
```

### 3. Cherry-Picking to `main`
Since `feature-new-sections` will have more updates, it was not merged entirely. Instead, only the **footer section** commit was cherry-picked into `main`.

First, the commit history was checked:
```bash
git log 
```

Then, the footer section commit was cherry-picked:
```bash
git checkout main
git cherry-pick dbd05d0f5bd7b62c524e737e65ca87a1b09457b5
```

### 4. Final Push to `main`
```bash
git push origin main
```

## Conclusion
- **Navbar, Hero, and Card** sections were initially added to `main`.
- **About and Footer** sections were added in `feature-new-sections`.
- **Only the Footer Section was cherry-picked** into `main`.
- The `feature-new-sections` branch remains active for further updates.

🚀 **Cherry-pick practice successfully completed!** 🎉
