# 014-OC对象的本质14-libmalloc源码

* 结构体内存大小对齐
* calloc内存对齐

##### 创建一个实例对象，至少需要多少内存？

```
#import <objc/runtime.h>
class_getInstanceSize([NSObject class])
```
##### 创建一个实例对象，实际分配了多少内存？
```
#import <malloc/malloc.h>
malloc_size((__bridge const void *)obj);
```



![](http://oriq21dog.bkt.clouddn.com/20180826214903.png)

