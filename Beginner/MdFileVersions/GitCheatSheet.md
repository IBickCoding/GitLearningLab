# Git Quick Reference Guide

> This is a cheat sheet for some of the commands for Git. It is not comprehensive, but it is inclusive of many of the commands you will use. If you don't know what a command does, you should learn it before using it as some are destructive in nature.

## 1. Repository Setup

| Command | Description | Common Flags |
|---|---|---|
| `git init` | Create a new Git repository. | - |
| `git clone <url>` | Copy an existing repository locally. | - |
| `git config user.name "Name"` | Set your Git username in the current repository. | `--global` Apply to all repositories |
| `git config user.email "email"` | Set your Git email in the current repository. | `--global` Apply to all repositories |
| `git config --list` | View active Git configuration. | - |

## 2. Inspect Repository

| Command | Description | Common Flags |
|---|---|---|
| `git status` | Show working tree and staging status. | `-s` short form; `-b` branch info |
| `git diff` | View unstaged changes. | `--stat` view changes to each file in a more user friendly format |
| `git diff --staged` | View staged changes. | - |
| `git show` | Show details for a commit/object. | `<hash>` specific object's details |
| `git log` | View commit history. | `--oneline` each entry condesnsed to one line, `--graph` "graphical" view, `--all` show all references |
| `git blame <filename>` | Show last author for each line. | - |

## 3. Stage Changes

| Command | Description | Common Flags |
|---|---|---|
| `git add <file>` | Stage a file. | - |
| `git add .` | Stage changes in current directory and its subdirectories. | - |
| `git add -A` | Stage all changes across the repository. | - |
| `git mv <old filename> <new filename>` | Move/rename tracked file. | - |
| `git rm <filename>` | Remove tracked file. | `--cached` keep a local copy |
| `git restore <filename>` | Discard unstaged changes. | - |
| `git restore --staged <filename>` | Unstage a file. | - |

## 4. Commits

| Command | Description | Common Flags |
|---|---|---|
| `git commit` | Create a commit. | `-m` create a commit message |
| `git commit -m "msg"` | Commit with inline message. | - |
| `git commit -a -m "msg"` | Stage modified tracked files and commit. | - |
| `git commit --amend` | Modify the previous commit. | - |

## 5. Branching

| Command | Description | Common Flags |
|---|---|---|
| `git branch` | List branches. | `-a` all branches, `-r` remote-tracking branches, `-m <new name>` renames current branch|
| `git switch <branch>` | Switch branches. | `-c` creates and swaps to that branch |
| `git merge <branch>` | Merge another branch. | - |
| `git rebase <branch>` | Apply commits on current branch and replay them over the designated branch. | - |
| `git branch -d <branch>` | Delete merged branch. | `-D` force delete branch |

## 6. Remotes

| Command | Description | Common Flags |
|---|---|---|
| `git remote` | List remotes. | `-v` URLs included |
| `git remote add origin <url>` | Add remote named origin with the given URL. | - |
| `git fetch` | Download remote changes. | `--all` fetch from all configured remotes |
| `git pull` | Fetch then merge. | `origin, upstream, etc` pull changes for specific remote |
| `git push` | Push current branch. | `origin, upstream, etc` push changes for specific remote |

## 7. Stash

| Command | Description | Common Flags |
|---|---|---|
| `git stash` | Save work temporarily. | `-u` include untracked work |
| `git stash list` | List all stashed changes. | - |
| `git stash apply` | Apply most recent stash without deleting it. | - |
| `git stash pop` | Apply, then remove most recent stashed changes. | - |
| `git stash drop` | Delete the most recent stashed changes. | - |

## 8. Undo Changes

| Command | Description | Common Flags |
|---|---|---|
| `git reset` | Unstage changes and move HEAD. | `--soft` moves HEAD but keeps all changes; `--mixed` moves HEAD, resets staging area, but keeps working files; `--hard` moves HEAD, resets staging area, changes files to match the commit. |
| `git revert <commit>` | Create commit that undoes another commit. | - |

## 9. History

| Command | Description | Common Flags |
|---|---|---|
| `git reflog` | View HEAD history. | - |
| `git log --graph --oneline --all` | Visualize commit graph. | - |

## 10. Tags

| Command | Description | Common Flags |
|---|---|---|
| `git tag` | List tags. | - |
| `git tag -a v1.0 -m "msg"` | Create annotated tag. | - |
| `git tag -d <tag>` | Delete tag. | - |
| `git push --tags` | Push all tags. | - |

## 11. Git Internals

| Command | Description |
|---|---|
| `git cat-file -p <object>` | Inspect Git objects. |
| `git ls-files` | List tracked files. |
| `git ls-tree <tree>` | Show tree contents. |
| `git hash-object <filename>` | Compute Git object hash. |

## Safety Notes

- `git reset --hard` permanently discards uncommitted work.
- `git commit -a` does **not** stage new untracked files.
