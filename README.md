# theGymnWork
Git is version control tool and Github is cloud based platform to host document and enable collaboration al are built on git. 

## Bundle 1

### squence of commands used for exercise 1



```shell
Admin@Aluxer MINGW64 /f
$ git clone https://github.com/MugemaneBertin2001/theGymnWork.git
Cloning into 'theGymnWork'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
Receiving objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
```
```shell
Admin@Aluxer MINGW64 /f
$ cd theGymnWork/
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ touch sampleFile.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add .
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "Created a file"
[main bbdea25] Created a file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sampleFile.html
 ```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 280 bytes | 140.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MugemaneBertin2001/theGymnWork.git
   b95e24d..bbdea25  main -> main
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ vi sampleFile.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add .
warning: in the working copy of 'sampleFile.html', LF will be replaced by CRLF the next time Git touches it
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "editted file"
[main 8dca45b] editted file
 1 file changed, 13 insertions(+)
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 387 bytes | 387.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MugemaneBertin2001/theGymnWork.git
   bbdea25..8dca45b  main -> main
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout -b dev
Switched to a new branch 'dev'
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git checkout -b test
Switched to a new branch 'test'
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (test)
$ git checkout  dev
Switched to branch 'dev'
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git branch -d test
Deleted branch test (was 8dca45b).
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ echo "<div>Home page</div>" > home.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ cat home.html
<div>Home page</div>
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash
No local changes to save
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git add .
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash
Saved working directory and index state WIP on dev: 8dca45b editted file
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ echo "<div>About page</div>" > about.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git add .
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash
Saved working directory and index state WIP on dev: 8dca45b editted file
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ echo "<div>Team page</div>" > team.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash
Saved working directory and index state WIP on dev: 8dca45b editted file
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash list
stash@{0}: WIP on dev: 8dca45b editted file
stash@{1}: WIP on dev: 8dca45b editted file
stash@{2}: WIP on dev: 8dca45b editted file
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ $ git stash apply stash@{1}
bash: $: command not found
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash apply stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
```


```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash apply stash@{2}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git restore -- stages .
error: pathspec 'stages' did not match any file(s) known to git
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git restore -- staged .
error: pathspec 'staged' did not match any file(s) known to git
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git restore --staged .
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash list
stash@{0}: WIP on dev: 8dca45b editted file
stash@{1}: WIP on dev: 8dca45b editted file
stash@{2}: WIP on dev: 8dca45b editted file
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash pop stash@[1]
error: stash@[1] is not a valid reference
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash pop stash@{1}
error: The following untracked working tree files would be overwritten by merge:
        about.html
Please move or remove them before you merge.
Aborting
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
The stash entry is kept in case you need it again.
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash list
stash@{0}: WIP on dev: 8dca45b editted file
stash@{1}: WIP on dev: 8dca45b editted file
stash@{2}: WIP on dev: 8dca45b editted file
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash pop stash@{2}
error: The following untracked working tree files would be overwritten by merge:
        home.html
Please move or remove them before you merge.
Aborting
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
The stash entry is kept in case you need it again.
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash pop stash@{1}
error: The following untracked working tree files would be overwritten by merge:
        about.html
Please move or remove them before you merge.
Aborting
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
The stash entry is kept in case you need it again.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git add .
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git commit -m "committing stashed files"
[dev dde5f6c] committing stashed files
 2 files changed, 2 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 ```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 391 bytes | 195.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/dev
remote:
To https://github.com/MugemaneBertin2001/theGymnWork.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (6334075741db4213c7ad2e60281fccafcc90caf2)
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ $ git reset --hard commit_hash
bash: $: command not found
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git reset --hard commit_hash
fatal: ambiguous argument 'commit_hash': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git reset --hard
HEAD is now at dde5f6c committing stashed files
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$
```

## Bundle 2

### squence of commands used for exercise 1


```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git branch ft/bundle-2
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ vi service.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git add services.html
fatal: pathspec 'services.html' did not match any files
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git add service.html
warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git commit -m "Add service.html and initial content"
[ft/bundle-2 e9f57b3] Add service.html and initial content
 1 file changed, 13 insertions(+)
 create mode 100644 service.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 398 bytes | 199.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/ft/bundle-2
remote:
To https://github.com/MugemaneBertin2001/theGymnWork.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git merge ft/bundle-2
Updating 8dca45b..e9f57b3
Fast-forward
 README.md    | 365 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html   |   1 +
 home.html    |   1 +
 service.html |  13 +++
 4 files changed, 379 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 8 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MugemaneBertin2001/theGymnWork.git
   8dca45b..e9f57b3  main -> main
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
```

