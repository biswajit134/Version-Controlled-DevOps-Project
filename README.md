# Build a Version-Controlled DevOps Project with Git
## Hints:
**1. Initialize repo a. and push to GitHub.**
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20184348.png?raw=true)
**2. Create dev, feature, and main branches.**
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20185931.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20190210.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20191040.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20191040.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20191701.png?raw=true)
**3. Use pull requests to merge.**
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20192629.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20192825.png?raw=true)
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20193253.png?raw=true)
**4. Add a proper README.md.**
**5. Use .gitignore and tags.**
![image_url](https://github.com/biswajit134/Version-Controlled-DevOps-Project/blob/main/SS/Screenshot%202026-02-17%20195219.png?raw=true)
**6. Document all tasks using markdown.**

## Interview Questions:
**1. What is Git?**

Git is a Distributed Version Control System (DVCS) used to track changes in source code during software development.

* Distributed: Every developer has a complete local copy of the entire project history, allowing them to work offline.

* Version Control: It records who made which changes and when, allowing you to revert to earlier versions if something breaks.

* Collaboration: It allows multiple developers to work on the same codebase simultaneously without overwriting each other's work.

**2. What is the difference between merge and rebase?**

Both commands integrate changes from one branch into another, but they do so in entirely different ways.

* Merge: Takes the contents of a source branch and integrates it with a target branch. It creates a brand-new "merge commit" that ties the histories of both branches together.

Pros/Cons: Preserves the complete, chronological history of the project, but can result in a messy, cluttered commit history.

* Rebase: Moves or "replays" a feature branch onto the very tip of the target branch.

Pros/Cons: Creates a perfectly linear, clean project history without extra merge commits. However, it rewrites project history, which can cause massive collaboration issues if you rebase a branch that has already been shared with others.

**3. What is a pull request?**

A pull request (PR) is a feature provided by Git hosting platforms like GitHub, GitLab, or Bitbucket (it is not a native Git command).
It is a formal request to merge a feature branch into the main branch. A PR alerts team members that code is ready, provides a dedicated forum for code review, allows for automated testing (CI/CD) to run against the new code, and initiates discussion before the code becomes part of the main project.

**4. How do you resolve merge conflicts?**

A merge conflict occurs when Git cannot automatically resolve differences in code between two commits (usually because the exact same line of code was altered in two different ways).
To resolve a conflict:

1. Identify the conflict: Run git status to see which files are unmerged.

2. Open the file: Look for Git's conflict markers: <<<<<<< (your current branch), ======= (the dividing line), and >>>>>>> (the incoming branch).

3. Edit the code: Manually decide which code to keep, combine the changes if necessary, and completely delete the conflict markers.

4. Finalize: Save the file, stage it using git add <filename>, and then run git commit to complete the merge process.

**5. What are Git tags?**

Git tags are static references that point to specific points in a repository's history. Unlike branches, which continuously move forward as new commits are added, tags are fixed. They are almost exclusively used to mark release points (e.g., v1.0.0, v2.4.1) so you can easily deploy or roll back to a specific, stable version of the software.

**6. What is Git workflow?**

A Git workflow is a standardized set of rules and practices that dictate how a team uses Git to collaborate on a project. It ensures everyone is branching, merging, and releasing software in a consistent way. Common examples include:

* GitFlow: A strict branching model utilizing separate branches for features, releases, and hotfixes.

* GitHub Flow: A simpler, agile-friendly model where all new work happens on feature branches that are merged directly into the main branch via pull requests.

* Trunk-Based Development: All developers commit small, frequent changes directly to a single shared branch (the trunk/main) to avoid long-lasting feature branches.

**7. Explain git stash.**

git stash temporarily shelves (or "stashes") changes you've made to your working directory that are not yet ready to be committed.
This is incredibly useful when you are in the middle of working on a feature, but suddenly need to switch branches to fix an urgent bug. You can stash your messy work, switch branches, do the fix, switch back, and run git stash pop to reapply your unfinished work exactly as you left it.

**8. What is the use of .gitignore?**

The .gitignore file is a plain text file placed in the root of a repository that explicitly tells Git which files or directories it should completely ignore and not track.
This is crucial for keeping repositories clean and secure. Common things added to a .gitignore include:

* Compiled code (e.g., .class, .exe files)

* Language/framework dependency folders (e.g., node_modules, venv)

* Hidden OS files (e.g., .DS_Store)

* Sensitive configuration files holding passwords or API keys (e.g., .env)