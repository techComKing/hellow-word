## hello-word
　　
 ### git基本命令 
 * git init //把这个目录变成Git可以管理的仓库
 * git add README.md //文件添加到仓库
 * git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
 * git commit -m "first commit" //把文件提交到仓库
 * git remote add origin git@github.com:wangjiax9/practice.git //关联远程仓库
 * git push -u origin master //把本地库的所有内容推送到远程库上
 
 
 
 - 如果新建远程仓库不是空的，例如你勾选了 Initialize this repository with a README。那么你通过命令 $ git push -u origin master是会报错的
 ----------------------------------------------------------------
 $ git push -u origin master
To https://github.com/techComKing/sparkLearning.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/techComKing/sparkLearning.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
-------------------------------------------------------------
 这是由于你新创建的那个仓库里面的README文件不在本地仓库目录中，这时我们可以通过以下命令先将内容合并以下：
 　　$ git pull --rebase origin master

　　再输入$ git push origin master。

　　等远程仓库里面有了内容之后，下次再从本地库上传内容的时候只需下面这样就可以了：

　　$ git push origin master。
