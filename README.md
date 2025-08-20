# Gym-Git-Exercise-Solutions

## bundle1

### exercise1
```bash 
PS C:\Users\user\Desktop\git-exercises> mkdir git-exercises
PS C:\Users\user\Desktop\git-exercises> cd git-exercises
PS C:\Users\user\Desktop\git-exercises> git init
PS C:\Users\user\Desktop\git-exercises> echo "git-exercises" > Gym-Git-Exercise-solutions
PS C:\Users\user\Desktop\git-exercises> echo "<p>this is my paragrath </p>" >  index.html
PS C:\Users\user\Desktop\git-exercises> git add README.md index.html
PS C:\Users\user\Desktop\git-exercises> git commit -m "Add README.md and index.html"
PS C:\Users\user\Desktop\git-exercises> git branch
PS C:\Users\user\Desktop\git-exercises> git branch -M main
PS C:\Users\user\Desktop\git-exercises> git branch -m main master
PS C:\Users\user\Desktop\git-exercises> git branch -m master main
PS C:\Users\user\Desktop\git-exercises> git add .
PS C:\Users\user\Desktop\git-exercises> git branch
* main
PS C:\Users\user\Desktop\git-exercises> git fetch origin
PS C:\Users\user\Desktop\git-exercises> git checkout ft/bundle-1
PS C:\Users\user\Desktop\git-exercises> git branch
* ft/bundle-1
  main
PS C:\Users\user\Desktop\git-exercises> git add .
PS C:\Users\user\Desktop\git-exercises> git commit -m "files added"
[ft/bundle-1 2a7b8b7] files added
 1 file changed, 1 insertion(+)
 create mode 160000 Gym-Git-Exercise-Solutions
PS C:\Users\user\Desktop\git-exercises> git push
```


```bash
PS C:\Users\user\Desktop\git-exercises> git branch
* ft/bundle-1
  main
PS C:\Users\user\Desktop\git-exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\user\Desktop\git-exercises> git branch 
* dev
  ft/bundle-1
  main
PS C:\Users\user\Desktop\git-exercises> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\user\Desktop\git-exercises> git branch
  dev
  ft/bundle-1
  main
* test
PS C:\Users\user\Desktop\git-exercises> git status
On branch test
PS C:\Users\user\Desktop\git-exercises> git checkout dev
M       Gym-Git-Exercise-Solutions
Switched to branch 'dev'
PS C:\Users\user\Desktop\git-exercises> git branch -d test
Deleted branch test (was 2a7b8b7).
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
```

### exercise 2
```bash
PS C:\Users\user\Desktop\git-exercises> @"<!DOCTYPE html><html><head><title>Home Page</title></head><body><h1>Welcome to the Home Page</h1><p>This is a new page created for Git exercises.</p></body></html>"@ > home.html
PS C:\Users\user\Desktop\git-exercises> git status
PS C:\Users\user\Desktop\git-exercises> git add home.html
PS C:\Users\user\Desktop\git-exercises> git stash save "Added home.html file with some contents"
PS C:\Users\user\Desktop\git-exercises> @"<!DOCTYPE html><html><head><title>About Page</title></head><body><h1>About Us</h1><p>This page contains information about our project.</p></body></html>"@ > about.html
PS C:\Users\user\Desktop\git-exercises> git add about.html
PS C:\Users\user\Desktop\git-exercises> git stash save "Added about.html file with some content"
PS C:\Users\user\Desktop\git-exercises> <!DOCTYPE html><html><head><title>Team Page</title></head><body><h1>Our Team</h1><p>This page introduces the team members.</p></body></html> team.html
PS C:\Users\user\Desktop\git-exercises> git add team.html
PS C:\Users\user\Desktop\git-exercises> git stash save "Added team.html file with some contents"
PS C:\Users\user\Desktop\git-exercises> git stash push home.html
No local changes to save
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\user\Desktop\git-exercises> git stash push -u home.html
No local changes to save
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
PS C:\Users\user\Desktop\git-exercises> git stash push home.html
Saved working directory and index state WIP on dev: 0767b95 players added
PS C:\Users\user\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 0767b95 players added
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev 
PS C:\Users\user\Desktop\git-exercises> git stash push about.html
Saved working directory and index state WIP on dev: 0767b95 players added
PS C:\Users\user\Desktop\git-exercises> git stash list
stash@{0}: WIP on dev: 0767b95 players added
stash@{1}: WIP on dev: 0767b95 players added
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
PS C:\Users\user\Desktop\git-exercises> git add .
PS C:\Users\user\Desktop\git-exercises> git commit -m "done"
On branch dev
nothing to commit, working tree clean
PS C:\Users\user\Desktop\git-exercises> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\Desktop\git-exercises> git push origin dev
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1.27 KiB | 648.00 KiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/thicien/Gym-Git-Exercise-Solutions.git
   bca9e5d..0767b95  dev -> dev
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\Desktop\git-exercises> git stash push team.html
Saved working directory and index state WIP on dev: 0767b95 players added
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html
        modified:   home.html
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\Desktop\git-exercises> git restore team.html
PS C:\Users\user\Desktop\git-exercises> git restore home.html
PS C:\Users\user\Desktop\git-exercises> git restore about.html
PS C:\Users\user\Desktop\git-exercises> git push origin dev
Everything up-to-date
PS C:\Users\user\Desktop\git-exercises> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\user\Desktop\git-exercises> git push origin dev
Everything up-to-date
PS C:\Users\user\Desktop\git-exercises> 
 *  History restored 
gitPS C:\Users\user\Desktop\git-exercises> git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Gym-Git-Exercise-Solutions (modified content)

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\Desktop\git-exercises> git add .
PS C:\Users\user\Desktop\git-exercises> git commit -m "tracked"
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Gym-Git-Exercise-Solutions (modified content)

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\Desktop\git-exercises> git add .
PS C:\Users\user\Desktop\git-exercises> git commit -m "full"
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   Gym-Git-Exercise-Solutions (modified content)

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\user\Desktop\git-exercises>