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
```shell
Admin@Aluxer MINGW64 ~
$ f:
bash: f:: command not found
```
```shell
Admin@Aluxer MINGW64 ~
$ cd f:
```
```shell
Admin@Aluxer MINGW64 /f
$ cd  theGymnWork/
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git add .
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git commit -m "changes on ^C
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git commit -m "ft/service-redesign"
[ft/service-redesign 358d21d] ft/service-redesign
 1 file changed, 848 insertions(+)
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 3.67 KiB | 1.83 MiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   a753a46..358d21d  ft/service-redesign -> ft/service-redesign
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
```
```shell

Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git merge ft/service-redesign
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main|MERGING)
$ git add .
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main|MERGING)
$ git status
On branch main
Your branch is up to date with 'origin/main'.
```
```shell
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   README.md
        modified:   service.html

```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main|MERGING)
$ git commit -m "After merge"
[main b712f11] After merge
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
```
```shell
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   505024b..b712f11  main -> main
```


## Bundle 3

### squence of commands used for exercise 1

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git branch ft/team-page
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ vi team.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git add team.html
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git commit -m "added team.html"
[ft/team-page 0b54550] added team.html
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 409 bytes | 409.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/ft/team-page
remote:
To https://github.com/MugemaneBertin2001/theGymnWork.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git branch ft/contact-page
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/team-page)
$ git log
commit 0b545502f4adfd85cb63ee035dd10957a1752835 (HEAD -> ft/team-page, origin/ft/team-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 20:00:41 2023 +0200

    added team.html

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:

commit fd0e046f6e322050737c7b41b2a07598bcc26c48 (origin/main, origin/HEAD, main, ft/contact-page)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 19:54:34 2023 +0200

    README.md rearrangement

commit b712f1180d7d8589f5e52d45a6e2d77d125f465a
Merge: 505024b 358d21d
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:52:56 2023 +0200

    After merge

commit 358d21d074688c66918526d7cb3e559506c892ba (origin/ft/service-redesign, ft/service-redesign)
Author: bertin <bertin.m2001@gmail.com>
Date:   Thu May 18 17:51:24 2023 +0200

    ft/service-redesign

commit 505024b6e8342c9b95c04d6cb2455984c32bc69f
:
```
## Bundle 3

### squence of commands used for exercise 2

```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git branch ft/home-page-redesign ft/faq-page
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git add .
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git commit -m "ordering README.md
> "
[ft/faq-page bfb942b] ordering README.md
 1 file changed, 198 insertions(+), 11 deletions(-)
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.56 KiB | 798.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   2cb2ffb..bfb942b  ft/faq-page -> ft/faq-page
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/faq-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ echo "some changes on main branch "> changes.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git add .
warning: in the working copy of 'changes.html', LF will be replaced by CRLF the next time Git touches it
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git commit -m "some changes on main branch"
[main 5a9ec38] some changes on main branch
 1 file changed, 1 insertion(+)
 create mode 100644 changes.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   fd0e046..5a9ec38  main -> main
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git add .
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git commit -m "commit after rebase "
On branch ft/home-page-redesign
nothing to commit, working tree clean
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 2.51 KiB | 642.00 KiB/s, done.
Total 12 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/MugemaneBertin2001/theGymnWork/pull/new/ft/home-page-redesign
remote:
To https://github.com/MugemaneBertin2001/theGymnWork.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git rebase --continue
fatal: No rebase in progress?
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git rebase main
Current branch ft/home-page-redesign is up to date.
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ ls
README.md   changes.html  faq.html   sampleFile.html
about.html  contact.html  home.html  service.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ vi home.html
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git add .
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git commit -m "some changes on home page"
[ft/home-page-redesign 4fa1b71] some changes on home page
 1 file changed, 1 insertion(+)
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 301 bytes | 150.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/MugemaneBertin2001/theGymnWork.git
   d2508f1..4fa1b71  ft/home-page-redesign -> ft/home-page-redesign
```
```shell
Admin@Aluxer MINGW64 /f/theGymnWork (ft/home-page-redesign)
```