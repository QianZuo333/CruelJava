Java文件从被加载到被卸载的整个生命过程
1. 加载
   常量池解析，Java字段和方法的解析
   将Java类的字节码文件加载到机器内存中，并在内存中构建出Java类的原型——类模板对象
   类模板对象，其实就是Java类在JVM内存中的一个快照
2. 链接（验证+准备+解析）
   主要作用：将字节码指令中对常量池的索引引用转换为直接引用
3. 初始化
   并非对类进行初始化，而是指执行类的<clinit>() 方法
   Java类中包含static修饰的静态字段，或者有使用static{}块包裹的代码段是，编译后会在字节码文件中包含一个名为<clint>()的方法，JVM初始化阶段便会调用该方法
4. 使用
   使用new关键字来实例化一个Java类
5. 卸载
   类模板存储在metaSpace区，当内存超出时，JVM的GC便有可能将其回收