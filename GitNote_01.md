GitNote 1
---
>第一次使用
```cmd
$ git config --global user.name "your name"
```
```cmd
$ git config --global user.email "your email"
```
常用CMD命令
```cmd
dir:显示目录内容
mkdir:make a directory
rmdir:remove a directory
del:delete a item[del *.txt]
cd:come directory (相对or绝对)路径
D:进入D盘
ping [-t] ip
ipconfig (all)
```

选择一个文件夹在其中创建版本库文件夹
```cmd
$ git init
```
添加文件到到暂存区

```cmd
$ git add readme.md
```
![版本库](https://www.liaoxuefeng.com/files/attachments/919020037470528/0)

提交文件到GitHub,把暂存区的所有内容提交到当前分支
>-m参数后面是本次提交的说明
>提交后缓冲区会清空,需要重新add

```cmd
$ git commit -m "file title"
```
检查目录状态
```cmd
$ git status
```

查看上次修改内容
```cmd
$ git diff filename
```
版本日志
```cmd
$ git log 
```
或者更简短的日志记录
```cmd
$ git log --pretty=oneline
```
从当前版本回退到上一个版本
```cmd
$ git reset --hard HEAD^
```
要取消回到哪个版本需要版本号
```cmd
$ git reset --hard VersionID
```
显示版本记录
```cmd
$ git reflog
```
从暂存区或master中恢复到工作区
>让这个文件回到最近一次git commit或git add时的状态
```cmd
$ git checkout -- filename
```
撤销暂存区的修改
```cmd
$ git reset HEAD filename
```
删除版本库中的文件
```cmd
$ git commit -m "remove filename"
```
删除工作区和暂存区的文件
```cmd
$ git rm filename
```
创建ssh密钥
```cmd
$ ssh-keygen -t rsa -C "email@xxx.com"
```
回车即可,不需要设置密码

关联库到GitHub
```cmd
$ echo "# GitNote" >> README.md
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin https://github.com/UserName/PepoName.git
$ git push -u origin main
```
创建远程库
```cmd
$ git remote add origin git@github.com:UserName/Pepo.git
```
列出远程库信息
```cmd
$ git remote -v
```
删除远程库
```cmd
git remote rm originName
```
克隆远程库
>第三个参数可以是https或者SSH,SSH更快
```cmd
git clone git@github.com:UserName/PepoName.git
```


