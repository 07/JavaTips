# Java Tips

[TOC]

## Java

### 1、什么情况下需要序列化？
- 当我们想把的内存中的对象状态保存到一个文件中或者数据库中时候；

- 当我们想用套接字在网络上传送对象的时候；

- 当我们想通过RMI传输对象的时候；

  Java 提供了一种对象序列化的机制，该机制中，一个对象可以被表示为一个字节序列，该字节序列包括该对象的数据、有关对象的类型的信息和存储在对象中数据的类型。将序列化对象写入文件之后，可以从文件中读取出来，并且对它进行反序列化 。





## MySQL

### 1、如果数据库的访问压力过大该如何优化？
- 数据库自身优化策略：建立索引，索引的思想是用空间换时间, 缺点如果数据量太大，过多索引占用大量磁盘空间，所以一般只对关键字段，经常需要检索的字段设置索引。
- 如果任务量过大，需要考虑分库分表，如果一天100万延迟任务，一月就3000万，一年就4亿2千万数据，对于MySQL，单表超过2万千，就算做了索引查询也非常慢，所以后续需要规划分库分表。



### 2、MySQL BLOB类型介绍
​	MySQL中，BLOB是一个二进制大型对象，是一个可以存储大量数据的容器，它能容纳不同大小的数据。BLOB类型实际是个类型系列（TinyBlob、Blob、MediumBlob、LongBlob），除了在存储的最大信息量上不同外，他们是等同的。MySQL的四种BLOB类型:

| 类型       | 大小(单位：字节) |
| ---------- | ---------------- |
| TinyBlob   | 最大  255        |
| Blob       | 最大  65K        |
| MediumBlob | 最大  16M        |
| LongBlob   | 最大  4G         |



### 3、MySQL 设置时区

​	set persist time_zone='+8:00';  然后重新登录MySQL。









## Spring

### 1、StringRedisTemplate和RedisTemplate有什么区别？

- StringRedisTemplate继承RedisTemplate
- 两者的数据是不共通的；也就是说StringRedisTemplate只能管理StringRedisTemplate里面的数据，RedisTemplate只能管理RedisTemplate中的数据。
- StringRedisTemplate默认采用的是String的序列化策略，保存的key和value都是采用此策略序列化保存的，
  RedisTemplate默认采用的是JDK的序列化策略，保存的key和value都是采用此策略序列化保存的。当你的redis数据库里面本来存的是字符串数据或者你要存取的数据就是字符串类型数据的时候，那么你就使用StringRedisTemplate即可，但是如果你的数据是复杂的对象类型，而取出的时候又不想做任何的数据转换，直接从Redis里面取出一个对象，那么使用RedisTemplate是更好的选择。

### 2、Spring中用到的设计模式

| 名称         | 举例                  |
| ------------ | --------------------- |
| 工厂模式     | BeanFactory           |
| 单例模式     | ApplicationContext    |
| 装饰器模式   | BeanWrapper           |
| 代理模式     | AopProxy              |
| 委派模式     | DispatcherServlet     |
| 策略模式     | HandleMapping         |
| 适配器模式   | HandlerApdapter       |
| 模板方法模式 | JdbcTemplate          |
| 观察者模式   | ContextLoaderListener |

​	







## IntelliJ Idea

### 1、设置行号

 - 第一步在我们的电脑上打开idea,可以看到代码的行号没有显示,
 - 第二步下面来显示代码行号,点击File->Settings,
 - 第三步进去Settings界面之后,依次点击Editor->General->Appearance，
 - 第四步在Appearance的右侧找到“Show line numbers”,进行勾选，
 - 第五步可以看到代码的行号已经显示出来了。









