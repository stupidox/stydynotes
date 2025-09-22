# stydynotes
修改用户名和邮箱：
git config --global user.name “stupidox”
git config --global user.email “email”

查看全部git配置信息(查看刚刚添加的用户名和邮箱)：
git config --list

保存用户及密码，下次免登录：
git config --global credential.helper store

关联远程仓库： git remote add origin git@github.com:stupidox/xxx.git

问题：
fatal: detected dubious ownership in repository at 'E:/javaWorkspace/crawler'
'E:/javaWorkspace/crawler' is owned by:
解决：
git config --global --add safe.directory "*"

问题：
warning: in the working copy of 'pom.xml', LF will be replaced by CRLF the next
time Git touches it
解决：
git config --global core.autocrlf true

git add .

git commit -am "init"

点击github头像，打开“Settings”–“SSH and GPG Keys”页面，Add SSH Key。验证： ssh -T git@github.com

由于新建的远程仓库是空的，所以要加上-u这个参数
git push -u origin master
之后仓库不是空的，就不用加上-u
git push origin master
