| Getting Started With A Repository |  |  |
|----|----|----|
| Command Number | Command | Command Description |
| 1 | git init | Initialize a new Repository |
| 2 | git clone | Clone an exisiting Repository |
|  |  |  |
| Preparing to Commit Work to the Repository |  |  |
| Command Number | Command | Command Description |
| 1 | git add \<file_name\> | Add an untracked file or unstaged changes |
| 2 | git add . | Add all untracked file or unstaged changes |
| 3 | git add -p | Chose which parts of a file to stage |
| 4 | git mv \<old\> \<new\> | Move the file |
| 5 | git rm \<file_name\> | Delete the indicated file |
| 6 | git rm --cached \<file_name\> | Tell Git to forget about the file without deleteing it |
| 7 | git reset \<file_name\> | Unstage a file |
| 8 | git reset | Unstage all files |
| 9 | git status | Check repository status and staging area. |
|  |  |  |
| Make Commits |  |  |
| Command Number | Command | Command Description |
| 1 | git commit | Make a commit (and open text editor to write message) |
| 2 | git commit -m 'message' | Make a commit and comment message |
| 3 | git commit -am 'message' | Commit all unstaged changes and comment message |
|  |  |  |
| Move Between Branches |  |  |
| Command Number | Command | Command Description |
| 1 | git switch \<name_of_branch\> or git checkout \<name_of_branch\> | Switch branches |
| 2 | git branch | Lists Branches |
| 3 | git branch --sort=-committerdate | List Branches bt most recently commited to |
| 4 | git switch -c \<name_of_branch\> or git checkout -b \<name_of_branch\> | Create a Branch |
| 5 | git branch -d \<name_of_branch\> | Delete a Branch |
| 6 | git branch -D \<name_of_branch\> | Force Delete a Branch |
|  |  |  |
| Pushing Changes and Commits |  |  |
| Command Number | Command | Command Description |
|  | git push origin main | Push the main branch to the remote origin |
|  | git push | Push the current branch to its remote "tracking branch" |
|  | git push -u origin \<name_of_branch\> | Push a branch tha you’ve never pushed before |
|  | git push --force-with-lease | Force Push |
|  | git push --tags | Push Tags |
|  |  |  |
| Pull Changes and Commits |  |  |
| Command Number | Command | Command Description |
|  | git fetch origin main | Fetch changes(but don’t change any of your local branches) |
|  | git pull --rebase | Fetch changes and then rebase your current branch |
|  | git pull origin main or git pull | Fetch changes and then merge them into your current branch |
|  |  |  |
| Configure Git |  |  |
| Command Number | Command | Command Description |
|  | git config user.name 'Your Name' | Set your user name |
|  | man git-config | See all availble configuration options |
|  | git config alias.st status | Add an alias |
|  |  |  |
| Discard Changes |  |  |
| Command Number | Command | Command Description |
|  | git restore \<name_of_file\> or git checkout \<name_of_file\> | Delete unstaged changes to one file |
|  | git restore --staged --worktree \<name_of_file\> or git checkout HEAD \<name_of_file\> | Delete all staged and unstaged changes to one file |
|  | git reset --hard | Delete all staged and unstaged changes |
|  | git clean | Delete untracked files |
|  | git stash | Stash' all staged and unstaged changes |
|  |  |  |
| Code Structure |  |  |
| Command Number | Command | Command Description |
|  | git log main or git log --graph main or git log --oneline | Look at a branch's history |
|  | git log -follow \<name_of_file\> | Shows every commit that modified a file, including before it was renamed |
|  | git log \<name_of_file\> | Show every commit that modified a file |
|  | git log -G banana | Find every commit that added or removed some text |
|  | git blame \<name_of_file\> | Show who last changed each line of a file |
|  |  |  |
|  |  |  |
