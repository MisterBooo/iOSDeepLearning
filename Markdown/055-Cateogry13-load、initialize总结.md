# 055-Cateogry13-load、initialize总结

##### load、initialize方法的区别是什么？  

1.调用方式 
> 1.load是根据函数地址直接调用
> ![](http://oriq21dog.bkt.clouddn.com/20180906112452.png)
> 2.initialize是通过objc_msgSend调用
![](http://oriq21dog.bkt.clouddn.com/20180906112603.png)

2.调用时刻
> 1.load是runtime加载类、分类的时候调用（只会调用1次）
> 2.initialize是类第一次接收到消息的时候调用，每一个类只会initialize一次（父类的initialize方法可能会被调用多次）


##### load、initialize的调用顺序
1.load
> 先调用类的load
> > 先编译的类，优先调用load
> > 调用子类的load之前，会先调用父类的load

> 再调用分类的load
> > 先编译的分类，优先调用load

2.initialize
> 先初始化父类
> 再初始化子类（可能最终调用的是父类的initialize方法）


