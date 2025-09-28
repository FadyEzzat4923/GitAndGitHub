# Git and GitHub

- **Git** is a version control system that manages and tracks changes in projects.
- Works with any server, not just GitHub.
- Provides both **CLI** and **GUI** tools.
- Enables **team collaboration** on the same project.
- Supports **reverting changes** when needed.

## Key Concepts

- **Repository (Repo):** Storage for project files and history.
- **Branch:** Independent line of development.
- **Local Repository:** Repository stored on your machine.
- **Remote Repository:** Repository hosted on a server (e.g., GitHub).
- **Commit:** A snapshot of project changes.
- **Clone:** Copying a repository (local or remote) to your machine.

## Common Commands

- **Push:** Upload local commits to the remote repository.
- **Pull:** Fetch and merge changes from remote to local.
- **Pull Request (PR):** Request to merge changes from one branch into another on the remote repository.

## Best Practices

- Create a new repository for each project.
- Use a new branch for each feature or enhancement.
- Manage **push** and **pull** permissions based on roles.
- Use `.md` files (Markdown) for project documentation.

## Collaboration Workflow

- Go to **Repository Settings** → **Manage Access** → **Add People** to invite collaborators.
- The invited member can then **clone** the repository:

  ```bash
  git clone <github_URL>
  ```

- After making changes, collaborators should always **pull the latest updates** before pushing:

  ```bash
  git pull origin <branch_name>
  ```

## Git Configuration

- **List all configurations:**

  ```bash
  git config --list
  ```

- **List all configurations with file origin:**

  ```bash
  git config -l --show-origin
  ```

- **Set global username:**

  ```bash
  git config --global user.name "Your Name"
  ```

- **Set global email:**

  ```bash
  git config --global user.email "your_email@example.com"
  ```

- **Set local username (per repository):**

  ```bash
  git config user.name "Your Name"
  ```

- **Set local email (per repository):**

  ```bash
  git config user.email "your_email@example.com"
  ```

## Code Practices

- **Clone from remote repository:**

  ```bash
  git clone <github_URL>
  ```

- **Initialize a new local repository:**

  ```bash
  git init
  ```

- **Stage changes (add files):**

  ```bash
  git add <file_name>   # Add specific file
  git add .             # Add all files
  ```

- **Check status of staged/unstaged files:**

  ```bash
  git status
  ```

- **Unstage a file (remove from staging area):**

  ```bash
  git reset HEAD <file_name>
  ```

- **Commit changes:**

  ```bash
  git commit -m "Commit message"
  ```

- **Push changes to remote:**

  ```bash
  git push origin <branch_name>
  ```

- **Pull changes from remote:**

  ```bash
  git pull origin <branch_name>
  ```

- **Create and switch to a new branch:**

  ```bash
  git checkout -b <branch_name>
  ```

- **Merge branch into current branch:**

  ```bash
  git merge <branch_name>
  ```

- **List branches / manage branches:**

  ```bash
  git branch
  ```

- **List remote repositories:**

  ```bash
  git remote -v
  ```

- **Push with upstream tracking (sets default branch for future pushes/pulls):**

  ```bash
  git push -u origin <branch_name>
  ```

After this, you can simply use `git push` or `git pull` without specifying the remote and branch.

- **Rename current branch:**

  ```bash
  git branch -m <new_branch_name>
  ```

- **Merge a branch into the current branch:**

  ```bash
  git merge <branch_name>
  ```
  
## Restoring and Cleaning

* **Unstage a file or all files (move back from staged to unstaged):**

  ```bash
  git restore --staged <file_name>
  git restore --staged *
  ```

* **Show which untracked files will be removed (dry run):**

  ```bash
  git clean -n
  ```

* **Remove untracked files forcefully:**

  ```bash
  git clean -f
  ```

## Reset and Force Push

* **Reset repository to a specific commit (permanently changes history):**

  * Hard reset (discard all changes):

    ```bash
    git reset --hard <commit_hash>
    ```
  * Soft reset (keep changes staged):

    ```bash
    git reset --soft <commit_hash>
    ```

* **Force push changes to the remote repository (overwrite history):**

  ```bash
  git push origin main --force
  ```

## Git Tags

* **List all tags:**

  ```bash
  git tag
  ```

* **Create a lightweight tag:**

  ```bash
  git tag v1.0
  ```

* **Push a specific tag to remote:**

  ```bash
  git push origin v1.0
  ```

* **Create an annotated tag with a message:**

  ```bash
  git tag -a v2.0 -m "Second Version"
  ```

* **List tags matching a pattern:**

  ```bash
  git tag -l "v1.*"
  ```

* **Delete a local tag:**

  ```bash
  git tag -d v2.0
  ```

* **Delete a remote tag:**

  ```bash
  git push origin --delete v2.0
  ```

## Git Aliases

- **Create a shortcut (alias) for a Git command:**

  ```bash
  git config --global alias.<shortcut> <command>
  ```

### Examples

- Alias for `status`:

  ```bash
  git config --global alias.st status
  ```

- Alias for `checkout`:

  ```bash
  git config --global alias.co checkout
  ```

- Alias for `commit`:

  ```bash
  git config --global alias.ci commit
  ```

- Alias for `branch`:

  ```bash
  git config --global alias.br branch
  ```

  ## Git Stash

- **Save uncommitted changes temporarily:**

  ```bash
  git stash
  ```

* **Save changes to a new stash with a custom name/message:**

  ```bash
  git stash save "stash_message"
  ```

- **List all stashes:**

  ```bash
  git stash list
  ```

- **Reapply the most recent stash and remove it from the stash list:**

  ```bash
  git stash pop
  ```

## Git Stash Management

- **Show changes stored in the most recent stash:**

  ```bash
  git stash show
  ```

- **Show changes stored in a specific stash (with index):**

  ```bash
  git stash show "stash@{index}"
  ```

- **Delete the most recent stash:**

  ```bash
  git stash drop
  ```

- **Delete a specific stash (with index):**

  ```bash
  git stash drop "stash@{index}"
  ```

* **Remove all stashes:**

  ```bash
  git stash clear
  ```
