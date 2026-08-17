# Project Submission Report

## 1. Student Details

- **Full Name:** Denzel Murimi
- **GitHub Username:** denzel-murimi
- **Email:** denzel.kahuthia@strathmore.edu

---

## 2. Deployed Project Link

- **Live GitHub Pages URL:** https://is-project-2026.github.io/ecommerce-166537/
---

## 3. Reflection — Grounded in Your Git History

### A. Your Best Commit

- **Commit URL:** https://github.com/IS-PROJECT-2026/ecommerce-166537/commit/c6bffda0b1119f0350be1d83c0fd43c769a92a45
- **Why this one?** This commit perfectly follows the Conventional Commits specification. It uses the `chore:` type for configuration, features an imperative subject line under 50 characters ("chore: configure nextjs for static export"), and utilizes a clear footer to automatically close Issue #6.

### B. A Mistake or Struggle

- **Link to the evidence:** https://github.com/IS-PROJECT-2026/ecommerce-166537/pull/5
- **What happened and how did you recover?** I accidentally committed directly to my local `main` branch before creating my feature branch. I recovered by using `git stash` to save my uncommitted changes, running `git reset --hard HEAD` to clean `main`, checking out my new feature branch, and then using `git stash pop` to reapply the work safely in isolation.

### C. A Pull Request You're Proud Of

- **PR URL:** https://github.com/IS-PROJECT-2026/ecommerce-166537/pull/5
- **What did you check before merging?** I acted as my own reviewer by checking the "Files changed" tab to ensure I didn't accidentally include unnecessary configuration files (like `.DS_Store`), and I verified the description included the keyword "Closes #4" to maintain traceability.

### D. One Thing You Would Do Differently

- **What would you change?** I would break down my milestone issues to be much more granular. My initial issue for building the storefront UI was too broad, which led to a massive, hard-to-review Pull Request. 
- **Link to the evidence of the original decision:** https://github.com/IS-PROJECT-2026/ecommerce-166537/issues/4

---

## 4. Screenshots of Key GitHub Features

### A. Milestones and Issues

![Active milestones](image.png)



### B. Project Board

![Kanban board showing tasks dynamically moving from To Do, to In Progress, to Done as development progressed.](image-1.png)



### C. Branching Architecture

![alt text](image-2.png)



### D. Pull Requests & Traceability

![alt text](image-3.png)

* 

---

## 5. Merge Conflict Evidence

### Conflict 1 — Full Chronology

**What cause did you use?** Same Line Modification (Content Conflict)

#### Step 1: Generating the Clash

[PASTE SCREENSHOT OF ATTEMPTED MERGE / TERMINAL WARNING HERE]

* **Caption:** The merge collision between `feat/banner-promo` and `feat/banner-urgent` resulting in a Git conflict warning.

#### Step 2: Inside the Code Editor (Conflict Markers)

[PASTE SCREENSHOT OF RAW CONFLICT MARKERS HERE]

* **Caption:** Both branches attempted to modify the hero banner string on the exact same line in `page.tsx`. I chose to keep the 'Flash Sale' text from the urgent branch.

#### Step 3: Resolution & Clean Merge

[PASTE SCREENSHOT OF CLEAN RESOLUTION HERE]

* **Caption:** The `page.tsx` file cleanly merged into `main` after manually deleting the raw Git conflict markers and committing the finalized text.

---

### Conflict 2 — Different Cause

**What cause did you use?** File Deletion vs. Modification (Tree Conflict)

**Why does this cause trigger a conflict?** This triggers a conflict because one branch attempts to add new code to a file (`globals.css`), while the other branch completely deletes that exact same file, confusing Git on whether the file should exist or not.

[PASTE SCREENSHOT OF CONFLICT MARKERS FOR CONFLICT 2 HERE]

* **Caption:** Terminal warning showing a tree conflict where `style/update-theme` modified `globals.css` while `chore/remove-legacy-css` deleted it.

---

### Conflict 3 — Different Cause

**What cause did you use?** File Rename vs. Modification

**Why does this cause trigger a conflict?** This occurs because Git loses track of the file's history. One branch changed the filename (from `schema.png` to `database-schema.png`), while a competing branch altered the contents of the original, un-renamed file.

[PASTE SCREENSHOT OF CONFLICT MARKERS FOR CONFLICT 3 HERE]

* **Caption:** Terminal output of `git status` showing the image asset caught in a rename/modify conflict.

---
##
## 6. Feedback & Evaluation

- [x] **Anonymous Evaluation Form:** [Course & Instructor Evaluation](https://forms.gle/YLybnsyXXErKEg3s9)