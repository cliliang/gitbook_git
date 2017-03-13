##已有工程加入远程git服务器
* [如何用git将项目代码上传到github](http://blog.csdn.net/laozitianxia/article/details/50682100)
* 对于已经存在的git工程，想改变远程仓库地址，可以如下：
> 1. 删除已有的.git文件：rm -r -f .git
> 2. git init
> 3. git add .
> 4. git commit -m "commit message"
> 5. git remote add origin git@github.com:cliliang/lib
> 6. git push origin master



