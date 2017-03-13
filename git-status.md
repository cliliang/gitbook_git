##查看状态
`git status -s`可以以简短的方式查看文件状态

```
$ git status -s
 M README
MM Rakefile
A  lib/git.rb
M  lib/simplegit.rb
?? LICENSE.txt
```
**新添加的未跟踪**文件前面有 ?? 标记，**新添加到暂存区**中的文件前面有 A 标记，修改过的文件前面有 M 标记。你可能注意到了 M 有两个可以出现的位置，出现在靠左边的 M 表示该文件**被修改了并放入了暂存区**，出现在右边的 M 表示该文件**被修改了但是还没放入暂存区**。

##提交更新
`git commit -a -m "commit files"`会自动把**所有已经跟踪过的文件**暂存起来一并提交，从而跳过 `git add`。如果文件还未跟踪，用此方法则不能将之提交。

##删除文件
1.对于已经存在于暂存区域的文件，如果只是简单的手动删除文件，这时检查状态时`deleted:    PROJECTS.md`，需要再用`git rm`记录此次删除文件的操作。
2.对于已经存在于暂存区域的文件，需要用`git rm -f RD.txt`,记录此次删除记录并自动在硬盘中删除文件。
3.对于已经存在于暂存区域的文件，如果只是删除对于此文件的跟踪，保留在硬盘上的文件，则需要使用`git rm --cached RD.txt`。

##重命名
重命名文件名，如果直接更改，查看状态后完成此次重命名操作，相当于

```
$ mv README.md README
$ git rm README.md
$ git add README
```
