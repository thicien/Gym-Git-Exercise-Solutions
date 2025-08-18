# Gym-Git-Exercise-Solutions

## bundle1

### exercise1
```bash 
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