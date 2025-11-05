# java入门

1. 运行在JVM虚拟机上

> 只要装了JVM就可以运行java

2. 三高:高可用,高性能,高并发

---

### java特性和优势

![1](..\img\1-1.png)

简单:类C	面向对象:符合人的思维	

可移植:Windows,Linux,Mac都可运行	高性能:有望超C++	

分布式:为分布式而生,对TCP/IP协议兼容好,URL,远程...

**动态性:反射**(框架)

多线程:边打游戏边听音乐

安全性:内存管理	健壮性:异常捕获

---

### 三大版本

![2](..\img\1-2.png)

---

### JDK , JRE , JVM 

> (JDK>JRE>JVM)

![3](..\img\1-3.png)

java,javac编译和运行

javadoc打包成文档		jar打包成应用（java运行时环境）

通过JVM屏蔽底层环境,实现跨平台

---

### java开发环境搭建

![4](..\img\1-4.png)

1. 下载JDK

2. 配置环境变量

   1. "新建"=>JAVA_HOME【JDK路径】

   2. 配置path变量(双击path打开)

      %JAVA_HOME%\bin	和	%JAVA_HOME%\jre\bin

   3. java -version

---

#### JDK目录

bin：放可执行程序，编译和运行（编译器：javac）

include：引用C/C++头文件

jre：java运行时环境

lib：java类库（用不到）

src：Java基础类源代码

---

文件类型	.java

默认格式：

```java
public class Hello{
    public static void main(String[] args){
        System.out.print("Hello,World!");
    }
}
```

执行：

> 编译：javac	【文件名.java】
>
> 运行：java	【文件名】 ==>不要加".class"

---

### IDE(集成开发环境)

eclipse, IDEA