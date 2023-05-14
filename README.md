# theGymnWork
Git is version control tool and Github is cloud based platform to host document and enable collaboration al are built on git. 

## squence of commands used



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
The stash entry is kept in case you need it again.```

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
$ git add .```

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
