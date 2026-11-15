# BookHaven

BookHaven is a lightweight online book catalog project built as part of a Git and GitHub workflow assignment. The site presents a clean, minimal browsing experience for readers and highlights a selection of featured books.

## Project Overview
- Name: BookHaven
- Purpose: Showcase a book catalog website with a home page and an about page
- Theme: Digital library / reading catalog
- Tools: HTML5, Git, GitHub workflow practice

## Features
- Simple landing page for the BookHaven catalog
- About page with project and contact information
- Featured books section highlighting notable titles
- Version control practice with branches and merges
- Ignore rules for log files and temporary folders
- Revert workflow demonstration for safe undo of commits

## Project Structure
```text
BookHaven/
??? index.html
??? about.html
??? .gitignore
??? git_commands.txt
??? README.md
??? debug.log            # ignored by Git
??? temporary.txt         # removed after revert test
??? temp/
    ??? cache.txt        # ignored by Git
```

## Commit Graph
```text
* d293d59 Revert "Add temporary.txt for testing revert"
* 6c9baee Add temporary.txt for testing revert
* 192e9a1 Add .gitignore to ignore log files and temp directory
* f0a4470 Add contact section to about.html
* 9cdef60 Update index.html: add featured books collection
* 6d19725 Initial commit: add index.html and about.html
```

## Git Workflow Summary
1. Initialize a Git repository and rename the default branch to main.
2. Create the initial site pages and commit them.
3. Add a featured books list on the main branch.
4. Create a feature branch and add contact/support info.
5. Merge the feature branch back into main.
6. Add `.gitignore` rules for logs and temp files.
7. Create a temporary file, commit it, and revert it cleanly.
8. Document the commands used in `git_commands.txt`.

## 8-Case Login System Test Case Table
| Case | Scenario | Test Input | Expected Result |
|------|----------|------------|-----------------|
| 1 | Valid login | username: admin, password: admin123 | Successful login |
| 2 | Empty username | username: "", password: admin123 | Error: username required |
| 3 | Empty password | username: admin, password: "" | Error: password required |
| 4 | Incorrect password | username: admin, password: wrongpass | Error: invalid credentials |
| 5 | Unknown username | username: guest, password: secret | Error: user not found |
| 6 | Password too short | username: admin, password: 123 | Error: password too short |
| 7 | SQL injection attempt | username: ' OR '1'='1, password: anything | Login rejected |
| 8 | Session timeout | user logs in, stays idle beyond timeout | Redirect to login page |

## Remote Setup Instructions
To connect this project to GitHub and push both branches:
```bash
git remote add origin <your-github-repo-url>
git push -u origin main
git push -u origin feature
```

## Notes
This project is intentionally kept simple and educational to demonstrate Git branching, merging, ignore rules, and revert workflow in a clean, assignment-ready structure.
