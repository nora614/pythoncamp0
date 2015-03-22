# how to use(push)

> Github优越于很多其他同类的一个特点就是我们不用所有的工作都在线操作，有些工作可以在本地操作之后从本地push到github中。

## 设置你的ssh key
### 为什么要设置ssh key？
我们都知道一把钥匙配一把锁（嗯特殊情况就不讨论了哈），ssh key就好像是为你本地和github端的版本库所搭建的特殊通道，只有从这条通道上传的文件github才安心，嗯，这是这个库的主人上传的，才好统一管理。

### 怎么设置ssh key
通用的方法是手动设置。但是也有特殊情况，有些人电脑装有客户端，这个可能就自动配置好了。

1. 这一步用于检查是否已经存在相应文件。如果列出了相应文件，可以跳过第二步。
   
   `$ ls -al ~/.ssh`

   

2. 这一步用于生成ssh key。

   `$ ssh-keygen -t rsa -C "youremail@example.com"`
   
   
3. 这一步用于将你的key添加到ssh－agent
 `eval "$(ssh-agent -s)"`

   `ssh-add ~/.ssh/id_rsa`
4. 首先使用这一条指令，把ssh key拷贝到自己的剪贴板：
   `pbcopy < ~/.ssh/id_rsa.pub `
   
   然后在github进入自己的账户，点击设置（小齿轮）－ssh keys－add ssh key，然后取一个title，把刚才剪贴的东西粘贴到下面的框子中，确认吧！ 

### 特殊情况
我在使用push功能的时候遇到了一个特殊情况。或许是因为我在本地装有github客户端的原因，所以一开始我自己没有手动设置自己的ssh keys，它就自己存在了，并且第一天push是成功的。可是第二天我要push的时候，它一直提醒我到gitbook的request denied, google之后发现都是说自己的ssh key出现了问题，所以又手动设置了一次。

### 参考教程

[Generating SSH keys](https://help.github.com/articles/generating-ssh-keys/)

[建立远程库－廖雪峰](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374385852170d9c7adf13c30429b9660d0eb689dd43a000)

*相比之下我更喜欢第一个，每一步都可以在终端操作，比第二份清楚直接*

## 关联本地仓库和远程库
1. 首先你需要在本地和在远程有相互对应的仓库。一种方法就是可以在线建立好仓库后，把它克隆到本地来。

   克隆有两种方法，如果你有客户端，直接在客户端克隆就好。如果没有，使用以下指令：

    `$ git clone git@github.com:your-name/your-repo.git`

   your-name和your-reop用自己的名字和库的名字替换好。
   
2. **在你的本地库内**（使用`cd`进入），使用如下命令，关联本地和远程：
   `git remote add origin git@github.com:your-name/your-repo.git`


## 如何从本地push

首先使用到如下指令，将你做的变动提交到本地的库：

`git add`

`git commit -m`

接下来使用：

`git push -u origin master`

第一次推的时候，使用`-u`将本地的所有内容都推上去，之后这个就可以省略了。

如果推不了，请尝试`git push -f -u origin master`进行强制推送，嗯是的，我们就是这么暴力～

### 如何从本地同时推到gitbook和github

[该教程详细说明了如何设置](https://github.com/OpenMindClub/OMOOC.py/wiki/gitbook_double_push)

