## 架构师学习路线（Java）

### 编程基础

##### 常用数据结构
数组、链表、堆、栈、队列、Hash表、二叉树等

##### 算法思想
算法时间复杂度和空间复杂度的分析计算

算法思想：递推、递归、穷举、贪心、分治、动态规划、迭代、分支界限

#### 经典算法
经典排序：插入排序、冒泡排序、快排（分划交换排序）、直接选择排序、堆排序、合并排序

经典查找：顺序查找、二分查找、二叉排序树查找

#### 高级数据结构
B+/B-数、红黑树、图等

#### 高级算法
图的深度优先搜索、图的广度优先搜索、拓扑排序、Dijkstra算法（单源最短路径）、霍夫曼编码、辗转相除法、最小生成树等


### Java语言基础
---
#### 基础语法
Java语法格式，常量和变量，变量的作用域，方法和方法的重载，运算符，程序流程控制，各种基本数据类型及包装类

#### 集合类（重要）
Collection以及各种List、Set、Queue、Map的实现以及集成关系，实现原理

Collections和Arrays

#### 其他Java API
String和StringBuffer，System和Runtime类，Date和DateFomat类

java.lang包

java.util包（集合类体系、规则表达式、zip，以及时间、随机数、属性、资源和Timer等）

java.math包

java.net包

java.text包（各种格式化类等）

java.security包

#### 面向对象、面向接口
对象的三大特性：封装、继承和多态，优缺点

如何设计类，类的设计原则

this关键字，final关键字，static关键字

对象的实例化过程

方法的重写和重载；方法和方法的参数传递过程

构造函数

内部类，抽象类，接口

对象的多态性（子类和父类之间的转换、父类纸箱子类的引用），抽象类和接口在多态中的应用

#### Java内存模型、垃圾回收

#### 关于异常
Throwable/Error/Exception，Checked Exception vs. Unchecked Exception，异常的捕捉和抛出，异常捕捉的原则，finally的使用

#### 多线程
线程和进程的概念

如何在程序中创建多线程，线程安全问题，线程之间的通讯

线程的同步

死锁问题的剖析

线程池

#### IO
java.io包，理解IO体系的基于管道模型的设计思路以及常用IO类的特性和使用场合。

File及相关类，字节流InputStream和OutputStream，字符流Reader和Writer，以及相应缓冲流和管道流，字节和字符的转化流，包装流，以及常用包装类使用

分析IO性能

#### XML
熟悉SAX、DOM以及JDOM的优缺点并且能够使用其中的一种完成XML的解析及内容处理；这几种解析方法的原理

#### 一些高级特性

反射、代理、泛型、枚举、Java正则表达式

#### 网络编程
网络通信协议原理及适用场景，Socket编程，WEB服务器的工作原理

#### 其他
JDK1.5、JDK1.6、JDK1.7、JDK1.8每个版本都比前面一个版本添加了哪些新特性，进行了哪些提升

## 数据库相关

#### 理论基础

数据库设计原则和范式

事务（ACID、工作原理、事务的隔离级别、锁、事务的传播机制）

#### 各种数据库优缺点、使用场景分析

MySQL/SQLServer/Oracle以及各种NoSQL(Redis、MongoDB、Memcached、HBase、CouchDB等)

#### SQL语句

数据库创建，权限分配，表的创建，增删改查，连接，子查询

触发器、存储过程、事务控制

#### 优化

索引原理及适用，大表查询优化，多表连接查询优化，子查询优化等

#### 分库、分表、备份、迁移

导入、导出，分库、分表，冷备热备，主从备份、双机热备、纵向扩展、横向扩展

#### JDBC

JDBC Connection、Statement、PreparedStatement、CallableStatement、ResultSet等不同类的使用

连接池（配置使用、实现原理）

ORM，DAO

### JavaWeb核心技术（包括部分前端）

Html5/Css/JS原生/jQuery

Ajax（跨域等）

JSP/JavaBean/Servlet/EL/JSTL/TabLib

JSF

JSON

EJB

序列化和反序列化

规则引擎

搜索引擎

模板引擎

缓存

身份认证

测试

集群

持久化

生成静态页技术

高性能

安全

事务JTA

其他需要了解的，如：管理JMX、安全JCCA/JAAS、集成JCA、通信JNDI/JMS/JavaMain/JAF、SSI技术

### 主流框架及工具

Struts1/Struts2

Spring（IoC、AOP等），SpringMVC

持久化：Hibernate/MyBatis

日志：Log4j

单元测试：JUnit

消息队列：ActiveMQ、RabbitMQ等

负载均衡：Nginx/HaProxy

Web服务器：Tomcat、JBoss、Jetty、Resin、WebLogic、WebSphere等

通信：WebService(cxf的soap、restful协议)

缓存：Redis、Memcached

工作流：Activity、JBPM

搜索引擎：lucene，基于lucene封装的solr

模板引擎：Velocity、FreeMaker

大数据：Hadoop（HDFS和MapReduce）

构建工具：Ant/Maven

### JavaWeb系统设计与架构

Java设计模式

JAVA与UML建模

面向服务架构：SOA/SCA/ESB/OSGI/EAI，微服务

面向资源架构：ROA/REST

面向云架构：COA/Saas/云计算

大型网站负载均衡、系统调优等

### More

#### 排错能力

应该可以根据异常信息比较快速的定位问题的原因和大致位置

#### 优化能力

#### 代码规范、代码管理

有自己的代码规范体系，代码可读性好

#### 知识面广

懂各种网络产品及特性，懂各种中间件，能够知道坑在哪儿，深谙各种技术方案的优缺点，懂整合各种资源并达到最优....了解各种技术及应用场景，有足够的工作经验解决集成中遇到的各种奇葩问题

#### 技术管理/技术总监：

产品管理、项目管理、团队建设、团队提升

#### CTO

发展战略
