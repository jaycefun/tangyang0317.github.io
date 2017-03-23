## 学习Hibernate

学习Hibernate
一.什么是Hibernate？
     简单的一句话，hibernate是对jdbc进行封装的对象关系映射的持久层框架。



二.Hibernate核心：
        

     从上图可以看出，hibernate主要有六个对象：
          hibernate.cfg.xml  -------->   hibernate的核心配置文件，配置数据源等操作；
          object.hbm.xml   -------->对象与数据库表的映射关系配置文件；
          configuration    -------->通过读取  hibernate.cfg.xml  ，拿到相应的配置信息，负责配置并启动Hibernate。
          SessionFactory  -------->初始化hibernate;
          Session   ---------->负责持久化数据对象的CRUD操作;
          Transaction   -------->负责实物操作;


     注：configuration是一个启动间对象，一旦SessionFactory创建完成他就被丢弃。




三：Hibernate的优缺点：

     优点：符合java面向对象编程的思想，开发更加对象化，一般不需要编写sql语句，直接操作对象即可；
               移植性强，代码大多具有可复用性；
               轻量级的框架，不需要继承，不需要实现接口；
               代码测试方便；
               开发效率高，生产能力强；
    
     缺点：使用数据库特性的语句，很难将调优；
               对大批量数据更新存在问题;
               系统中存在大量攻击查询功能；
               程序员会忘记SQL语法，越来越懒。

