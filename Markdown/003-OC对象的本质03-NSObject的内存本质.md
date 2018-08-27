# 003-OC对象的本质03-NSObject的内存本质

一个OC对象在内存中是如何布局的

```
@interface NSObject  {
    Class isa  ;
}
@end
struct NSObject_IMPL {
	Class isa;
};

```

