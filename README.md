# githubStart
利用git远程添加项目库

## 设置本地Git仓库与远程Github仓库连接 
- 创建 SSH Key(邮件替换成自己的)
```
$ ssh-keygen -t rsa -C "youremail@example.com"
```
一路回车，使用默认值即可。.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥。

- 登陆GitHub，打开“Settings”->“SSH and GPG Keys”，“New SSH Key”操作。

Title任意，在Key文本框里复制id_rsa.pub文件内容。

- 点“Add SSH Key”，你就应该看到已经添加的Key

为什么GitHub需要SSH Key呢？因为GitHub需要识别出你推送的提交确实是你推送的，而不是别人冒充的，而Git支持SSH协议，所以，GitHub只要知道了你的公钥，就可以确认只有你自己才能推送。

## 文件（夹）上传
- 创建Git本地仓库 
```
git init
```
- 将项目文件添加到仓库
```
git add dir/filename
```
- 文件提交
```
git commit -m '注释'
```
- 将本地创库关联到github上 (地址换成自己的)
```
git remote add origin https://github.com/flyer0126/githubStart
```
- 上传之前，先pull一下 (自己的分支，默认为master)
```
git pull origin master
```
- 上传代码到github远程仓库
```
git push -u origin master
```
提示输入Github Username和Password，然后可以正常上传了。 
