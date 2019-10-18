# Java面向对象知识点

事件：2019年10月12日14:10:00

作者：胜Hero

##### 第一章：**  环境搭建

###### 第一点.    架构

a)      搭建（model）模型层，创建实体类

b)      搭建（service）控制层，创建服务类

c)      搭建（tool）工具层，创建工具类

###### 第二点.  命名规范

a)      类名首字母应该大写。字段、方法以及对象（句柄）的首字母应小写。对于所有标识符，其中包含的所有单词都应紧靠在一起，而且大写中间单词的首字母。

b)      不能以数字开头，名称只能由字母、数字、下划线、$符号组成，称不能使用JAVA中的关键字，不允许出现中文及拼音

##### **第二章：**  类和对象的创建

###### 第一点.    构造方法

a)      构造方法名称和类名相同，没有返回值类型，构造方法主要的作用是给成员变量初始化赋值

###### 第二点.    构造方法重载

a)      如果同一个类中包含了两个及以上的方法，它们的方法名相同，但参数或参数类型不同则称之为方法从在，成员方法和构造方法都可以重载

###### 第三点.    Static

a)      Static通常用来修饰属性，方法和代码块，被修饰的代码之间存放在内存中，无论是否执行

##### **第三章：**  封装

###### 第一点.    封装概述

a)      封装是指将对象的属性私有化，不允许外部程序直接访问，通过该类提供的方法实现对内部信息的操作

###### 第二点.    封装好处

a)      提高了安全性

b)      提高了复用性

c)      隐藏了实现细节

###### 第三点.    封装使用步骤

a)      将属性私有化

b)      定义get和set方法，在方法内部设置取值范围

c)      拥抱get和set进行调用

###### 第四点.    封转注意事项

a)      类的属性均用（private）私有修饰符

###### 第五点.    封转的访问权限

 

 

| 修饰符            | 同一个类 | 同一个包 | 子类 | 所有类 |
| ----------------- | -------- | -------- | ---- | ------ |
| Private（私有的） | *        |          |      |        |
| Defaule(默认)     | *        | *        |      |        |
| Protected         | *        | *        | *    |        |
| Public（公共的）  | *        | *        | *    | *      |

 

##### **第四章：**  继承

###### 第一点.    继承的使用

a)      子类继承父类所有的属性和方法，只能调用父类的非private属性和方法

b)      Java只支持单继承，但允许多层继承

c)    

```java
  [修饰符] class 类名 extends 父类｛

        属性定义

        方法定义

	｝
```



###### 第二点.    继承中的构造方法

a)      Super关键字

b)      Super和this很像，区别是this是调用本地的对象，方法，属性；super是调用父类的

c)      Super（）：调用父类的有参构造方法，不再调用父类的无参构造方法

d)      无论子类调用是否有参，在继承中只调用父类无参构造方法，如果父类没有无参构造方法则必须调用父类有参构造方法

###### 第三点.    重写

a)      重写称为方法的覆盖，即子类的方法名，返回值，类型参数及个数完全相同，唯一不同的只是方法的实现内容，这种称为重写

###### 第四点.    异常处理

a)      Try{ }catch(    ){     }块

​                          i.          当try中代码执行完不会发生异常时则忽略catch

​                         ii.          当try中代码执行有问题是则用catch捕获

b)      常见异常类型

| 异常                           | 说明                                               |
| ------------------------------ | -------------------------------------------------- |
| Exception                      | 异常层次结构的根类（必须放在最后，因为它范围最大） |
| ArithmeticException            | 算数错误，如以零作为除数                           |
| ArraylndexOutOfBoundsException | 数组下标越界                                       |
| NullPointerException           | 空指针异常                                         |
| ClassNotFoundExceotion         | 不能加载所需类                                     |
| InputMismatchExceotion         | 得到的数据类型与实际类型不符                       |
| ClassCastException             | 对象强制类型转换出现错误                           |
| IllegalArgumentException       | 方法接到非法参数                                   |
| NumberFormatException          | 数字歌手转换异常                                   |

 

##### **第五章：**  多态

###### 第一点.    多态概述

a)      多态是指不同类的对象对同一消息做出不同相应

b)      多态存在的3个必要条件:

​                          i.          要有继承，要有重写，父类引用指向子类对象

c)      多态好处：

​                          i.          可替换性

​                         ii.          可扩充性

​                        iii.          接口性

​                        iv.          简化性

###### 第二点.    多态使用

