# Gitbook使用心得

## gitbook是什么
> gitbook是git同系列的又一个产品吗？

Too naive! git是什么你知道吗？

> 该词源自英国俚语，意思大约是“混账”。

不闹了。**Git**是一个分散式版本控制软件，可以让程序员们共同开发一个软件，但是不需要在同一个网络下工作。

> 版本控制，就是以版本来管理自己开发的软件。这样做可以用版本来追踪和维护代码，也可以随时返回到上一个代码。我记得自己在codeskulpter上做作业的时候，经常保存一次就把这一次的作业加入收藏夹，想来也算版本控制了呢，高级版的作业做不出来我就交比它前一个版本的作业。。。

**Github**,是一个共享虚拟主机服务*(web-based hosting service for software development projects using Git)*，用于存放使用Git版本控制的软件代码和内容项目。

> 所以说，github算是git的一个衍生

**Gitbook**可以在线形成一本书。但是估计是新产品，太新了，在wiki上甚至我都没有找到它的页面，所以很多不好用的地方，比如上传的速度很慢，自动和github链接的功能还没有好。

**Gitlab**是当年（也就是去年）我记错了github的名字误打误撞知道的，基本上是github的山寨版。

> 它可使用 Github/Git 和 Markdown 来制作精美的电子书，也就是说你不使用这些也是可以的。可以就像写博客一样在gitbook上写作。的确我并没有在它身上看到版本控制，远程协作也看不到，github关联与否也是个人的事儿。所以，不是同一系列的。

## 如何使用gitbook
### 形成目录
先到自己的版本库里面编辑summary文件，方法如图：
![](/Users/nora/Documents/pythoncamp0/pic/summary.png)
先把目录编好，即使不能写好全部也可以对自己现在正在写的部分进行规划。
### 实现双推
gitbook可以在线编辑，也可以本地推送。我们一般采取后者，并且是github和gitbook双推。

我是如何实现双推的，以及在其中遇到了什么问题：
[link](file:///Users/nora/Documents/pythoncamp0/source/part2/howtopush.md)
###
## 教程推荐
[官方help](http://help.gitbook.com)

[另外一份教程](http://www.chengweiyang.cn/gitbook/gitbook.com/newbook.html)

我最推荐第一份，官方的这一份已经很详细了，但因为是全英文的，所以有阅读困难的可以先参考第二份，上手了再来看第一份。