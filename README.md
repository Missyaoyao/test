

总结：其实只需要进行下面几步就能把本地项目上传到Github

     1、在本地创建一个版本库（即文件夹），通过git init把它变成Git仓库；

     2、把项目复制到这个文件夹里面，再通过git add .把项目添加到仓库；

     3、再通过git commit -m "注释内容"把项目提交到仓库；

     4、在Github上设置好SSH密钥后，新建一个远程仓库，通过https://github.com/Missyaoyao/test.git将本地仓库和远程仓库进行关联；

     5、最后通过git push -u origin master把本地仓库的项目推送到远程仓库（也就是Github）上；（若新建远程仓库的时候自动创建了README文件会报错，解决办法看上面）。


二、遇到问题与解决方案注意：初次使用的话，在输入上面指令过程中会遇到以下几个问题：（这部分引用悠悠大神的，致谢，传送门：https://www.cnblogs.com/yoyoketang/p/7302515.html）

1.要是cmd窗口看到提示以下这两个信息

$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

解决办法：按上面的提升，cmd窗口接着输入

>git config --global user.name "这里是你的github用户名"   

>git config --global user.email xxx@xxx.com(你的邮箱)

2.提交到远程时候，提示：

fatal: remote origin already exists.

解决办法：删除远程git仓库

>git remote rm origin

3.首次操作过程中需要登录就按提示输入账号名和密码