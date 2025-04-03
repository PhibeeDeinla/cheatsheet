# Git CheatSheet

## Basics

### Cloning

- clone GitHub Repository url

```bash
git clone <github-repo-url>
```

### Pulling

- Pull all updates on (remote) branch

```bash
git pull <branch-name>
```

### Pushing

- Push all local Commit(s) to remote branch

```bash
git push origin <branch-name>
```

### Add to Stage

- Add all files to Staged state

```bash
git add . # dot (.) means all
```

- Add specific file to Staged state

```bash
git add <file>
```

### Status

- See Status or State of file(s)

```bash
git status
```

### Commits

- Commit file(s) from Unstaged to Staged state

```bash
git commit -m"Message here"
```

### Branching

- Create new (local) branch

```bash
git branch <branch-name> # ex. git branch task/001
```

- Create new (local) branch, but switch to it immediately

```bash
git checkout -b <branch-name>
```

- Go to specific branch

```bash
git checkout <branch-name>
```

- See both remote and local branch

```bash
git branch -a
```

- See all (remote) branch

```bash
git branch -r
```

- See all (local) branch

```bash
git branch
```

### Reset

- Reset Staged file(s) to Unstaged state.

```bash
git reset .  # all files in the current directory
# or
git reset <file>
```

### Checkout

- Revert all changes for Unstaged file(s) to it's Unmodified state.

> <b>BE CAUTIOUS:</b> <br/>means it will <b>DELETE / REMOVE</b> your changes

```bash
git checkout . # all files in the current directory
# or
git checkout <file>
```

### Stash

- Stash all Staged/UnStaged file(s) branch `-u` means including untracked file(s)

```bash
git stash save -m"Stash Message" -u
```

- See all Stash list

```bash
git stash list
```

### Fetching

- Fetch all (remote) branch

```bash
git fetch --all
# or
git fetch origin
```

### Log

- See All Commit history (includes only Commit Hash, Author and Message)

```bash
git log
```

- See Commit History in Graph, If you don't need branch or tag name:

```bash
git log --oneline --graph --all --no-decorate
```

- See Commit History in Graph, If you don't even need color (to avoid tty color sequence):

```bash
git log --oneline --graph --all --no-decorate --no-color
```

### Configs

- Modify Git Configs

```bash
# use `--global` global directory
git config --global user.email "your_email@example.com" # corresponds to your GitHub Email
git config --global user.name "ExampleName" # corresponds to your GitHub UserName

# use `--local` current or specific directory
git config --local user.email "your_email@example.com"
git config --local user.name "ExampleName"
```

## Advanced

### Merge Branch

- to merge specific branch to (local) current branch

```bash
git merge <branch-name>
```

### Reverting Commits

- to revert specific commit, normally for commits alread pushed remote

```bash
git revert <SHA-1> # SHA-1 corresponds to hash of specific commit history
```

### Reset to previous Commits

- to revert specific commit, normally for commits alread pushed remote

```bash
git reset --soft HEAD~{N} # N corresponds to number of steps backward
```

- to undo, git reset applied

```bash
git reset 'HEAD@{1}'
```

### Pick Commits

- to pick specific commit or changes then applying it to current branch

```bash
git cherry-pick <SHA-1> # SHA-1 corresponds to hash of specific commit history from any branch
```

### Deleting Untracked file(s)

> <b>BE CAUTIOUS:</b>

- to <b>DELETE</b> untracked or new file(s) in your current directories

```bash
git clean -d -f
```

### Deleting Branch

- to remove a (local) branch only from your machine:

```bash
git branch -d <local-branch-name>
```

> <b>BE CAUTIOUS:</b>

- to remove a (remote) branch; but it's better manually remove it on GitHub instead, if needed.

```bash
git push origin -d <remote-branch-name>
```
