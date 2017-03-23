## GitHub 学习记录

### lesson1 一些简单的git命令

- git config --global user.name "mcy2016" //配置用户名

- git init //初始化

- git add readme //提交到仓库

- git commit -m "提交注释" //提交注释

- git status //查看状态

- git log //查看提交日志

### lesson2 

- git remote add wyyd https://github.com/mcy2016/githubStudy.git // 连接到远程仓库（关联远程仓库）

- git push wyyd master //push 到远程仓库

> 每次修改完都需要执行 git add readme.md , git commit -m "注释内容"，git push wyyd master。这三步
> 也可以简化成两步，git commit -a -m "注释内容"， git push wyyd master.这两步

### lesson3 分支

- git branch //列出分支

- gti branch dev //创建分支 

- git checkout dev //切换分支

- git branch -d && gti branch -D //删除要地分支

> 删除本地分支后要使用 git push wyyd :dev  才能删除远程分支。注意：分支名前面的空格不能省略。

### lesson4 远程拉取文件 pull

- git pull wyyd master //把远程的文件拉取到本地，这会直接覆盖本地文件

- git fetch wyyd master //从远程master分支获取更新

- git diff master wyyd/master //比较本地master和远程master(wyyd/master)有什么不同

- git merge wyyd/master //合并

- 当远程和本地仓库文件有冲突时（也就是远程有的我们没有，我们有的远程没有），使用git checkout --ours README.md,意思是以我们本地的文件为最终版本，然后再进行合并操作，git merge wyyd/master,再进行commit 和push操作

### lesson5 SSH(Secure shell)

- ssh-keygen -t rsa -C "1991993249@qq.com" 生成公钥并保存

- 打开生成的公钥文件里的内容，粘贴进gtihub平台的ssh里。

- 重新生成配置文件，git remote, git remote rm wyyd, git remote add wyyd git@github.com:mcy2016/GitHubStudy.git

- git clone -b master https://github.com/mcy2016/GitHubStudy.git


测试更新