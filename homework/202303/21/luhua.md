### classpath作用
用来支持JVM如何搜索class
#### 通过系统环境变量设置（不推荐）
#### 在JVM启动时设置
`java -classpath .;C:\work\project\bin abc.Hello  <br>
java -cp.;C:\work\project\bin abc.Hello
`

<br>
不要把任何Java核心库添加到classpath中，JVM根本不依赖classpath加载核心库

### Jar包
把目录打一个包，变成一个文件，JVM会自动去jar文件里搜索