a)      向上继承

​                          i.          子类向父类的转换称为向上转型

​                         ii.          <父类型><引用变量明>=new<子类型>();

b)      向下继承

​                          i.          将一个指向子类对象的父类引用赋给一个子类的引用，即将父类类型转换为子类类型，称为向下转型

​                         ii.          向下转型必须经过向上转型才能得到父类型的引用变量

​                        iii.          <子类型><引用变量名>=(<子类型>) <父类型的引用变量>

###### 第三点.    Instanceof运算符

a)      在向下转型的过程从可以进行判断是否转型成功

###### 第四点.    Try-catch-finall块

a)      Finall里面的内容无论是否发生异常均被执行

###### 第五点.    多重catch块

a)      可以捕获多个不同类型的异常

##### **第六章：**  抽象

###### 第一点.    抽象类

a)      抽象就是用程序的逻辑方法和数据结构来模拟现实生活中的世界

b)      抽象类就是用来被继承的，没有具体的实例，无法被new出对象

c)      语法：public abstract class 类名｛｝

d)      抽象类中可以写普通方法，但必须至少有一个抽象方法

###### 第二点.    抽象方法

a)      抽象方法没有方法体

b)      语法：public abstract 返回值类型 方法名（参数列表）；

c)      子类必须重写父类的抽象方法

###### 第三点.    注意项

a)      包含抽象方法的一定是抽象类

b)      抽象类中不一定都是抽象方法

c)      构造方法不能被声明为抽象方法

d)      Abstact不能与 public，static，final，native并列修饰同一个方法

###### 第四点.    Final修饰符

a)      Final修饰的类不能被继承

b)      因为不能被继承所以该类中的方法默认都是final修饰

c)      该类如果不需要有子类，不需要重写，不需要被扩展就用final修饰

d)      Final修饰的方法可以被继承不可被重写

e)      Final修饰的对象则该对象的引用不能改变，但值可以改变

f)       Final修饰的属性变为常量，值不可更改

##### **第七章：**  接口

###### 第一点.    什么是接口

a)      接口是一套规范，满足规范的设备就可以组装到一起

###### 第二点.    语法

a)      [修饰符] interface 借口名extends父接口1，父接口2~~｛｝

b)      Class 类名 extends 父类名 implements 接口1,接口2~~ {}

###### 第三点.    注意事项

a)      接口的命名规则与类相同

b)      接口中只能定义常量不能定义变量

c)      接口中所有的方法都是抽象方法

d)      接口不实例化，不能有构造方法

e)      接口的实现类必须实现接口的全部方法

##### **第八章：**  集合框架

###### 第一点.    定义

a)      集合是存储对象最常见的一种方式（容器）

###### 第二点.    内容

a)      Java集合分为两大类Collection和Map

b)      区别：

​                          i.          Collection接口存储一组不唯一（允许重复）、无序的对象

​                         ii.          Set接口继承Collection接口，存储一组唯一（不允许重复）、无序的对象

​                        iii.          List接口继承Collection接口，存储一组不唯一（允许重复）、有序（以元素插入次序）的对象

​                        iv.          Map接口存储一组成对的键-值对象，体统key（键）到value(值)的射影

###### 第三点.    List接口

a)      List接口分为ArrayList与LinkedList

b)      创建方法：

​                          i.          List 名称=new ArrayList();

​                         ii.          LinkedList 名称=new LinkedList();

c)      区别为：

​                          i.          ArrayList是实现了基于动态数组的数据结构，LinkedList基于链表的数据结构

​                         ii.          对于随机访问git和set,ArrayList优于LinkedList，因为LinkedList要移动指针

​                        iii.          对于新增和删除操作add和remove，LinkedLIst占优势，因为ArrayList要移动数据

d)      List常见的方法

| 方法名称                  | 说明                                        |
| ------------------------- | ------------------------------------------- |
| add(object   o)           | 在列表末尾顺序添加元素，起始索引位置从0开始 |
| add(int   index,object o) | 在指定位置添加指定内容                      |
| int   sitze()             | 返回列表中元素个数                          |
| get(int   index)          | 返回指定位置的元素                          |
| contains(object   o)      | 判断列表中是否存在之指定元素                |
| remove(object   o)        | 从列表中删除元素                            |
| remove(int   index)       | 删除指定位置元素                            |

e)      LinkedList集合的特殊方法

