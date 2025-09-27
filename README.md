# Git and GitHub

* **Git** is a version control system that manages and tracks changes in projects.
* Works with any server, not just GitHub.
* Provides both **CLI** and **GUI** tools.
* Enables **team collaboration** on the same project.
* Supports **reverting changes** when needed.

## Key Concepts

* **Repository (Repo):** Storage for project files and history.
* **Branch:** Independent line of development.
* **Local Repository:** Repository stored on your machine.
* **Remote Repository:** Repository hosted on a server (e.g., GitHub).
* **Commit:** A snapshot of project changes.
* **Clone:** Copying a repository (local or remote) to your machine.

## Common Commands

* **Push:** Upload local commits to the remote repository.
* **Pull:** Fetch and merge changes from remote to local.
* **Pull Request (PR):** Request to merge changes from one branch into another on the remote repository.

## Best Practices

* Create a new repository for each project.
* Use a new branch for each feature or enhancement.
* Manage **push** and **pull** permissions based on roles.
* Use `.md` files (Markdown) for project documentation.

## Code Practices

* **Clone from remote repository:**

  ```bash
  git clone <github_URL>
  ```

* **Initialize a new local repository:**

  ```bash
  git init
  ```

* **Stage changes (add files):**

  ```bash
  git add <file_name>   # Add specific file
  git add .             # Add all files
  ```

* **Check status of staged/unstaged files:**

  ```bash
  git status
  ```

* **Unstage a file (remove from staging area):**

  ```bash
  git reset HEAD <file_name>
  ```

* **Commit changes:**

  ```bash
  git commit -m "Commit message"
  ```

* **Push changes to remote:**

  ```bash
  git push origin <branch_name>
  ```

* **Pull changes from remote:**

  ```bash
  git pull origin <branch_name>
  ```

* **Create and switch to a new branch:**

  ```bash
  git checkout -b <branch_name>
  ```

* **Merge branch into current branch:**

  ```bash
  git merge <branch_name>
  ```

* **List branches / manage branches:**

  ```bash
  git branch
  ```
* **List remote repositories:**

  ```bash
  git remote -v
  ```
