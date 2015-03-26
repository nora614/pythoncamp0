# WEEK 2 Guess the number!

## 第一次尝试：

3.25号晚上，因为自己周三开始看视频，很赶，所以有些地方囫囵吞枣了，晚上打算先简化一下过程（去掉input），看看能不能先让游戏跑起来。结果没有。引用一下很短的错误代码：

主要的报错信息为：你的变量既是local的也是global 的

## 第二次尝试
3.26早晨，九点四十第一次成功的完成了自己的guess number
非常简单的一个作品，没有计次，感觉界面也可以再友好一些。

[最简单的作品](https://github.com/nora614/omooc.py/blob/master/src/iippy-1.py)

### 过程
今天早晨还是使用了教授的给的template，并且认为我的program不能操作成功的原因是因为昨晚的问题（变量没有搞懂）。

早晨在组里@糖糖糖的帮助下，理解了：

1. 全局变量如果要在一个函数中使用必须在这个函数里定义一下，比如我在函数外面声明一个global a，函数里面使用a，这两个a是不一样的，函数里也要说明是global a才行。

2. 犯了这么一个错误：
> def input_guess(guess,the_number):
    global guess, the_number
    guess = int(g)
    if guess > the_number:
        print "You can guess lower~"
    elif guess < the_number:
        print "You can guess higher~"
    else:
        print "Congrats!That's correct!"
    return( )
    
 因为我觉得我的函数里面有两个要用到的值，所以就用了这个.但实际上，thenumber已经在前面定义过了，guess的值是g决定的，所以真正的变量就一个g
 
 ## 第三次尝试
 3.26上午十点半。
 我觉得这个游戏的目标是，让玩家感觉到坐在他对面的是一个人和他一起玩。
 
 ### 成果：
 [codeskulpter](http://www.codeskulptor.org/#user39_PFbfEy0tF7_0.py)
 
 [github](https://github.com/nora614/omooc.py/blob/master/src/iippy-2.py)
 
 - 增加了告诉使用者你猜的是什么数字的提示信息
 - 增加了假如使用者猜测超出了range的提示信息
 
 ### 下一次操作的目标：
 假如使用者猜测range100超过了7次，或者range1000超过了10次，提醒一下正确方法。
 可能要用到循环和计数了吧。。。嗯先去吃饭