### squence of commands used for exercise 2

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout main
Already on 'main'
M       README.md
Your branch is up to date with 'origin/main'.

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git pull origin main
From https://github.com/MugemaneBertin2001/theGymnWork
 * branch            main       -> FETCH_HEAD
Already up to date.

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git branch ft/service-redesign

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       README.md

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ vi service.html

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git add services.html
fatal: pathspec 'services.html' did not match any files

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git add service.html

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git commit -m "Update service.html for service redesign"
[ft/service-redesign a753a46] Update service.html for service redesign
 1 file changed, 3 insertions(+)

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 339 bytes | 113.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/ft/service-redesign
remote:
To https://github.com/MugemaneBertin2001/theGymnWork.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git push
Everything up-to-date

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add services.html
fatal: pathspec 'services.html' did not match any files

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add service.html

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "Add different changes to services.html in main branch"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add README.md

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "Add different changes to services.html in main branch"
[main 67aa11f] Add different changes to services.html in main branch
 1 file changed, 108 insertions(+)

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.01 KiB | 519.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   e9f57b3..67aa11f  main -> main

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/service-redesign
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add .

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "Readme"
[main 505024b] Readme
 1 file changed, 1 insertion(+), 1 deletion(-)

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 292 bytes | 292.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   67aa11f..505024b  main -> main

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git diff main ft/service-redesign
diff --git a/README.md b/README.md
index 2011d3b..fc3660c 100644
--- a/README.md
+++ b/README.md
@@ -363,111 +363,3 @@ HEAD is now at dde5f6c committing stashed files
 Admin@Aluxer MINGW64 /f/theGymnWork (dev)
 $
 ```
-
-## Bundle 2
-
-### squence of commands used for exercise 1
-
-
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (dev)
-$ git branch ft/bundle-2
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (dev)
-$ git checkout ft/bundle-2
-Switched to branch 'ft/bundle-2'
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ vi service.html
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git add services.html
-fatal: pathspec 'services.html' did not match any files
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git add service.html
-warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git commit -m "Add service.html and initial content"
-[ft/bundle-2 e9f57b3] Add service.html and initial content
- 1 file changed, 13 insertions(+)
- create mode 100644 service.html
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git push
-fatal: The current branch ft/bundle-2 has no upstream branch.
-To push the current branch and set the remote as upstream, use
-
-    git push --set-upstream origin ft/bundle-2
-
-To have this happen automatically for branches without a tracking
-upstream, see 'push.autoSetupRemote' in 'git help config'.
-
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git push --set-upstream origin ft/bundle-2
-Enumerating objects: 4, done.
-Counting objects: 100% (4/4), done.
-Delta compression using up to 4 threads
-Compressing objects: 100% (3/3), done.
-Writing objects: 100% (3/3), 398 bytes | 199.00 KiB/s, done.
-Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
-remote: Resolving deltas: 100% (1/1), completed with 1 local object.
-remote:
-remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
-remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/ft/bundle-2
-remote:
-To https://github.com/MugemaneBertin2001/theGymnWork.git
- * [new branch]      ft/bundle-2 -> ft/bundle-2
-branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (ft/bundle-2)
-$ git checkout main
-Switched to branch 'main'
-Your branch is up to date with 'origin/main'.
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-$ git merge ft/bundle-2
-Updating 8dca45b..e9f57b3
-Fast-forward
- README.md    | 365 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
- about.html   |   1 +
- home.html    |   1 +
- service.html |  13 +++
- 4 files changed, 379 insertions(+), 1 deletion(-)
- create mode 100644 about.html
- create mode 100644 home.html
- create mode 100644 service.html
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-$ git status
-On branch main
-Your branch is ahead of 'origin/main' by 8 commits.
-  (use "git push" to publish your local commits)
-
-nothing to commit, working tree clean
-```
-
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-$ git push
-Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
...skipping...
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
...skipping...
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
-To https://github.com/MugemaneBertin2001/theGymnWork.git
-   8dca45b..e9f57b3  main -> main
-```
-```shell
-Admin@Aluxer MINGW64 /f/theGymnWork (main)
-```
-
-### squence of commands used for exercise 2
\ No newline at end of file
diff --git a/service.html b/service.html
index 256f588..8b6c257 100644
--- a/service.html
+++ b/service.html
@@ -5,6 +5,9 @@
 </head>
 <body>
     <div>
+           <div>
+               changes to service.html
+           </div>
         <h1>Services</h1>
         <p>This is the service page.</p>
     </div>
(END)
