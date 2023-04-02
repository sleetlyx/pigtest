# pigtest
 新的  本地分支提交文件
 liyongxing@sleet MINGW64 /d/temp/gitpro
$ echo "# pigtest" >> README.md

liyongxing@sleet MINGW64 /d/temp/gitpro
$ git init
Initialized empty Git repository in D:/temp/gitpro/.git/

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git starus
git: 'starus' is not a git command. See 'git --help'.

The most similar command is
        status

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git commit -m "first commit"
[master (root-commit) dc0f663] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git branch -M main

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git remote add origin https://github.com/sleetlyx/pigtest.git

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git remote
origin

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git remote master
error: unknown subcommand: `master'
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename [--[no-]progress] <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand


liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch master

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git remote
origin

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch
* main
  master

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git checkout -b master origin/master
fatal: 'origin/master' is not a commit and a branch 'master' cannot be created from it

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch master
fatal: a branch named 'master' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git checkout -b master
fatal: a branch named 'master' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 221 bytes | 221.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/sleetlyx/pigtest.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -M lyx

liyongxing@sleet MINGW64 /d/temp/gitpro (lyx)
$ git branch
* lyx
  master

liyongxing@sleet MINGW64 /d/temp/gitpro (lyx)
$ git checkout -b main
Switched to a new branch 'main'

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch lyx
fatal: a branch named 'lyx' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -M lyx

liyongxing@sleet MINGW64 /d/temp/gitpro (lyx)
$ git branch
* lyx
  master

liyongxing@sleet MINGW64 /d/temp/gitpro (lyx)
$ git branch  -r
  origin/main

liyongxing@sleet MINGW64 /d/temp/gitpro (lyx)
$ git checkout master
Switched to branch 'master'

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git remote add master https://github.com/sleetlyx/pigtest.git

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git branch -r
  origin/main

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git status
On branch master
nothing to commit, working tree clean

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git branch -a
  lyx
* master
  remotes/origin/main

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ vim README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git commit -m "master 提交"
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")


liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git commit -m "master 提交"
[master 442c56d] master 提交
 1 file changed, 1 insertion(+)

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git push -u origin master
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 297 bytes | 297.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/sleetlyx/pigtest/pull/new/master
remote:
To https://github.com/sleetlyx/pigtest.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git branch -a
  lyx
* master
  remotes/origin/main
  remotes/origin/master

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git chekout -b main
git: 'chekout' is not a git command. See 'git --help'.

The most similar command is
        checkout

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git checkout -b main
Switched to a new branch 'main'

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git status
On branch main
nothing to commit, working tree clean

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -a
  lyx
* main
  master
  remotes/origin/main
  remotes/origin/master

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ vim README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch lyx
fatal: a branch named 'lyx' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ gti branch
bash: gti: command not found

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ gti branch
bash: gti: command not found

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch
  lyx
* main
  master

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch master
fatal: a branch named 'master' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -m master
fatal: a branch named 'master' already exists

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -d master
Deleted branch master (was 442c56d).

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -a
  lyx
* main
  remotes/origin/main
  remotes/origin/master

liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git branch -b master
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-f] [--recurse-submodules] <branch-name> [<start-point>]
   or: git branch [<options>] [-l] [<pattern>...]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --verbose         show hash and subject, give twice for upstream branch
    -q, --quiet           suppress informational messages
    -t, --track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --set-upstream-to <upstream>
                          change the upstream info
    --unset-upstream      unset the upstream info
    --color[=<when>]      use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --abbrev[=<n>]        use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --delete          delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --move            move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    -c, --copy            copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --list            list branch names
    --show-current        show current branch name
    --create-reflog       create the branch's reflog
    --edit-description    edit the description for the branch
    -f, --force           force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --column[=<style>]    list branches in columns
    --sort <key>          field name to sort on
    --points-at <object>  print only branches of the object
    -i, --ignore-case     sorting and filtering are case insensitive
    --recurse-submodules  recurse through submodules
    --format <format>     format to use for the output


liyongxing@sleet MINGW64 /d/temp/gitpro (main)
$ git  checkout -b master
Switched to a new branch 'master'

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git status
On branch master
nothing to commit, working tree clean

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ vim README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ ls
README.md

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

liyongxing@sleet MINGW64 /d/temp/gitpro (master)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced 
