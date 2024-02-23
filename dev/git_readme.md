# Git Cheat-Sheet

## Git Configuration

- Set username: `git config --global user.name "Your Name"`
- Set email: `git config --global user.email "your_email@example.com"`
- List all settings: `git config --list`

## Git Repository

- Initialize a new Git repository: `git init`
- Clone an existing repository: `git clone <repository-url>`

## Git Basic Commands

- Check status: `git status`
- Add changes to staging: `git add <file-or-directory>`
- Commit changes: `git commit -m "Commit message"`
- Pull latest changes from remote: `git pull`
- Push local commits to remote: `git push`

## Branching

- List branches: `git branch`
- Create a new branch: `git branch <branch-name>`
- Switch to a branch: `git checkout <branch-name>`
- Merge a branch into the current branch: `git merge <branch-name>`
- Delete a branch: `git branch -d <branch-name>`

## Stashing

- Stash changes: `git stash`
- List stashes: `git stash list`
- Apply stashed changes: `git stash apply`
- Drop a stash: `git stash drop`

## Viewing Changes

- View changes: `git diff`
- View commit history: `git log`
- View specific commit: `git show <commit-hash>`

## Remote Repositories

- View remote repositories: `git remote -v`
- Add a new remote: `git remote add <remote-name> <remote-url>`
- Remove a remote: `git remote rm <remote-name>`

## Undoing Changes

- Undo unstaged changes: `git checkout -- <file>`
- Reset staged changes: `git reset HEAD <file>`
- Revert a commit: `git revert <commit-hash>`
- Reset to a specific commit: `git reset --hard <commit-hash>`

## Tags

- List tags: `git tag`
- Create a new tag: `git tag <tag-name>`
- Delete a tag: `git tag -d <tag-name>`

## Advanced Git

- Rebase: `git rebase <branch-name>`
- Cherry-pick: `git cherry-pick <commit-hash>`
- Squash commits: `git rebase -i <commit-hash>^`
