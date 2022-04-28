<font face="微软雅黑" size=1 color=black>

[toc]

## 1.1 java代码的结构
### 1.1.1 public类的数量
java程序是由类组成的，类使用{}包括起来，函数使用{}包括起来。
一个源文件（.java）中最多只能有一个public类（主类），文件名称必须与public类的名称相同。其他类的数量不限定，编译完成后每个类都会生成对应的字节码文件。

### 1.1.2 java程序的入口
字节码程序的入口是public main方法，每个类都能有public main方法。

```java
public class hello {
    public static void main(String[] args){ //hello的main函数
        System.out.print("hello world");
    }
}

class dog{
    public static void main(String[] args){  //dog的main函数
        System.out.println("dog"); 
    }
}
```

## 1.2 java开发规范
java区分大小写。使用javac编译时，源文件.java的编码方式必须和javac相同。运行class字节码文件时，无需带.class后缀。
1. 运算符和等号的两边要加上空格。
2. 源码文件.java使用utf-8编码。
3. 每行字符的数量不要超过80个。
4. 代码编程风格有：次行风格、行尾风格（推荐）。
5. 类和方法的注释使用文档注释，即javadoc的方式。非javadoc的注释是给代码的维护者参考的。

## 2.1 java转义字符的使用
\t 制表，固定宽度输出，可以实现对齐；\n 换行，换行之后光标到下一行行首；\r 回车 回车与换行不同，回车之后光标会回到行首。
输出\（反斜杠）、"（双引号）、'（单引号）都需要使用\进行转义。

```java
public class ChangeChar{
    public static void main(String[] args){
        System.out.println("北京\t天津\t上海");
        System.out.println("java学习\r需要努力"); //回车的转义可能导致覆盖，因为回车后光标会到行首
        System.out.print("书名\t作者\t价格\t销量\n三国\t罗贯中\t120\t1000");
    }
}
```

## 2.2 相对路径与绝对路径
相对路径是从当前目录开始定位，形成的路径。绝对路径是从根目录开始定位形成的路径。
```shell
d---abc---test100
       ---test200
 ---abd---test100
       ---test200
```
从abc\test100到abd\test200相对路径为：..\..\abd\test200。绝对路径为：d:\abd\test200。
