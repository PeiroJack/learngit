# 学习尚硅谷的git教程做的笔记

[学习网址]( https://www.bilibili.com/video/av24441039?p=43 )

学习到P43 在Eclipse中Git插件

预计看完java，开始找项目练手的时候用到



# github上找开源项目

 [git搜索]( https://help.github.com/en/github/searching-for-information-on-github/searching-for-repositories )

in:name example 名字中有“example”
in:readme example readme中有“example”
in:description example 描述中有“example”

stars:>1000 star>1000
forks:>1000 fork>1000
pushed:>2019-09-01 2019年9月1日后有更新的

language:java 用Java编写的项目 



# Linus指令

``` 
ll 查看目录资源
ls -lA 查看包括隐藏的资源
ls -l|less 分层的查看资源(按q退出)
mkdir 新建目录
pwd 查看当前所处的目录
cat [file] (猫眼)连接文件并打印到标准输出设备上
~ 用户夹目录
vim [file name] 新建/修改一个文件
rm [file name] 删除文件
```

# vim指令

```
set nu 显示行数
:wq 保存退出
```



# git指令

```
git init 初始化一个git仓库

设置签名 项目级别/仓库级别
git config user.name 用户名  
git config user.email 用户邮箱
信息保存位置： ./.git/config 文件
设置签名 系统用户级别
git config --global user.name 用户名
git config --global user.email 用户邮箱

git status 状态查看操作 查看工作区、暂存区状态
git add [file name] 添加操作 将工作区的“新建/修改”添加到暂存区
git rm --cached [file name] 删除暂存区中的文件修改
git commit [file name] commit文件进入vim
git commit -m "commit message" [file name] 提交操作 将暂存区的内容提交到本地库

git log 显示日志（空格向下翻页，b向上翻页，q退出）
git log --pretty=oneline 单行显示日志
git log --oneline 单行显示日志 哈希值只显示一部分
git reflog 显示日志 可查看指针信息

git reset --hard [局部索引值]
git reset --hard 回退到最近那个版本
git reset --hard HEAD^ 往后退版本
git reset --hard HEAD~n 往后退n步版本
--soft 仅仅在本地库移动HEAD指针
--mixed 在本地库移动HEAD指针 重置暂存区
--hard 在本地库移动HEAD指针 重置暂存区 重置工作区

git diff [file name] 将工作区中的文件和暂存区进行比较
git diff [本地库中历史版本] [file name] 将工作区中的文件和本地库历史记录进行比较
git diff 将工作区中所有的文件和暂存区进行比较

git branch [分支名] 创建分支
git branch -v 查看分支
git checkout [分知名]

合并分支
git checkout [被合并分支名]
git merge [有新内容的分支名]

解决冲突
git add [文件名]
git commit -m "日志信息" 此时commit一定不能带具体文件名

git remove -v 查看当前所有远程地址别名
git remote add [别名][远程地址]
git remote add origin https://github.com/PeiroJack/learngit.git
git push [别名][分支名]
git push origin master
git clone [远程地址]

pull=fetch+merge
git fetch [远程库地址别名][远程分支名]
git checkout 'origin/master' 跳转到远程库分支
git checkout master 返回master分支

git merge [远程库地址别名/远程分支名]
git pull [远程库地址别名] [远程分支名]

SSH登录
进入当前用户的根目录
cd ~

删除.ssh 目录
rm -rvf .ssh

运行命令生成.ssh 密钥目录
ssh-keygen -t rsa -C [用户邮箱]
ssh-keygen -t rsa -C 3532926353@qq.com

进入.ssh目录查看文件列表
cd .ssh
Is -lF

查看id_rsa.pub文件内容
cat id_rsa.pub
```

