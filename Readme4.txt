
Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4 (master)
$ git clone "https://github.com/11812142/GitDemo.git"
Cloning into 'GitDemo'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 12 (delta 1), reused 9 (delta 1), pack-reused 0
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (1/1), done.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4
$ cd GitDemo

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git branch
* master

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ dir
welcome.txt

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git branch GitWork

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git branch
  GitWork
* master

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git checkout GitWork
Switched to branch 'GitWork'

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ dir
welcome.txt

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ touch hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ dir
hello.xml  welcome.txt

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ cat hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ notepad hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ git status
On branch GitWork
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.xml

nothing added to commit but untracked files present (use "git add" to track)

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ git add .

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ git commit -m 'Commit the changes'
[GitWork 0e4f03d] Commit the changes
 1 file changed, 1 insertion(+)
 create mode 100644 hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ git status
On branch GitWork
nothing to commit, working tree clean

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (GitWork)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ cat hello.xml
cat: hello.xml: No such file or directory

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ touch hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ cat hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ notepad hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.xml

nothing added to commit but untracked files present (use "git add" to track)

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git add .

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git commit -m 'Commit the changes in the master'
[master 255a99e] Commit the changes in the master
 1 file changed, 1 insertion(+)
 create mode 100644 hello.xml

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git log --oneline --graph --decorate  --all
* 255a99e (HEAD -> master) Commit the changes in the master
| * 0e4f03d (GitWork) Commit the changes
|/
* 0b6b3d6 (origin/master, origin/HEAD) First commit
* 5be2ea2 Done
* e437b68 (origin/new_branch) Task done
* 1d49cee Add files via upload

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git diff master..master

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git diff master..GitWork
diff --git a/hello.xml b/hello.xml
index 16e98cd..b6fc4c6 100644
--- a/hello.xml
+++ b/hello.xml
@@ -1 +1 @@
-Hello this is master branch
\ No newline at end of file
+hello
\ No newline at end of file

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git merge GitWork
Auto-merging hello.xml
CONFLICT (add/add): Merge conflict in hello.xml
Automatic merge failed; fix conflicts and then commit the result.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git merge GitWork
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git diff master..GitWork
diff --git a/hello.xml b/hello.xml
index 16e98cd..b6fc4c6 100644
--- a/hello.xml
+++ b/hello.xml
@@ -1 +1 @@
-Hello this is master branch
\ No newline at end of file
+hello
\ No newline at end of file

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git diff FETCH_HEAD..GitWork
fatal: ambiguous argument 'FETCH_HEAD..GitWork': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git merge GitWork
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git log --oneline --graph --decorate  --all
* 255a99e (HEAD -> master) Commit the changes in the master
| * 0e4f03d (GitWork) Commit the changes
|/
* 0b6b3d6 (origin/master, origin/HEAD) First commit
* 5be2ea2 Done
* e437b68 (origin/new_branch) Task done
* 1d49cee Add files via upload

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git diff master..master

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git diff master..GitWork
diff --git a/hello.xml b/hello.xml
index 16e98cd..b6fc4c6 100644
--- a/hello.xml
+++ b/hello.xml
@@ -1 +1 @@
-Hello this is master branch
\ No newline at end of file
+hello
\ No newline at end of file

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git merge GitWork
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git merge GitWork
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both added:      hello.xml

no changes added to commit (use "git add" and/or "git commit -a")

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git merge --abort

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git merge GitWork
Auto-merging hello.xml
CONFLICT (add/add): Merge conflict in hello.xml
Automatic merge failed; fix conflicts and then commit the result.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both added:      hello.xml

no changes added to commit (use "git add" and/or "git commit -a")

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ cat hello.xml
<<<<<<< HEAD
Hello this is master branch
=======
hello
>>>>>>> GitWork

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git add .

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master|MERGING)
$ git commit -m 'merged and resolved the conflict in hello.txt'
[master b0327f8] merged and resolved the conflict in hello.txt

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$ git merge GitWork
Already up to date.

Pratibha Sheoran@LAPTOP-L5GF1LUK MINGW64 /d/Gitlearn/git4/GitDemo (master)
$
