[廖雪峰git教程]( https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496 )

# Git

git用c语言开发的

 SVN 是集中式版本库控制系统 

 Git 是分布式版本控制系统 



 初始化一个Git仓库，使用`git init`命令。 

添加文件到Git仓库，分两步：

1. 使用命令`git add `，注意，可反复多次使用，添加多个文件；
2. 使用命令`git commit -m `，完成。



[git commit之后进入vim（vi）界面，如何退出。](https://blog.csdn.net/zimosangtian/article/details/80848526 ) 

今天用git commit -m “注释”提交的时候，注释写错了，于是各种查资料开始了和git bash vim的纠缠。。。（网上的资料我真是没操作成功，不过最后还是摸索出来了。

首先 使用 git commit --amend 命令（修改最近一次提交的注释信息），会进入到vim 编辑器

然后 你会发现编辑器里你怎么输入都没反应，这是因为vim处在不可编辑状态，

按下字母键 c（此时进入编辑状态），可以开始修改注释信息了

修改好后，你会发现怎么都退出不了，然后如下操作：

按下Esc (退出编辑状态)； 接着连按两次大写字母Z，你会惊喜的发现，终于保存好退出来了！



### 小结

- 要随时掌握工作区的状态，使用`git status`命令。
- 如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。

