# 020-OC对象的分类04-object_getClass内部实现


##### 1.Class objc_getClass(const char *aClassName)
> 1 传入字符串类名
> 2 返回对应的类对象

##### 2.Class object_getClass(id obj)
> 传入的obj可能是instance对象、class对象、meta-class对象
> 返回值
> 如果是instance对象，则返回class对象
> 如果是class对象，则返回meta-class对象
> 如果是meta-class对象，则返回NSObject的meta-class对象
 
##### 3.- (Class)class、+(Class)class
 > 返回的是类对象     

![](http://oriq21dog.bkt.clouddn.com/20180829195815.png)

