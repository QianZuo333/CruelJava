## Java如何实现反射
在JVM加载Java类的时候，就将Java类的类元信息（类元信息及变量和方法）保存到内存中，这样在运行期直接读取目标内存种的数据便能获取到相应的信息
类元信息：打包好的数据模板，在运行期可以被识别
但是C++等语言的类模板信息在编译器便被完全擦除

## 字节存储机制
### Little-Endian
字节按内存由低到高排列，数据位增长方向和内存增长方向相同，但是方便机器处理
0x1:1,0x2:10,0x3:100
Intel的80x86系列时唯一坚持使用小端的芯片
### Big-Endian
字节按内存由高到低排列
### 网络字节序
TCP/IP协议中使用的字节序，通常为Big-Endian