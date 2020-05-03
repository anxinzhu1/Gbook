> 日常手册/指北 分享

    [FAQ] 用git命令行在本地新建目录push至远程gitlab的说明

## 综述
> 初识git基本命令行

## 背景
> 课程预习任务ch0：在本地新增playground下用户名目录，并push到网页端


## 问题
> 终端关闭后之前写的代码是不是就不见了。。


## 操作

**注意：必须参考[预习资料附录](https://learnpythonthehardway.org/python3/appendixa.html))练习命令行
**

> 用git init指向所需操作的目录（文件夹）playgroud,用pwd验证所在文件夹是否正确

> 用mkdir在这个目录里新增自己的用户名目录

> 用cd将位置转移至新增的用户名目录，并用pwd验证

> 用git status验证状态
```
airdeMacBook-Pro:playground air$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```
> 在新增的用户名目录里放上新文件（空目录gitlab会默认没有更新）后添加更新
```
airdeMacBook-Pro:playground air$ git add anxinzhu
airdeMacBook-Pro:playground air$ git add .
```
> 此时再用git status验证
```
airdeMacBook-Pro:playground air$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   anxinzhu/study note.md
```
如上新文件已显示
> 取一个commit标题
```
airdeMacBook-Pro:playground air$ git commit -m "First study note"
[master 9352f3e] First study note
 1 file changed, 6 insertions(+)
 create mode 100644 anxinzhu/study note.md
```
> git push
```
airdeMacBook-Pro:playground air$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 309 bytes | 309.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To gitlab.com:101camp/7py/playground.git
   789fa2c..9352f3e  master -> master
```

# 总结
> 必须先练习git基本命令行
如果有操作错误，有必要时需要删除本地目录，从头开始clone后继续

## refer
> [wikis参考资料](https://gitlab.com/101camp/7py/tasks/-/wikis/How2/How2UseGit)