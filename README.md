# 2025 June 4 Per Scholas SBA Version Control

Re:  steps taken to create and manage branches:

1.  Created new repository in GitHub, cloned to local.  Entered new directory, checked and saw .git existed.  Terminal indicated main branch active, but git branch did not detect branch.  Added README.md and committed, entered "git branch -M main", checked git branch again, main branch detected and active.

2.  "git checkout -b feature/header", created index.html and added header, committed.

3.  "git checkout main"

4.  "git checkout -b feature/footer", created index.html and added footer, committed.

5.  "git checkout feature/header", modified index.html by adding a footer (creating a simulated conflict).

6.  "git checkout main"

7.  "git merge feature/footer", merged with no issues.

8.  "git merge feature/header", merge conflict.  Resolved in VSCode.  Still on main branch; git add, git commit.  Currently writing markdown before git push.

Re:  handling merge conflict

I was not initially able to handle the merge conflict in VSCode, as I thought I needed to get the red ! to disappear.  I requested and received help, and now understand the red ! disappears after git add, and need not be immediately resolved in VSCode to proceed.

In this particular case, two entirely separate files were created.  First, the feature/header branch was created, after which the index.html file was created and filled, second the feature/footer branch was created, after which another index.html file was created and filled.  Modifying the feature/header branch to add a footer did not, I think, significantly change what followed.

Merging the feature/footer to main resulted in no issues, there being nothing in main to conflict with.  Merging feature/header, though, conflicted with the entirely different file that had been created in feature/footer, so needed manual resolution.

I accepted the material in feature/header, and manually copy/pasted the code I wanted to keep from feature/footer.  This resolved the conflict, though the red ! was still present in VSCode.  Still in the main branch, I git add.  I believe the red ! disappeared in VSCode at that point.  No outstanding issues.

Re:  Peer Review Evidence:

Per instructions, we may dispense with this section.  Noted, we did carry this out in class, and I think the procedure is clear, though I intend to work on it later.