* git --version  版本号

* git config --global user.name "用户名"		设置用户名
* git config --global user.email  xxx@xx.com 	 设置用户邮箱
* git config --list				查看设置列表
* git log 					查看所有日志
* git reflog					查看所有分支的所有操作记录
* git log -行数 --pretty=oneline  		一行一行的输出指定行数的日志

* git diff HEAD -- 文件   			与版本库中的文件对比

* git ls-files					查看本地仓库中的所有文件
---------------------------------------
工作区->暂存区->Git仓库

* 提交:
* git init 			初始化本地仓库
* git add 文件名  		将文件添加到暂存区
* git status 			查看暂存区状态
* git commit -m '提交时的描述'  	提交
* git reset HEAD  		撤销操作(回退到上一步)
* git commit -a 		提交到暂存区并提交(组合命令)

-------------------------------------------------------
### 版本的操作
* git reset --hard HEAD^ 	版本回退到上一个版本
* git reset --hard HEAD^^	回退到上两个版本

* git reset --hard HEAD~1	回退一个版本(~后跟要回退版本数)


* git reset --hard 版本唯一的标识符(前几位不重复)		回到最新的版本



* 文件删除(修改)
* git checkout -- 文件名 	将本地仓库中的文件拉取到工作区(文件误删并且本地仓库中存在)
* git rm 文件名		删除工作区及本地仓库中的文件




### 克隆远程项目到本地
* git clone 项目链接

### 本地文件推送到远程
* git remote add origin 远程仓库链接
* git push -u 绑定的名称 master


### ssh链接git
'''
1.ssh-keygen -t rsa -C "邮箱地址"
生成的公钥私钥路径
Your identification has been saved in /c/Users/32029/.ssh/id_rsa
Your public key has been saved in /c/Users/32029/.ssh/id_rsa.pub

2.在github上设置ssh,填写公钥

3.测试
ssh -T  git@github.com      ->  填写密码 ->成功

4.上传本地仓库
git remote add 别名 ssh地址
git push -u origin main
'''













