## 常量池
Java类中绝大多数信息都由常量描述，尤其是Java类中定义的方法和变量，都由常量保存

### 基本结构
由常量池数量和常量池数组两部分组成
常量池数量紧跟在版本号后面，常量池数组紧跟在常量池数量后面

### 常量池分配总体链路
``
onstantPoolOop constant_pool = oopFactory::new_constantPool(length, 
    oopDesc::IsSafeConc,
    CHECK_(nullHandle));
`` <br>
#### oopFactory
oop的工厂类，JVM内部，常量池，字段，符号，方法等一切都被对象包装起来，一起对象
在内存中都通过oop这种指针进行指向。
在JVM内部，所有对象的内存分配，对象创建与初始化工作都通过oopFactory这个入口得以实现
