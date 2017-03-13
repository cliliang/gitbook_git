`git status -s`可以以简短的方式查看文件状态

```
$ git status -s
 M README
MM Rakefile
A  lib/git.rb
M  lib/simplegit.rb
?? LICENSE.txt
```
**新添加的未跟踪**文件前面有 ?? 标记，**新添加到暂存区**中的文件前面有 A 标记，修改过的文件前面有 M 标记。你可能注意到了 M 有两个可以出现的位置，出现在靠左边的 M 表示该文件被修改了并放入了暂存区，出现在右边的 M 表示该文件被修改了但是还没放入暂存区。