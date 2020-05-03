## 综述
> 如何通过SHH#将远程仓库clone到本地


# 背景
> 错误或不适合的参考链接[不适合的参考](https://blog.csdn.net/xuezhangjun0121/article/details/80735291)
> 正确参考链接，[官方文档](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
或[微信群助教发的链接](https://docs.gitlab.com/ee/ssh/README.html)


## 问题
> 有个问题是为何要将clone到本地


## 操作
> 1.下载好git后，在终端根据[说明链接](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html)添加用户名及设置邮件并检验

> 2.生成本地SHH密钥，`ssh-keygen -t rsa -b 4096 -C "email@example.com"`，注意此处邮件地址改成自己的

当出现`Enter file in which to save the key (/Users/air/.ssh/id_rsa):`时，~~注意按指示准确输入~~，直接按回车键。

> 3.在gitlab上新增SHH密钥，先复制刚生成的本地SHH密钥，用代码`pbcopy < ~/.ssh/id_rsa.pub`执行复制，就不用找文件夹位置，我找了没找到，不知道是不是应该找不到……

  在头像下方打开settings-SHH keys进入，粘贴密钥，按add即可

> 4.检验是否设置成功，用代码`ssh -T git@gitlab.com`，如果显示`Welcome to GitLab, @your usename!`，就说明ok了~可以去clone了


## 总结试错点
> 生成密钥时让输入文件名，~~没有按括号提示中准确输入，输了很多次随机想出来的文件名，最后才发现有提示……~~

> 由于不习惯用代码来执行操作，感觉代码操作应该更难，所以花了很久找文件名，没想到代码执行起来更便捷

> 关于搜索资料：

先看官方文档（看了官方文档才知道不用输入文件名，直接按回车）

最好用英文关键词在google中搜索，我是用中文搜了一整句话