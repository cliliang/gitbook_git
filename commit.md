##重新提交
有时候我们提交完了才发现漏掉了几个文件没有添加，或者提交信息写错了。此时，可以运行带有 --amend 选项的提交命令尝试重新提交：
```
$ git commit --amend
```
这个命令会将暂存区中的文件提交。如果自上次提交以来你还未做任何修改（例如，在上次提交后马上执行了此命令），那么快照会保持不变，而你所修改的只是提交信息。例如，你提交后发现忘记了暂存某些需要的修改，可以像下面这样操作：
```
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend
```
最终你只会有一个提交，第二次提交将代替第一次提交的结果。

##取消暂存的文件
想对两个已修改的文件分开提交，但是却使用`git add *`将两个文件都加入了暂存区，这时可以使用`reset`将文件从暂存区移出：
```
$ git add *
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
  renamed:    README.md -> README
  modified:   CONTRIBUTING.md
```
这时使用`$ git reset HEAD README.md` 命令即可将README.md文件从暂存区中移出。

##撤消对文件的修改
文件已经修改，但是并不想保留时，想重新回到未修改时的样子，可以使用以下命令
```
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
  modified:   CONTRIBUTING.md
```
像上面提示的那样`git checkout -- CONTRIBUTING.md`，这样，被修改的文件就能够回到修改前的样子。

>在Git中**任何已提交**的东西几乎总是可以恢复的。甚至那些被删除的分支中的提交或使用 --amend 选项覆盖的提交也可以恢复。然而，任何你未提交的东西丢失后很可能再也找不到了。





