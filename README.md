# Jcodes_GitCMD_Book

# Git CLI Command Reference

A curated list of useful Git commands for everyday workflows, debugging, branching, and more.

---

## Setup & Configuration

```
git config --global user.name "Your Name"        # Set your global username
git config --global user.email "you@example.com" # Set your global email
git config --list                                 # List all config settings
git init                                         # Initialize a new Git repository
```

## Basic Workflow

```
git clone <repo_url>         # Clone a remote repository locally
git status                   # Check repository status
git add <file>               # Stage changes for commit
git add .                    # Stage all changes
git commit -m "message"      # Commit staged changes with a message
git commit --amend           # Amend last commit (e.g. fix message)
git push origin <branch>     # Push commits to remote branch
git pull origin <branch>     # Fetch and merge remote changes
```

## Branching & Merging

```git branch                   # List local branches
git branch -a                # List all branches (local & remote)
git branch <branch_name>     # Create a new branch
git checkout <branch_name>   # Switch to another branch
git switch <branch_name>     # Alternative to checkout for branch switching
git checkout -b <branch>     # Create & switch to new branch
git merge <branch_name>      # Merge a branch into current branch
git rebase <branch_name>     # Rebase current branch onto another branch
git branch -d <branch_name>  # Delete local branch
git push origin --delete <branch_name>  # Delete remote branch
```

## History & Logs

```
git log                     # Show commit history
git log --oneline           # Compact single-line commits
git log --graph --oneline   # Show branch graph with commits
git diff                    # Show unstaged changes
git diff --staged           # Show staged changes
git show <commit_hash>      # Show details of a commit
git blame <file>            # Show line-by-line last change info
git reflog                  # Show history of HEAD changes (useful for recovery)
```

## Undo & Recovery

```
git reset <file>            # Unstage file changes
git reset --hard HEAD       # Discard all local changes
git checkout -- <file>      # Discard changes in working directory for a file
git revert <commit_hash>    # Create a new commit that reverses a previous commit
git bisect start            # Start a binary search to find a bad commit
git bisect good <commit>    # Mark a commit as good during bisect
git bisect bad <commit>     # Mark a commit as bad during bisect
git bisect reset            # End bisect session
```



## Remote Repositories

```
git remote -v               # Show remote URLs
git remote add <name> <url> # Add a new remote
git fetch <remote>          # Fetch changes from remote without merging
git pull                    # Fetch and merge remote changes
git push                    # Push changes to remote
```

## Tags

```
git tag                     # List tags
git tag <tag_name>          # Create a tag
git push origin <tag_name>  # Push tag to remote
git push origin --tags      # Push all tags to remote
```

## Advanced & Useful

```
git stash                   # Stash changes for later
git stash pop               # Apply stashed changes and remove stash
git stash list              # List stashes
git cherry-pick <commit>    # Apply a commit from another branch
git worktree add <path> <branch>  # Check out multiple branches simultaneously
git submodule update --init --recursive  # Initialize and update submodules
git clean -fd               # Remove untracked files and directories
```

## Helpful Aliases (Add these with git config)

```
git config --global alias.co checkout      # Use 'git co' instead of 'git checkout' (switch branches or files)
git config --global alias.br branch        # Use 'git br' instead of 'git branch' (list, create, or delete branches)
git config --global alias.ci commit        # Use 'git ci' instead of 'git commit' (commit changes)
git config --global alias.st status        # Use 'git st' instead of 'git status' (check current working state)
git config --global alias.lg "log --oneline --graph --all"  # Use 'git lg' to see a visual commit graph across all branches
```