| 方法                 | 作用                     |
| -------------------- | ------------------------ |
| addFirst(object   o) | 在列表首部添加元素       |
| addLast(object   o)  | 在列表尾部添加元素       |
| getFirst()           | 返回列表中的第一个元素   |
| getLast()            | 返回列表中的最后一个元素 |
| removeFirst()        | 删除并返回第一个         |
| rermoveLast()        | 删除并返回最后一个       |

 

###### 第四点.    Map集合类

a)      专门用来处理键值关系的数据

b)      Map map=new HastMap();

c)      Map常用方法

| 方法名称                       | 说明                                      |
| ------------------------------ | ----------------------------------------- |
| put(object   key,object value) | 键值对应进行存储   键不可重复，值可以重复 |
| get(object   o)                | 返回键相关联的值,没有返回null             |
| remove(object   o)             | 删除指定键的映射                          |
| size()                         | 返回元素个数                              |
| keyset()                       | 返回键的集合                              |
| values()                       | 返回值的集合                              |
| containsKey(object   o)        | 存在指定的键值则返回true                  |
| isEmpty()                      | 不存在键值关系返回true                    |
| cleat()                        | 从此映射中删除所有映射                    |

 

###### 第五点.    泛型集合

a)      泛型集合是指在创建集合对象时之ID那个集合中的元素，从集合中抽取元素时无需进行转换

b)      例：

​                          i.          Map<String, ArrayList>Commodity=new HashMap<String, ArrayList>();

##### **第九章：**  文件操作

###### 第一点.    什么是流

a)	在java中所读到的信息，是通过一根管道，输送到数据文件中的，这根管道中的信息称之为流（Stream）。而在java程序中打开流这个操作称之为写（write）

###### 第二点.    字节输出流写文件

```java
//指定文件夹
String lj="D:/java\\as.txt";			
/*
 * 字节输出流
 */
FileOutputStream out=new FileOutputStream(lj);
String str="dsfsdfwefw";
//将字符串转换为字节
byte [] words=str.getBytes();
//将数据写到文件中
//(文件名,第几位开始,第几位结束);
out.write(words,0,words.length);
//关闭输出流
out.close();
```



###### 第三点.    字符输出流写文件

```java
//指定文件夹
String lj="D:/java\\as.txt";
/*			
 * 字符串输出流
 */
FileWriter fw=new FileWriter(lj);
//写入内容
fw.write("我热爱java@_@");
//刷新输出流
fw.flush();
//关闭输出流
fw.close();
```



###### 第四点.    字节输入流读文件

```java
//指定文件夹
String lj="D:/java\\as.txt";
//创建对象	
InputStream input=new FileInputStream(lj);
//读取单个字符		
input.read();
//将数据读取到字节数组中
input.read(byte [] b);
//从输入流中读取最多len长度的字符，保存到字符数组b中，保存位置从off开始
input.read(btye [] b,int off,int len);
//返回输入流读取的估计字节数
input.available();
//关闭输入流
input.close();
```



###### 第五点.    字符输入流独文件

```java
//指定文件夹
String lj="D:/java\\as.txt";
//创建对象	
FileReader input=new FileReader(lj);
//读取单个字符		
input.read();
//将数据读取到字节数组中
input.read(byte [] b);
//从输入流中读取最多len长度的字符，保存到字符数组b中，保存位置从off开始
input.read(btye [] b,int off,int len);
//关闭输入流
input.close();
```



##### **第十章：**  多线程

###### 第一点.    线程创建

方式1：

```java
//1.定义一个类实现Runnable接口
public class MyThreadOne implements Runnable{
    //2.实现接口中唯一的run()方法
	public void run() {
		// TODO Auto-generated method stub
		System.out.println("这是启用Runnable接口创建的子线程");
	}
}

```

```java
//3.声明一个线程实体
public class Establish {
	public static void main(String[] args) {
        MyThreadOne myThraedOne=new MyThreadOne();
        //4.通过start()方法启动
        new Thread(myThraedOne).start();
    }
}
```

方式2：

```java
//1.创建MyThread并继承Thread类
public class Mythread extends Thread(){
    //2.实现Thread中的run类
    public void run(){
        System.in.println("这是继承Tread类创建的子线程");
    }
}

```

```java
//3.生成对象
public class Establish {
	public static void main(String[] args) {
        Mythread Mythread=new Mythread();
        //4.通过start()方法启动
        Mythread.start();
    }
}

```

不足之处还请反馈到邮箱：728165564@qq.com,我们会及时处理

