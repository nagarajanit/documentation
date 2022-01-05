> # Git Global Configurations
- `git config --flobal user.name "<<name>>"`
- `git config --global user.email <<emailid>>`
- `git config --global core.editor "code --wait" - Setting Default Editor to VSCode`
- `git config --global diff.tool vscode - Setting VSCode for diff tool`
- `git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"` 
>**Note: Sometimes $Local $Remote might have not got added. Please check using command(git config --global -e) and update it accordingly**
- `git config --global -e - View/Edit git settings`

---

# Git Commands
| Commands | Description |
| ----------- | ----------- |
| git init | Initializing git repository |
| git add . | adding all file to staging area |
| git add `<<file1>> <<file2>>` | adding file1 &file2 to staging area |
| git rm `<<file1>> <<file2>>` | removes files from working directory & staging area |
| git mv `main.js file1.js` | rename files from working directory & staging area |
| git status | list the pending changes (i.e. modified and created file) |
| git status -s | short status. There are two columns before the file names. first column to represent staging area and second column represents working directory  |
| git difftool | It will bring up unstaged stages(i.e. differences between working directory and Staging area) |
| git difftool --staged | It will bring up staged stages(i.e. differences between staging are directory and last commit) |
| git log | Viewing detailed commits includes commit ID, description,changes,author |
| git log --oneline | Viewing commits in one line with commit ID and description |
| git log --oneline --all | List all the commits that includes across the branch |
| git log --oneline --reverse | Viewing commits in one line with commit ID and description 
| git log --oneline --author="Mosh" | Filters the logs with the commit made by the author "Mosh" |
| git log --oneline --after="2020-08-17" | Filters the logs with the commit after the date Aug 17, 2020 |
| git log --oneline --grep="GUI" | Filters the logs with the commit message containing "GUI". Note: Filter keyword is a case sensitive |
| git log --oneline --S"hello()" | Filters the logs has the commits content with added/removed function declaration(hello()) |
| git log --oneline --S"OBJECTIVES" | Filters the logs has the commits content with "OBJECTIVES" |
| git log --oneline --toc.txt | Filters the commits which touches the file "toc.txt" |
| git log --oneline --patch --toc.txt | Filters & view the commits in detail which touches the file "toc.txt" |
| git log master..bugfix | List the commits that are present in bugfix branch but not in master |
| git diff master..bugfix | List the changes between bugfix and master branch |
| git diff --name-only master..bugfix | If you want to see only the file names that are changed |
| git show HEAD~2 (or) git show `<<commit id>>` | Viewing the particular commit |
| git show HEAD~2:sections/creation-snapshots/staged-changes.txt | view a file under the particular commit. Note: sections/creation-snapshots/staged-changes.txt is a file path   |
| git show HEAD~2 --name-only | List all the files modified under the commit  |
| git show HEAD~2 --name-status | List all the files with the status(i.e. added/modified/deleted) modified under the commit  |
| git diff HEAD~2 HEAD | Differences between current Head and 2 commits back |
| git diff HEAD~2 HEAD audience.txt | Difference of a file change(audience.txt) between these two commits |
| git diff HEAD~2 HEAD --name-only | list of the file changes between these two commits |
| git checkout `<<commitid>>` | checking out a particular commit. Note: you would see a warning message "Head is in detached state" which is okay.You must use this only checkout the files and view the changes for that particular commit.|
| git branch -m `<<old branch name>>` `<<new branch name>>` | renaming local branch|
| git restore --staged `<<file>>` | revert the changes from next environment |
| git commit -m `<<message>>` | commiting a file |
| git switch -c `<<new branch name>>` | Create a branch and switch to new branch |
| git switch `<<branch name>>` | switch to branch |
| git branch -d `<<branch name>>` | delete a branch |
| git branch --merged | view the list of merged branches |
| git branch --no-merged | view the list of unmerged branches |
| git switch master, git merge `<<branch name>>` | merging branch to master |
| git merge --abort | Aborting merge |
| git reset --hard HEAD~ `<<index>>` | undoing faulty merge if changes has not been pushed to master |
| git revert -m 1 HEAD | if changes are already merged into github and you want to revert your commit then you need to apply new commit |
| git switch `<<branch name>>`, git rebase master | you wanted to rebase your branch with the latest changes of master or the branch you are interested in, then use both commands. Example: First switch to bugfix branch and then apply rebase to master branch. Sometimes, you will endup with conflict, resolve that conflict |
| git switch `<<branch name>>`, git rebase master, git rebase --continue | Sometimes, you will endup with conflict, resolve that conflict and apply git rebase --continue |
| git rebase --abort | you are in middle of rebase and you wanted to abort the rebase |
| git switch master, git cherry-pick `<<commitid>>` | you wanted to apply one specific commit from feature branch to master branch, then use cherry-pick |
| git fetch, git merge origin/master | git fetching, git merge. By doing this, we are not disturbing the remote changes directly to our local master. Git fetching pulls the commit and have the commits points to origin/master. And then, when we do merge commit, our local & remote commits gets merged. Sometimes, you need to fetch the commits only from particular remote branch, then you use this cmd(git fetch origin `<<branch name>>`) |
| git pull --rebase | git pulling(fetch+merge) |
| git push | pushing changes to github |
| git stash push -am `"comment"` | stashing changes to a safe place. -am includes if you have any new files |
| git stash list | List the stash |
| git stash show `<<index>>` | Before applying stash files, if you want to view the changes. index could be 0 or 1 or so on... |
| git stash apply `<<index>>` | Applying the stash from 0 or 1 index |
| git stash drop `<<index>>` | After applying, we need to drop that stash index |
| git stash clear | Clears all the stash |



