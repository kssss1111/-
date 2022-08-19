---

---

# 一、数据库基础知识

**先谈发音**

MySQL如何发音？在国内MySQL发音有很多种，Oracle官方文档说他们念作

My sequal['si:kwəl]。

![SNAGHTML49673ab](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/SNAGHTML49673ab.PNG)

## I、数据库基本概念

1. **数据**

   数据（Data）是指对客观事物进行描述并可以鉴别的符号，这些符号是可识别的、抽象的。它不仅指狭义上的数字，而是有多种表现形式：字母、文字、文本、图形、音频、视频等。

2. **数据库**

   数据库是数据管理的有效技术，是由一批数据构成的有序集合，这些数据被存放在结构化的数据表里。数据表之间相互关联，反映客观事物间的本质联系。

3. **数据库管理系统**

   数据库管理系统（Database Management System，DBMS）是用来定义和管理数据的软件。

4. **数据库应用程序**

   数据库应用程序（Database Application System，DBAS）是在数据库管理系统基础上，使用数据库管理系统的语法，开发的直接面对最终用户的应用程序。

5. **数据库管理员**

   数据库管理员（Database Administrator，DBA）是指对数据库管理系统进行操作的人员，其主要负责数据库的运营和维护。

## II、数据库分类

![image-20211019152519525](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211019152519525.png)

**关系型数据库**

关系型数据库最典型的**数据结构是表**，由**二维表**及其**之间的联系**所组成的一个数据组 织。可以采用结构化查询语言（SQL）对数据库进行操作。

**优点**：

1. **易于维护**：都是使用表结构，格式一致；
2. **使用方便**：SQL语言通用，可用于复杂查询；
3. **复杂操作**：支持SQL，可用于一个表以及多个表之间非常复杂的查询。

**缺点**：

1. **读写性能比较差**，尤其是海量数据的高效率读写；
2. **固定的表结构**，灵活度稍欠；
3. **高并发读写需求**，传统关系型数据库来说，硬盘I/O是一个很大的瓶颈。

**非关系型数据库**

非关系型数据库也称之为NoSQL数据库，是一种数据结构化存储方法的集合，可以是文档或者键值对等。

优点：

1. **格式灵活**：存储数据的格式可以是key,value形式、文档形式、图片形式等等，文档形式、图片形式等等，使用灵活，应用场景广泛，而关系型数据库则只支持基础类型。
2. **速度快**：nosql可以使用硬盘或者随机存储器作为载体，而关系型数据库只能使用硬盘；
3. **高扩展性**；
4. **成本低**：nosql数据库部署简单，基本都是开源软件。

缺点：

1. **不提供sql支持，学习和使用成本较高**；
2. **无事务处理**；
3. **数据结构相对复杂，复杂查询方面稍欠**。

**实时效果反馈**

**1**.**关系型数据库模型是将复杂的数据结构用来表示**。

A 文件

B 一维结构

C 二维表结构

D 自定义方式

**2**.**数据库管理系统是用来定义和的软件。**

A 管理应用程序

B 管理密码

C 管理数据

D 管理管理员

**答案**

1=>C 2=>C

## III、下载MySQL

MySQL官网地址：mysql.com

![image-20211103164526373](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211103164526373-16359291278515-16359291979098.png)

![image-20211103164628328](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211103164628328-16359291894086-16359291951737.png)

![image-20211103164715051](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211103164715051-16359292363659.png)

![image-20211103164750032](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211103164750032-163592927109210.png)

![image-20211103165040414](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211103165040414-163592944131811.png)

##  IV、MySQL的安装与卸载

### 1、MySQL安装

![image-20211020144034102](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144034102.png)

![image-20211020144231070](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144231070.png)

![image-20211020144328726](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144328726.png)

![image-20211020144418157](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144418157.png)

![image-20211020144449646](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144449646.png)

![image-20211020144800088](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020144800088.png)

![image-20211020145118420](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145118420.png)

![image-20211020145237607](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145237607.png)

![image-20211020145329903](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145329903.png)

![image-20211020145418418](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145418418.png)

![image-20211020145443438](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145443438.png)

![image-20211020145517569](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020145517569.png)

### 2、MySQL卸载

![image-20211020150305207](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020150305207.png)

![image-20211020150433787](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020150433787.png)

![image-20211020161642553](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020161642553.png)

![image-20211020150622994](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020150622994.png)

![image-20211020150842934](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020150842934.png)

![image-20211020152735461](https://www.itbaizhan.com/wiki/imgs/Mysql/image-20211020152735461.png)

 

## V、SQL语言

![image-20211106184859713](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106184859713-16361957632672.png)

### 1、SQL语言简介

结构化查询语言(Structured Query Language)简称 SQL(发音：sequal['si:kwəl])，是一种数据库查询和程序设计语言，用于存取数据以及查询、更新和管理关系数据库系统。

**SQL 能做什么？**

- SQL 面向数据库执行查询
- SQL 可在数据库中插入新的记录
- SQL 可更新数据库中的数据
- SQL 可从数据库删除记录
- SQL 可创建新数据库
- SQL 可在数据库中创建新表
- SQL 可在数据库中创建存储过程
- SQL 可在数据库中创建视图
- SQL 可以设置表、存储过程和视图的权限

### 2、SQL 标准

SQL 是 1986 年 10 月由美国国家标准局（ANSI）通过的数据库语言美国标准，接着，国际标准化组织（ISO）颁布了 SQL 正式国际标准。1989 年 4 月，ISO 提出了具有完整性特征的 SQL89 标准，1992 年 11 月又公布了 SQL92 标准，在此标准中，把数据库分为三个级别：基本集、标准集和完全集。在 1999 年推出 99 版标准。最新版本为 SQL2016 版。比较有代表性的几个版本：SQL86、SQL92、SQL99。

### 3、SQL语言分类

1. **数据查询语言**（DQL：Data Query Language）其语句，也称为“数据检索语句”，用以从表中获得数据，确定数据怎样在应用程序给出。关键字 SELECT 是 DQL（也是所有 SQL）用得最多的动词。
   - SELECT
   - FROM
   - WHERE
   - ORDER BY
   - HAVING
2. **数据操作语言**（DML：Data Manipulation Language）其语句包括动词 INSERT，UPDATE 和 DELETE。它们分别用于添加，修改和删除表中的行。
   - INSERT：添加数据
   - UPDATE：更新数据
   - DELETE：删除数据
3. **数据定义语言**（DDL：Data Definition Language）定义数据库对象语言，其语句包括动词 CREATE 和 DROP 等。
   - CREATE：创建数据库对象
   - ALTER：修改数据库对象
   - DROP：删除数据库对象
4. **数据控制语言**（DCL：Data Control Language）它的语句通过 GRANT 或 REVOKE 获得许可，确定用户对数据库对象的访问。
   - GRANT：授予用户某种权限
   - REVOKE：回收授予的某种权限
5. **事务控制语言**（TCL ：Transaction Control Language）它的语句能确保被 DML 语句影响的表的所有行及时得以更新。
   - COMMIT：提交事务
   - ROLLBACK：回滚事务
   - SAVEPOINT：设置回滚点

> 注意：
>
> ------
>
> 数据操纵语言DML（insert、update、delete）针对表中的数据 ；
>
> 而数据定义语言DDL（create、alter、drop）针对数据库对象，比如数据库database、表table、索引index、视图view、存储过程procedure、触发器trigger；

### 4、SQL语言语法

1. SQL语句不区分大小写，关键字建议大写。
2. SQL语句可以单行或多行书写，以分号结尾。

**实时效果反馈**

**1**.**SQL语言语法中要求关键字**。

A 不区分大小写

B 区分大小写

C 可简写

D 可省略

**2**.**如下说法正确的是**。

A SQL语句必须多行书写，以分号结尾；

B SQL语句必须单行书写，以分号结尾；

C SQL语句可以单行或多行书写，以冒号结尾；

D SQL语句可以单行或多行书写，以分号结尾;

**答案**

1=>A 2=>D

 创建与删除数据库

## VI、创建数据库

![image-20211107121954202](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107121954202-16362587950835.png)

1. 使用DDL语句创建数据库

   ```
   1
   CREATE DATABASE  数据库名 DEFAULT CHARACTER SET  字符编码;
   ```

   示例：

   创建一个test 的数据库，并查看该数据库，以及该数据库的编码。

   创建数据库：

   ```
   1
   create database test default character set utf8;
   ```

   查看数据库：

   ```
   1
   show databases;
   ```

   查看数据库编码：

   ```
   1
   select schema_name,default_character_set_name from information_schema.schemata 
   ```

   ```
   2
   where schema_name = 'test';
   ```

2. 使用Navicat创建数据库

   示例：

   创建一个test2 的数据库。

   ![image-20211027142925314](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211027142925314.png)

   ![image-20211027143029589](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211027143029589.png)

## VII、删除数据库

![image-20211107122221670](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107122221670-16362589427326.png)

1. 使用DDL语言删除数据库

   ```
   1
   DROP DATABASE  数据库名称;
   ```

   示例：

   删除 test 数据库

   ```
   1
   drop database test;
   ```

2. 使用Navicat删除数据库

   示例：

   删除test2数据库

   ![img](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/SNAGHTML98f7b0d.PNG)

## VIII、	选择数据库

在创建表时，需要先选择数据库。

```
1
USE 数据库名;
```

示例：

创建一个名称为 bjsxt 的数据库，编码为 utf8。

```
1
create database bjsxt default character set utf8;
```

选择该数据库。

```
1
USE bjsxt;
```

**实时效果反馈**

**1**.**创建数据库语句: CREATE 数据库名 DEFAULT CHARACTER SET 字符编码;**

A DATABASE

B DATABASES

C DATA

D BASE

**2**.**删除数据库语句： DATABASE 数据库名称**

A REMOVE

B DELETE

C DROP

D DROPS

**答案**

1=>A 2=>C

## IX、 MySQL中的数据类型

![image-20211107124903917](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107124903917-16362605453877.png)

### 1、整数类型

| **MySQL数据类型** | **含义（有符号）**                   |
| ----------------- | ------------------------------------ |
| tinyint(m)        | 1个字节 范围(-128~127)               |
| smallint(m)       | 2个字节 范围(-32768~32767)           |
| mediumint(m)      | 3个字节 范围(-8388608~8388607)       |
| int(m)            | 4个字节 范围(-2147483648~2147483647) |
| bigint(m)         | 8个字节 范围(+-9.22*10的18次方)      |

数值类型中的长度 m 是指显示长度，并不表示存储长度，只有字段指定 zerofill 时有用

例如： int(3) ，如果实际值是 2 ，如果列指定了 zerofill ，查询结果就是 002 ，左边用 0 来 填充

### 2、浮点类型

| **MySQL数据类型** | **含义**                                      |
| ----------------- | --------------------------------------------- |
| float(m,d)        | 单精度浮点型 8位精度(4字节) m总个数，d小数位  |
| double(m,d)       | 双精度浮点型 16位精度(8字节) m总个数，d小数位 |

### 3、字符类型

| **MySQL数据类型** | **含义**                        |
| ----------------- | ------------------------------- |
| char(n)           | 固定长度，最多255个字符         |
| tinytext          | 可变长度，最多255个字符         |
| varchar(n)        | 可变长度，最多65535个字符       |
| text              | 可变长度，最多65535个字符       |
| mediumtext        | 可变长度，最多2的24次方-1个字符 |
| longtext          | 可变长度，最多2的32次方-1个字符 |

> **char和varchar：**
>
> ------
>
> 1. char长度固定， 即每条数据占用等长字节空间；适合用在身份证号码、手机号码等定长。
> 2. varchar可变长度，可以设置最大长度；适合用在长度可变的属性。
> 3. text不设置长度， 当不知道属性的最大长度时，适合用text。
>
> 按照查询速度： char最快， varchar次之，text最慢。

> **字符串型使用建议：**
>
> ------
>
> 1. 经常变化的字段用varchar
> 2. 知道固定长度的用char
> 3. 尽量用varchar
> 4. 超过255字符的只能用varchar或者text
> 5. 能用varchar的地方不用text

### 4、日期类型

| **MySQL数据类型** | **含义**                     |
| ----------------- | ---------------------------- |
| date              | 日期 YYYY-MM-DD              |
| time              | 时间 HH:MM:SS                |
| datetime          | 日期时间 YYYY-MM-DD HH:MM:SS |
| timestamp         | 时间戳YYYYMMDD HHMMSS        |

### 5、二进制数据(BLOB)

1. BLOB和TEXT存储方式不同，TEXT以文本方式存储，英文存储区分大小写，而Blob是以二进制方式存储，不分大小写。
2. BLOB存储的数据只能整体读出。
3. TEXT可以指定字符集，BLOB不用指定字符集。

**实时效果反馈**

**1**.**数值类型中的 int(m)其中m是指，只有字段指定 zerofill 时有用。**

A 存储长度

B 显示长度

C 固定长度

D 可变长度

**2**.**浮点类型中的double(m,d)其中m是指**。

A 整数长度，

B 小数长度

C 总长度；

D 整数最大值;

**答案**

1=>B 2=>C

## X、 创建表与删除表

### 1、创建表

![image-20211107135440292](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107135440292-163626510919512.png)

1. **使用DDL语句创建表**

   ```
   1
   CREATE TABLE 表名(列名 类型,列名 类型......);
   ```

   示例：

   创建一个 employees 表包含雇员 ID ，雇员名字，雇员薪水。

   ```
   1
   create table employees(employee_id int,employee_name varchar(10),salary float(8,2));
   ```

   查看已创建的表。

   ```
   1
   show tables;
   ```

2. **使用Navicat创建表**

   示例：

   创建employees2表。

![image-20211107140603407](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107140603407-163626516425113.png)

![image-20211107140959312](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107140959312-163626540043415.png)

![image-20211107141049175](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107141049175-163626545004316.png)

### 2、删除表

![image-20211107135421021](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107135421021-16362644620199.png)

1. **使用DDL语句删除表**

   ```
   1
   DROP TABLE 表名;
   ```

   示例：

   删除 employees 表。

   ```
   1
   drop table employees;
   ```

2. **使用Navicat删除表**

   示例：

   删除employees2表

![image-20211107141141771](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107141141771-163626550268317.png)

![image-20211028160316734](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211028160316734-163540819777711.png)

![image-20211107141210141](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107141210141-163626553105018.png)

**实时效果反馈**

**1**.**创建表语句: CREATE (列名 类型,列名 类型......);**

A 表名 TABLES

B TABLES 表名

C 表名 TABLE

D TABLE 表名

**2**.**删除表语句： 表名;**

A REMOVE TABLE

B DELETE TABLE

C DROP TABLE

D TABLE DROP

**答案**

1=>D 2=>C

## XI、修改表

### 1、修改表名

![img](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/SNAGHTML39ea7d0.PNG)

1. **使用DDL语句修改表**

   ```
   1
   ALTER TABLE  旧表名 RENAME  新表名;
   ```

   示例一：

   创建一个 employees 表包含雇员 ID ，雇员名字，雇员薪水。

   ```
   1
   create table employees(employee_id int,employee_name varchar(10),salary float(8,2));
   ```

   复制

   示例二：

   将 employees 表名修改为 emp。

   ```
   1
   alter table employees rename emp;
   ```

2. **使用Navicat修改表名**

   选择表按F2。

![image-20211105170018853](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105170018853-16361028199791.png)

**实时效果反馈**

**1**.**修改表名语句：ALTER TABLE 旧表名 新表名;**

A RENAME

B NAME

C UPDATE NAME

D MODIFY NAME

**答案**

1=>A

###   2、修改列名

![image-20211107143831601](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107143831601-163626711262719.png)

1. **使用DDL语句修改列名**

   ```
   1
   ALTER TABLE  表名 CHANGE COLUMN  旧列名 新列名 类型;
   ```

   示例：

   将 emp 表中的 employee_name 修改为 name。

   ```
   1
   alter table emp change column employee_name name varchar(20);
   ```

   复制

2. **使用Navicat修改列名**

![image-20211105170848542](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105170848542-16361033296002-16361033368643.png)

![image-20211105171208532](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105171208532-16361035294164.png)

**实时效果反馈**

**1**.**修改列名语句：ALTER TABLE 表名 旧列名 新列名 类型;**

A MODIFY COLUMN

B UPDATE COLUMN

C CHANGE COLUMN

D COLUMN

**答案**

1=>C

### 3、修改列类型

![image-20211107145302903](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107145302903-163626798406720.png)

1. **使用DDL语句修改列类型**

   ```
   1
   ALTER TABLE  表名 MODIFY  列名 新类型;
   ```

   示例：

   将 emp 表中的 name 的长度指定为 40。

   ```
   1
   alter table emp modify name varchar(40);
   ```

2. **使用Navicat修改列类型**

![image-20211105172612408](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105172612408-16361043735065.png)

![image-20211105172814098](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105172814098-16361044951106.png)

**实时效果反馈**

**1**.**修改列类型语句：ALTER TABLE 表名 ;**

A UPDATE 列名

B UPDATE 列名 新类型

C MODIFY 列名

D MODIFY 列名 新类型

**答案**

1=>D

###  4、添加新列

![image-20211107150241096](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107150241096-163626856206521.png)

1. **使用DDL语句添加新列**

   ```
   1
   ALTER TABLE  表名 ADD COLUMN  新列名 类型;
   ```

   示例：

   在 emp 表中添加佣金列，列名为 commission_pct。

   ```
   1
   alter table emp add column commission_pct float(4,2);
   ```

2. **使用Navicat添加新列**

![image-20211105173503592](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105173503592-16361049045437.png)

![image-20211105173530862](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105173530862-16361049317838.png)

**实时效果反馈**

**1**.**添加新列语句：ALTER TABLE 表名 ;**

A ADD COLUMN 新列名 类型

B ADD 新列名 类型

C ADD COLUMN 新列名

D COLUMN 新列名 类型

**答案**

1=>A

###  5、删除指定列

![image-20211107150926442](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211107150926442-163626896761222.png)

1. **使用DDL语句删除指定的列**

   ```
   1
   ALTER TABLE  表名 DROP COLUMN  列名;
   ```

   示例：

   删除 emp 表中的 commission_pct。

   ```
   1
   alter table emp drop column commission_pct;
   ```

   复制

2. **使用Navicat删除指定的列**

![image-20211105174133917](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105174133917-16361052949369-163610529884610.png)

![image-20211105174242382](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211105174242382-163610536333511.png)

**实时效果反馈**

**1**.**删除指定列语句：ALTER TABLE 表名 ;**

A REMOVE 列名

B REMOVE COLUMN 列名

C DROP 列名

D DROP COLUMN 列名

**答案**

1=>D

##  XII、MySQL中的约束

![image-20211106192511873](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106192511873-16361979134021.png)

### 1、约束概述

数据库约束是对表中的数据进行进一步的限制，保证数据的正确性、有效性和完整性。

1. **主键约束(Primary Key) PK**

   > 主键约束是使用最频繁的约束。在设计数据表时，一般情况下，都会要求表中设置一个主键。 主键是表的一个特殊字段，该字段能唯一标识该表中的每条信息。例如，学生信息表中的学号是唯一的。

2. **外键约束(Foreign Key) FK**

   > 外键约束经常和主键约束一起使用，用来确保数据的一致性。

3. **唯一性约束(Unique)**

   > 唯一约束与主键约束有一个相似的地方，就是它们都能够确保列的唯一性。与主键约束不同的是，唯一约束在一个表中可以有多个，并且设置唯一约束的列是允许有空值的。

4. **非空约束(Not Null)**

   > 非空约束用来约束表中的字段不能为空。

5. **检查约束(Check)**

   > 检查约束也叫用户自定义约束，是用来检查数据表中，字段值是否有效的一个手段，但目前 MySQL 数据库不支持检查约束。

**实时效果反馈**

**1**.**如下对主键约束描述正确的是。**

A 允许有重复出现，不能有空值

B 不允许有重复出现，但可以有空值

C 不允许有重复出现，不能有空值

D 允许有重复，允许有空值

**2**.**如下对外键约束描述正确的是**。

A 不允许重复，不允许有空值

B 不允许重复，允许有空值

C 允许有重复，不允许有空值

D 允许有重复，允许有空值

**答案**

1=>C 2=>D

###  2、添加主键约束(Primary Key)

1. 单一主键

   使用一个列作为主键列，当该列的值有重复时，则违反唯一约束。

2. 联合主键

   使用多个列作为主键列，当多个列的值都相同时，则违反唯一约束。

#### ①、修改表添加主键约束

1. 使用DDL语句添加主键约束

   ```
   1
   ALTER TABLE  表名 ADD PRIMARY KEY(列名)
   ```

   示例：

   将 emp 表中的 employee_id 修改为主键。

   ```
   1
   alter table emp add primary key(employee_id);
   ```

   复制

   #### ②、主键自增长

   MySQL 中的自动增长类型要求：

   - 一个表中只能有一个列为自动增长。
   - 自动增长的列的类型必须是整数类型。
   - 自动增长只能添加到具备主键约束与唯一性约束的列上。
   - 删除主键约束或唯一性约束，如果该列拥有自动增长能力，则需要先去掉自动增长然 后在删除约束。

   ```
   1
   alter table 表名 modify 主键 类型 auto_increment;
   ```

   示例：

   将 emp 表中的 employee_id 主键修改为自增。

   ```
   1
   alter table emp modify employee_id int auto_increment;
   ```

2. 使用Navicat添加主键约束

![image-20211106153726565](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106153726565-16361842477141.png)

![image-20211106155408963](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106155408963-16361852500313.png)

**实时效果反馈**

**1**.**添加主键约束语句：ALTER TABLE 表名 ;**

A ADD PRIMARY KEY(列名)

B ADD KEY(列名)

C ADD PRIMARY(列名)

D ADD PRIMARY KEY

**答案**

1=>A

### 3、删除主键

1. **使用DDL语句删除主键**

   ```
   1
   ALTER TABLE  表名 DROP PRIMARY KEY;
   ```

   > 注意：
   >
   > ------
   >
   > **删除主键时，如果主键列具备自动增长能力，需要先去掉自动增长，然后在删除 主键。**

   示例：

   删除emp表中的 employee_id 主键约束。

   去掉自动增长：

   ```
   1
   alter table emp modify employee_id int;
   ```

   复制

   删除主键：

   ```
   1
   alter table emp drop primary key;
   ```

2. **使用Navicat删除主键**

![image-20211106155430755](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106155430755-16361852718634.png)

![image-20211106155458431](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106155458431-16361852994875.png)

**实时效果反馈**

**1**.**删除主键约束语句：ALTER TABLE 表名 ;**

A REMOVE PRIMARY

B REMOVE PRIMARY KEY

C DROP PRIMARY KEY

D DROP PRIMARY

**答案**

1=>C

 添加外键约束(Foreign Key)

![20190901112939391](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/20190901112939391.png)

### 4、修改表添加外键约束

1. 使用DDL语句添加外键约束

   ```
   1
   ALTER  TABLE  表名 ADD CONSTRAINT  约束名  FOREIGN  KEY( 列 名 ) REFERENCES  参照的表名(参照的列名);
   ```

   示例一：

   创建 departments 表包含 department_id 、department_name ，location_id。

   ```
   1
   create table departments(department_id int,department_name varchar(30),location_id int);
   ```

   示例二：

   修改departments表，向department_id列添加主键约束与自动递增。

   ```
   1
   alter table departments add primary key(department_id);
   ```

   ```
   2
   alter table departments modify department_id int auto_increment;
   ```

   示例三：

   修改 emp 表，添加 dept_id 列。

   ```
   1
   alter table emp add column dept_id int;
   ```

   示例四：

   向 emp 表中的 dept_id 列添加外键约束。

   ```
   1
   alter table emp add constraint emp_fk foreign key(dept_id) references departments(department_id);
   ```

2. 使用Navicat添加外键约束

![image-20211106161642724](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106161642724-16361866036456.png)

![image-20211106161843815](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106161843815-16361867246937.png)

**实时效果反馈**

**1**.**添加外键约束语句：ALTER TABLE 表名 ADD CONSTRAINT ;**

A FOREIGN KEY( 列 名 ) REFERENCES 参照的表名(参照的列名)

B 约束名 FOREIGN KEY( 列 名 )

C 约束名 ( 列 名 ) REFERENCES 参照的表名(参照的列名)

D 约束名 FOREIGN KEY( 列 名 ) REFERENCES 参照的表名(参照的列名)

**答案**

1=>D

###  5、删除外键约束

1. 使用DDL语句删除外键约束。

   ```
   1
   ALTER TABLE  表名 DROP FOREIGN KEY  约束名;
   ```

   示例：

   删除 dept_id 的外键约束。

   ```
   1
   alter table emp drop foreign key emp_fk;
   ```

2. 使用Navicat删除外键约束

![image-20211106164123290](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106164123290-16361880845188.png)

![image-20211106164226071](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106164226071-16361881469409.png)

**实时效果反馈**

**1**.**删除外键语句：ALTER TABLE 表名 ;**

A REMOVE FOREIGN KEY

B REMOVE FOREIGN KEY 约束名

C DROP FOREIGN KEY 约束名

D DROP FOREIGN KEY

**答案**

1=>C

###  6、添加唯一性约束(Unique)

#### ①、修改表添加唯一性约束

1. 使用DDL语句添加唯一性约束。

   ```
   1
   ALTER TABLE  表名 ADD CONSTRAINT  约束名 UNIQUE(列名);
   ```

   示例：

   向 emp 表中的 name 添加唯一约束。

   ```
   1
   alter table emp add constraint emp_uk unique(name);
   ```

2. 使用Navicat添加唯一性约束

![image-20211106170055725](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106170055725-163618925663510.png)

![image-20211106170109062](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106170109062-163618927031711.png)

**实时效果反馈**

**1**.**添加唯一性约束语句：ALTER TABLE 表名 ADD CONSTRAINT ;**

A UNIQUE(列名)

B 约束名 UNIQUE(列名)

C 约束名 UNIQUE

D 约束名(列名)

**答案**

1=>B

####  ②、删除唯一性约束

1. 使用DDL语句删除唯一性约束。

   ```
   1
   ALTER TABLE  表名 DROP KEY  约束名;
   ```

   示例：

   删除 name 的唯一约束。

   ```
   1
   alter table emp drop key emp_uk;
   ```

2. 使用Navicat删除唯一性约束。

![image-20211106220747921](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106220747921-16362076691381.png)

![image-20211106220809319](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106220809319-16362076903562.png)

**实时效果反馈**

**1**.**删除唯一性约束语句：ALTER TABLE 表名 ;**

A DROP KEY 约束名

B DROP KEY

C REMOVE KEY 约束名

D REMOVE KEY

**答案**

1=>A

 非空约束(Not Null)

### 7、修改表添加非空约束

1. 使用DDL语句添加非空约束。

   ```
   1
   ALTER TABLE  表名 MODIFY  列名 类型 NOT NULL;
   ```

   示例：

   向 emp 表中的 salary 添加非空约束。

   ```
   1
   alter table emp modify salary float(8,2) not NULL;
   ```

2. 使用Navicat添加非空约束。

![image-20211106221241119](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106221241119-16362079620641.png)

![image-20211106221250244](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106221250244-16362079711522.png)

**实时效果反馈**

**1**.**添加非空约束语句：ALTER TABLE 表名 ;**

A UPDATE 列名 NOT NULL

B UPDATE 列名 类型 NOT NULL

C MODIFY 列名 NOT NULL

D MODIFY 列名 类型 NOT NULL

**答案**

1=>D

###  8、删除非空约束

1. 使用DDL语句删除非空约束。

   ```
   1
   ALTER TABLE  表名 MODIFY  列名 类型 NULL;
   ```

   示例：

   删除emp表中salary 的非空约束。

   ```
   1
   alter table emp modify salary float(8,2) NULL;
   ```

2. 使用Navicat删除非空约束。

![image-20211106221602158](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106221602158-16362081632013.png)

![image-20211106221647799](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211106221647799-16362082088084.png)

**实时效果反馈**

**1**.**删除非空约束语句：ALTER TABLE 表名 ;**

A UPDATE 列名 类型 NULL

B UPDATE 类型 NULL

C MODIFY 列名 NULL

D MODIFY 列名 类型 NULL

**答案**

1=>D

###  9、创建表时添加约束

查询表中的约束信息：

```
1
SHOW KEYS FROM  表名;
```

示例：

创建 depts 表包含 department_id 该列为主键且自动增长，department_name 列不 允许重复，location_id 列不允含有空值。

```
1
create table depts(department_id int primary key auto_increment,department_name varchar(30) unique,location_id int not null);
```

 MySQL中DML操作

![img](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/SNAGHTML504ac48.PNG)

## XIII、添加数据(INSERT)

1. **选择插入**

   ```sql
   INSERT INTO  表名(列名 1 ，列名 2 ，列名 3.....) VALUES(值 1 ，值 2 ，值 3......);
   ```
   
   示例：
   
   向 departments 表中添加一条数据，部门名称为 market ，工作地点 ID 为 1。
   
   ```sql
   insert into departments(department_name,location_id) values("market", 1);
   ```
   
2. **完全插入**

```sql
INSERT INTO  表名 VALUES(值 1 ，值 2 ，值 3......);
```

> 注意：
>
> ------
>
> 如果主键是自动增长，需要使用 default 或者 null 或者 0 占位。

示例一：

向 departments 表中添加一条数据，部门名称为 development ，工作地点 ID 为 2 。使用 default 占位。

```
1
insert into departments values(default,"development",2);
```

示例二：

向 departments 表中添加一条数据，部门名称为human ，工作地点 ID 为 3 。使用 null 占 位。

```
1
insert into departments values(null,"human",3);
```

示例三：

向 departments 表中添加一条数据，部门名称为 teaching ，工作地点 ID 为 4 。使用 0 占 位。

```
1
insert into departments values(0,"teaching",4);
```

**实时效果反馈**

**1**.**插入数据时，对于自增长主键占位方式不正确的是;**

A insert into departments values(default,"development",2);

B insert into departments values(null,"development",2);

C insert into departments values(0,"development",2);

D insert into departments values("","development",2);

**答案**

1=>D

##  XIV、默认值处理(DEFAULT)

在 MySQL 中可以使用 DEFAULT 为列设定一个默认值。如果在插入数据时并未指定该列的值，那么 MySQL 会将默认值添加到该列中。

**创建表时指定列的默认值**

```
1
CREATE TABLE 表名(列名 类型 default 默认值,......);
```

示例：

创建 emp3 表，该表包含 emp_id 主键且自动增长，包含 name ，包含 address 该列默认 值为”未知”。

```
1
create table emp3(emp_id int primary key auto_increment,name varchar(10),address varchar(50) default 'Unknown');
```

**修改表添加新列并指定默认值**

```
1
ALTER TABLE 表名 ADD COLUMN 列名 类型 DEFAULT 默认值;
```

复制

示例：

修改 emp3 表，添加job_id 该列默认值为 0。

```
1
alter table emp3 add column job_id int default 0;
```

**插入数据时的默认值处理**

如果在插入数据时并未指定该列的值，那么MySQL 会将默认值添加到该列中。如果是 完全项插入需要使用 default 来占位。

示例：

向 emp3 表中添加数据，要求 address 列与job_id 列使用默认值作为该列的值。

```
1
insert into emp3(name) values("admin");
2
insert into emp3 values(default,"oldlu",default,default);
```

**实时效果反馈**

**1**.**创建表时指定默认值：CREATE TABLE 表名();**

A 列名 default 默认值

B 列名 类型 默认值

C 列名 类型 default 默认值

D default 列名 类型 默认值

**答案**

1=>C

##  XV、更新数据(UPDATE)

```
1
UPDATE 表名 SET  列名=值，列名=值 WHERE 条件;
```

> 注意：
>
> ------
>
> 更新语句中一定要给定更新条件，否则表中的所有数据都会被更新。

示例：

更新 emp3 表中的 id 为 1 的数据，添加 address 为 BeiJing。

```
1
update emp3 set address = "BeiJing" where emp_id = 1;
```

**实时效果反馈**

**1**.**更新数据：UPDATE 表名 ;**

A 列名=值，列名=值 WHERE 条件

B SET 列名=值，列名=值 WHERE 条件

C SET 列名=值 列名=值 WHERE 条件

D WHERE 条件 SET 列名=值，列名=值

**答案**

1=>B

##  XVI、删除数据(DELETE)

**DELETE删除数据**

```
1
DELETE FROM  表名 WHERE 条件;
```

> 注意：
>
> ------
>
> 在DELETE语句中，如果没有给定删除条件则会删除表中的所有数据。

示例：

删除 emp3 表中 emp_id 为 1 的雇员信息。

```
1
delete from emp3 where emp_id = 1;
```

**TRUNCATE清空表**

```
1
TRUNCATE TABLE  表名;
```

示例：

删除 emp3 表中的所有数据。

```
1
truncate table emp3;
```

**清空表时DELETE与 TRUNCATE 区别**

- truncate 是整体删除(速度较快)， delete 是逐条删除(速度较慢)；
- truncate 不写服务器 log，delete 写服务器 log，也就是 truncate 效率比 delete 高的原因；
- truncate 是会重置自增值，相当于自增列会被置为初始值，又重新从 1 开始记录，而 不是接着原来的值。而 delete 删除以后， 自增值仍然会继续累加。

**实时效果反馈**

**1**.**删除数据：DELETE ;**

A 表名 WHERE 条件

B FROM WHERE 条件

C WHERE 条件 FROM 表名

D FROM 表名 WHERE 条件

**答案**

1=>D

 MySQL查询数据

# 二、SELECT基本查询

## I、SELECT语句的功能

![image-20211108102640378](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108102640378-16363384017051.png)

SELECT 语句从数据库中返回信息。使用一个 SELECT 语句，可以做下面的事：

- **列选择：**能够使用 SELECT 语句的列选择功能选择表中的列，这些列是想

  要用查询返回的。当查询时，能够返回列中的数据。

- **行选择：**能够使用 SELECT 语句的行选择功能选择表中的行，这些行是想

  要用查询返回的。能够使用不同的标准限制看见的行。

- **连接：**能够使用 SELECT 语句的连接功能来集合数据，这些数据被存储在不

  同的表中，在它们之间可以创建连接，查询出我们所关心的数据。

## II、SELECT基本语法

![image-20211108102931283](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108102931283-16363385723842.png)

**基本** **SELECT** **语句**

在最简单的形式中，SELECT 语句必须包含下面的内容：

- 一个 SELECT 子句，指定被显示的列
- 一个 FROM 子句，指定表，该表包含 SELECT 子句中的字段列表

在语法中：

| 语句                 | 含义                   |
| -------------------- | ---------------------- |
| SELECT               | 是一个或多个字段的列表 |
| *                    | 选择所有的列           |
| DISTINCT             | 禁止重复               |
| column \| expression | 选择指定的字段或表达式 |
| alias                | 给所选择的列不同的标题 |
| FROM table           | 指定包含列的表         |

## III、添加测试数据

将data.sql文件通过Navicat导入到MySQL中itbz数据库中。该文件包含了课程中所使用的案例表。

![image-20211108153148084](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108153148084-16363567090023.png)

![image-20211108153316448](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108153316448-16363567973974.png)

![image-20211108153434794](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108153434794-16363568757836.png)

![image-20211108153710136](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108153710136-16363570309657.png)

**实时效果反馈**

**1**.**在最简单的查询形式中，SELECT 语句必须包含。**

A 一个SELECT子句，一个FROM子句；

B 一个SELECT子句；

C 一个FROM子句；

D 一个SELECT子句，一个FROM子句，一个INSERT子句；

**答案**

1=>A

##  IV、**查询中的列选择**

### 1、选择所有列

![image-20211108103722679](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108103722679-16363390436823.png)

用跟在 SELECT 关键字后面的星号 (*)，你能够显示表中数据的所有列。

示例：

查询 departments 表中的所有数据。

```
1
select * from departments;
```

### 2、选择指定列

![image-20211108103948162](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108103948162-16363391892004-16363524499811.png)

能够用 SELECT 语句来显示表的指定列，指定列名之间用逗号分隔。

示例：

查询 departments 表中所有部门名称。

```
1
select department_name from departments;
```

**实时效果反馈**

**1**.**用 SELECT 语句来显示表的指定列，指定列名之间用分隔**

A 空格

B 逗号

C 分号

D 冒号

**答案**

1=>B

##  V、**查询中的算术表达式**

![image-20211108104429301](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108104429301-16363394703815.png)

需要修改数据显示方式，如执行计算，或者作假定推测，这些都可能用到算

术表达式。一个算术表达式可以包含列名、固定的数字值和算术运算符。

### **1、使用算术运算符**

![image-20211108105024482](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108105024482-16363398255821.png)

示例：

查询雇员的年薪，并显示他们的雇员ID，名字。

```
1
select employees_id,last_name, 12*salary from employees;
```

### 2、**运算符的优先级**

![image-20211108105139791](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108105139791-16363399007832.png)

如果算术表达式包含有一个以上的运算，乘法和除法先计算。如果在一个表达式中

的运算符优先级相同，计算从左到右进行。可以用圆括号强制其中的表达式先计算。

示例一：

计算 employees 表中的员工全年薪水加 100 以后的薪水是多少，并显示他们的员工ID与名字。

```
1
select employees_id,last_name, 12*salary+100 from employees;
```

示例二：

计算 employees 表中的员工薪水加 100 以后的全年薪水是多少，并显示他们的员工ID与名字。

```
1
select employees_id,last_name, 12*(salary+100) from employees;
```

**实时效果反馈**

**1**.**一个算术表达式可以包含**

A 列名

B 固定的数字值

C 算术运算符

D 列名、固定的数字值和算术运算符

**答案**

1=>D

 **MySQL中定义空值**

![image-20211108105728724](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108105728724-16363402497673.png)

如果一行中的某个列缺少数据值，该值被置为 *null*， 或者说包含一个空。

空是一个难以获得的、未分配的、未知的，或不适用的值。空和 0 或者空格不相同。 0 是一个数字，而空格是一个字符。

### 3、**算术表达式中的空值**

![image-20211108110633517](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108110633517-16363407946564.png)

示例：

计算年薪包含佣金。

```
1
select 12*salary*commission_pct from employees;
```

**实时效果反馈**

**1**.**下列说法正确的是**

A 包含空值的算术表达式结算结果为计算后的值

B 包含空值的算术表达式结算结果为“ ”

C 包含空值的算术表达式结算结果为空

D 包含空值的算术表达式结算结果为0

**答案**

1=>C

##  VI、**MySQL中的别名**

### 1、**使用列别名**

![image-20211108111536276](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108111536276-16363413372703.png)

```
1
SELECT  列名 AS  列别名 FROM  表名 WHERE  条件;
```

复制

示例：

查询 employees 表将雇员 last_name 列定义别名为 name。

```
1
select last_name as name from employees;
2
select last_name name from employees;
```

### 2、使用表别名

```
1
SELECT  表别名.列名  FROM  表名 as 表别名 WHERE  条件;
```

示例：

查询 employees 表为表定义别名为emp，将雇员 last_name 列定义别名为 name。

```
1
select emp.last_name name from employees emp;
```

**实时效果反馈**

**1**.**列别名：SELECT FROM 表名;**

A 列名 AS 列别名 | 列别名

B 列名 AS 列别名 | 列名 列别名

C 列别名 | 列名 列别名

D AS 列别名

**答案**

1=>B

##  VII、**MySQL中去除重复**

![image-20211108111841477](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108111841477-16363415224064.png)

#### **除去相同的行**

![image-20211108111928165](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108111928165-16363415695255.png)

```
1
SELECT DISTINCT 列名 FROM 表名;
```

示例：

查询 employees 表，显示唯一的部门 ID。

```
1
select distinct department_id from employees;
```

去除相同的结果集：

```mysql
SELECT DISTINCT department_id , salary FROM employees;
```

结果：![image-20220713185013023](../AppData/Roaming/Typora/typora-user-images/image-20220713185013023.png)

**实时效果反馈**

**1**.**剔除相同行：SELECT 列名 FROM 表名;**

A DISTINCT

B DISTINCTS

C DIST

D DT

**答案**

1=>A

##  VIII、**查询中的行选择**

![image-20211108112257976](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108112257976-16363417793986.png)

用 WHERE 子句限制从查询返回的行。一个 WHERE 子句包含一个必须满足的条件，WHERE 子句紧跟着 FROM 子句。如果条件是 true，返回满足条件的行。

在语法中：

WHERE 限制查询满足条件的行

*condition* 由列名、表达式、常数和比较操作组成

```
1
SELECT * |  投影列 FROM  表名 WHERE  选择条件;
```

示例：

查询 departments 表中部门 ID 为 90 的部门名称与工作地点 ID。

```
1
select department_name,location_id from departments where department_id =4;
```

**实时效果反馈**

**1**.**用 子句限制从查询返回的行。**

A DISTINCT

B SELECT

C FROM

D WHERE

**答案**

1=>D

##  IX、**MySQL中的比较条件**

![image-20211108113133923](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108113133923-16363422949439.png)

符号 != 也能够表示 不等于条件。

示例一：

查询 employees 表中员工薪水大于等于 3000 的员工的姓名与薪水。

```
1
select last_name,salary from employees where salary >= 3000;
```

示例二：

查询 employees 表中员工薪水不等于 5000 的员工的姓名与薪水。

```
1
select last_name,salary from employees where salary<>5000;
```

**实时效果反馈**

**1**.**在MySQL数据中用表示不等于。**

A <> | ^=

B <> | !=

C <> | 不等于

D ^= | 不等于

**答案**

1=>B

###  1、其他比较条件

![image-20211108113753093](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108113753093-16363426742061.png)

#### ①、**使用BETWEEN条件**

![image-20211108113825997](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108113825997-16363427068472.png)

可以用 BETWEEN 范围条件显示基于一个值范围的行。指定的范围包含一个下限和一个上限。

示例：

查询 employees 表，薪水在 3000-8000 之间的雇员ID、名字与薪水。

```
1
select employee_id,last_name,salary from employees where salary between 3000 and 8000;
```

#### **②、使用IN条件**

![image-20211108114053807](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108114053807-16363428546143.png)

示例：

查询 employees 表，找出薪水是 5000,6000,8000 的雇员ID、名字与薪水。

```
1
select employee_id,last_name,salary from employees where salary in(5000,6000,8000);
```

#### ③、**使用LIKE条件**

![image-20211108114619714](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108114619714-16363431805424.png)

示例：

查询 employees 中雇员名字第二个字母是 e 的雇员名字。

```
1
select last_name from employees where last_name like '_e%';
```

#### ④、**使用NULL条件**

![image-20211108114911070](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108114911070-16363433518785.png)

NULL 条件，包括 IS NULL 条件和 IS NOT NULL 条件。

IS NULL 条件用于空值测试。空值的意思是难以获得的、未指定的、未知的或者不适用的。因此，你不能用 = ，因为 null 不能等于或不等于任何值。

示例一：

找出 emloyees 表中那些没有佣金的雇员雇员ID、名字与佣金。

```
1
select employee_id,last_name,commission_pct from employees where commission_pct is null;
```

示例二：

找出 employees 表中那些有佣金的雇员ID、名字与佣金。

```
1
select employee_id,last_name,commission_pct from employees where commission_pct is not null;
```

**实时效果反馈**

**1**.**如下说法正确的是。**

A 在LIKE语句中，%表示零个或多个字符，_表示一个字符

B 在LIKE语句中，%表示一个字符，_表示零个或多个字符

C 在LIKE语句中，%表示零个，_表示一个字符或多个字符

D 在LIKE语句中，%表示多个字符，_表示一个或零个字符

**答案**

1=>A

###  2、逻辑条件

![image-20211108115116857](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108115116857-16363434779666.png)

逻辑条件组合两个比较条件的结果来产生一个基于这些条件的单个的结果，或者逆

转一个单个条件的结果。当所有条件的结果为真时，返回行。

SQL 的三个逻辑运算符是：

- AND
- OR
- NOT

可以在 WHERE 子句中用 AND 和 OR 运算符使用多个条件。

示例一：

**查询 employees 表中雇员薪水是 8000 的并且名字中含有e 的雇员名字与薪水。**

```
1
select last_name,salary from employees where salary = 8000 and last_name like '%e%';
```

示例二：

**查询 employees 表中雇员薪水是 8000 的或者名字中含有e 的雇员名字与薪水。**

```
1
select last_name,salary from employees where salary = 8000 or last_name like '%e%';
```

示例三：

**查询 employees 表中雇员名字中不包含 u 的雇员的名字。**

```
1
select last_name from employees where last_name not like '%u%';
```

**实时效果反馈**

**1**.**SQL 的三个逻辑运算符是。**

A AND、NULL、NOT

B BETWEEN、OR、NOT

C AND、OR、IN

D AND、OR、NOT

**答案**

1=>D

## X、优先规则

![image-20211108115829130](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108115829130-16363439100477.png)

![image-20211108120010707](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108120010707-16363440115668.png)

在图片的例子中，有两个条件：

- 第一个条件是 job_id 是 AD_PRES 并且薪水高于 15,000。
- 第二个条件是 job_id 是 SA_REP。

![image-20211108120150482](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108120150482-16363441115109.png)

在图片中的例子有两个条件：

- 第一个条件是 job_id 是 AD_PRES 或者 SA_REP 。
- 第二个条件是薪水高于$15,000

**实时效果反馈**

**1**.**对于优先规则，下列说法正确的是。**

A NOT、AND、OR、算术运算

B 算术运算、OR、NOT、AND

C AND、算术运算、NOT、OR

D 算术运算、NOT、AND、OR

**答案**

1=>D

##  XI、**使用 ORDER BY 排序**

![image-20211108120312192](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108120312192-163634419296310.png)

在一个不明确的查询结果中排序返回的行。ORDER BY 子句用于排序。如果使用了 ORDER BY 子句，它必须位于 SQL 语句的最后。

**SELECT 语句的执行顺序如下：**

- FROM 子句
- WHERE 子句
- SELECT 子句
- ORDER BY 子句

示例一：

查询 employees 表中的所有雇员，显示他们的ID、名字与薪水，并按薪水升序排序。

```
1
select employee_id,last_name,salary from employees order by salary;
2
select employee_id,last_name,salary from employees order by salary asc;
```

示例二：

查询 employees 表中的所有雇员，显示他们的ID与名字，并按雇员名字降序排序。

```
1
select employee_id,last_name from employees order by last_name desc;
```

#### **使用别名排序**

![image-20211108120617716](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108120617716-163634437886811.png)

示例：

显示雇员ID，名字。计算雇员的年薪，年薪列别名为annsal，并对该列进行升序排序，

```
1
select employee_id,last_name ,12*salary annsal from employees order by annsal;
```

#### **多列排序**

![image-20211108120933780](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108120933780-163634457463012.png)

示例：

以升叙排序显示 DEPARTMENT_ID 列，同时以降序排序显示 SALARY 列。

```
1
select department_id,salary from employees order by department_id asc ,salary desc;
```

**实时效果反馈**

**1**.**对SELECT 语句的执行顺序描述正确的是。**

A SELECT 子句、FROM 子句、WHERE 子句、ORDER BY 子句

B ORDER BY 子句、FROM 子句、WHERE 子句、SELECT 子句

C WHERE 子句 、FROM 子句、SELECT 子句、ORDER BY 子句

D FROM 子句 、WHERE 子句、SELECT 子句、ORDER BY 子句

**答案**

1=>D

##  XII、SQL查询语句练习##

1.创建一个查询，显示收入超过 12,000 的雇员的名字和薪水。

```sql
SELECT 
employee_id,LAST_NAME,SALARY 
FROM employees 
WHERE SALARY > 12000;
```

2.创建一个查询，显示雇员号为 176 的雇员的名字和部门号。

```sql
SELECT 
EMPLOYEE_ID,LAST_NAME,DEPARTMENT_ID 
FROM employees 
WHERE EMPLOYEE_ID = 176;
```

复制

3.显示所有薪水不在 5000 和 12000 之间的雇员的名字和薪水。

```sql
SELECT 
LAST_NAME,SALARY 
FROM employees 
WHERE SALARY not BETWEEN 5000 AND 12000;
```

4.显示所有在部门 20 和 50 中的雇员的名字和部门号，并以名字按字母顺序排序。

```sql
SELECT 
LAST_NAME,SALARY,DEPARTMENT_ID 
FROM employees 
WHERE DEPARTMENT_ID BETWEEN 20 AND 50 
ORDER BY LAST_NAME ASC; 
```

5.列出收入在 5,000 和 12,000 之间，并且在部门 20 或50 工作的雇员的名字和薪水。将列标题分别显示为 Employee 和 Monthly Salary

```sql
SELECT 
LAST_NAME as Employee,SALARY as 'Monthly Salary' 
FROM employees 
WHERE SALARY BETWEEN 5000 and 12000 AND DEPARTMENT_ID IN (20,50);
```

6.显示所有没有主管经理的雇员的名字和工作岗位。

```sql
SELECT 
LAST_NAME,JOB_ID 
FROM employees
WHERE MANAGER_ID is NULL;
```

7.显示所有有佣金的雇员的名字、薪水和佣金。以薪水和佣金的降序排序数据。

```sql
SELECT 
LAST_NAME,SALARY,COMMISSION_PCT 
FROM employees
WHERE COMMISSION_PCT is not NULL 
ORDER BY SALARY DESC, COMMISSION_PCT DESC;
```

8.显示所有名字中有一个 a 和一个 e 的雇员的名字。

```sql
SELECT 
LAST_NAME
FROM employees 
WHERE LAST_NAME LIKE '%a%' AND LAST_NAME LIKE '%e%';
```

9.显示所有工作岗位是销售代表（SA_REP）或者普通职员(ST_CLERK)，并且薪水不等于 2,500、3,500 或 7,000 的雇员的名字、工作岗位和薪水。

```sql
SELECT 
LAST_NAME,JOB_ID,SALARY 
FROM employees 
WHERE (JOB_ID = 'SA_REP' OR JOB_ID = 'ST_CLERK') 
AND (SALARY != 2500 OR SALARY != 3500 OR SALARY != 7000);
```

 SQL函数

# 三、函数介绍

![image-20211108210615188](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108210615188-16363767761631.png)

函数是 SQL 的一个非常强有力的特性，函数能够用于下面的目的：

- 执行数据计算
- 修改单个数据项
- 操纵输出进行行分组
- 格式化显示的日期和数字
- 转换列数据类型

SQL 函数有输入参数，并且总有一个返回值。

## I、**函数分类**

![image-20211108210836879](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108210836879-16363769178142.png)

1. 单行函数

   单行函数仅对单个行进行运算，并且每行返回一个结果。

   常见的函数类型：

   - 字符
   - 数字
   - 日期
   - 转换

2. 多行函数

多行函数能够操纵成组的行，每个行组给出一个结果，这些函数也被称为组函数。

**实时效果反馈**

**1**.**下列对单行函数描述正确的是。**

A 单行函数对多个行进行运算，并且每行返回一个结果

B 单行函数仅对单个行进行运算，并且每行返回多个结果

C 单行函数仅对单个行进行运算，并且每行返回一个结果

D 单行函数仅对单个行进行运算，并且每行不会返回结果

**答案**

1=>C

 单行函数

![image-20211108211331808](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108211331808-16363772128703.png)

## II、****单行函数分类**

![image-20211108211422620](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108211422620-16363772636544.png)

**实时效果反馈**

**1**.**单行函数包含了。**

A 字符函数、运算函数、日期函数、转换函数、通用函数

B 字符函数、数字函数、日期函数、转换函数、通用函数

C 字符函数、数字函数、处理函数、转换函数、通用函数

D 字符函数、数字函数、日期函数、定义函数、通用函数

**答案**

1=>B

##  III、字符函数

![image-20211108211531513](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211108211531513-16363773333405.png)

**大小写处理函数**

| **函数**           | 描述                  | 实例                                                        |
| ------------------ | --------------------- | ----------------------------------------------------------- |
| LOWER(s)\|LCASE(s) | 将字符串 s 转换为小写 | 将字符串 OLDLU转换为小写：`SELECT LOWER("OLDLU"); -- oldlu` |
| UPPER(s)\|UCASE(s) | 将字符串s转换为大写   | 将字符串 oldlu转换为大写：`SELECT UPPER("oldlu"); -- OLDLU` |

示例：

显示雇员 Davies 的雇员号、姓名和部门号，将姓名转换为大写。

```sql
SELECT
EMPLOYEE_ID,UPPER(LAST_NAME),DEPARTMENT_ID 
FROM employees 
WHERE LAST_NAME = 'davies';
```

**字符处理函数**

| 函数                        | 描述                                                      | 实例                                                         |
| :-------------------------- | :-------------------------------------------------------- | :----------------------------------------------------------- |
| LENGTH(s)                   | 返回字符串 s 的长度                                       | 返回字符串oldlu的字符数`SELECT LENGTH("oldlu"); --5;`        |
| CONCAT(s1,s2...sn)          | 字符串 s1,s2 等多个字符串合并为一个字符串                 | 合并多个字符串`SELECT CONCAT("sxt ", "teacher ", "oldlu"); --sxt teacher oldlu;` |
| LPAD(s1,len,s2)             | 在字符串 s1 的开始处填充字符串 s2，使字符串长度达到 len   | 将字符串 x 填充到 oldlu字符串的开始处：`SELECT LPAD('oldlu',8,'x'); -- xxxoldlu` |
| LTRIM(s)                    | 去掉字符串 s 开始处的空格                                 | 去掉字符串 oldlu开始处的空格：`SELECT LTRIM(" oldlu") ;-- oldlu` |
| REPLACE(s,s1,s2)            | 将字符串 s2 替代字符串 s 中的字符串 s1                    | 将字符串 oldlu 中的字符 o 替换为字符 O：`SELECT REPLACE('oldlu','o','O'); --Oldlu` |
| REVERSE(s)                  | 将字符串s的顺序反过来                                     | 将字符串 abc 的顺序反过来：`SELECT REVERSE('abc'); -- cba`   |
| RPAD(s1,len,s2)             | 在字符串 s1 的结尾处添加字符串 s2，使字符串的长度达到 len | 将字符串 xx填充到 oldlu字符串的结尾处：`SELECT RPAD('oldlu',8,'x'); -- oldluxxx` |
| RTRIM(s)                    | 去掉字符串 s 结尾处的空格                                 | 去掉字符串 oldlu 的末尾空格：`SELECT RTRIM("oldlu "); -- oldlu` |
| SUBSTR(s, start, length)    | 从字符串 s 的 start 位置截取长度为 length 的子字符串      | 从字符串 OLDLU中的第 2 个位置截取 3个 字符：`SELECT SUBSTR("OLDLU", 2, 3); -- LDL` |
| SUBSTRING(s, start, length) | 从字符串 s 的 start 位置截取长度为 length 的子字符串      | 从字符串 OLDLU中的第 2 个位置截取 3个 字符：`SELECT SUBSTRING("OLDLU", 2, 3); --LDL` |
| TRIM(s)                     | 去掉字符串 s 开始和结尾处的空格                           | 去掉字符串 oldlu 的首尾空格：`SELECT TRIM(' oldlu ');--oldlu` |

示例：

显示所有工作岗位名称从第 4 个字符位置开始，包含字符串 REP的雇员的ID信息，将雇员的姓和名连接显示在一起，还显示雇员名的的长度，以及名字中字母 a 的位置。

```sql
SELECT 
employee_id,CONCAT(LAST_NAME,FIRST_NAME),JOB_ID,LENGTH(LAST_NAME),INSTR(LAST_NAME,'a') "Contains 'a'?"  ## 如果有a，则输出a出现的位置，无a，输出0；
FROM employees
WHERE SUBSTR(JOB_ID,4) = 'REP';
```

##  IV、**数字函数**

| 函数名                             | 描述                                                         | 实例                                                         |
| :--------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| ABS(x)                             | 返回 x 的绝对值                                              | 返回 -1 的绝对值：`SELECT ABS(-1) -- 返回1`                  |
| ACOS(x)                            | 求 x 的反余弦值(参数是弧度)                                  | `SELECT ACOS(0.25);`                                         |
| ASIN(x)                            | 求反正弦值(参数是弧度)                                       | `SELECT ASIN(0.25);`                                         |
| ATAN(x)                            | 求反正切值(参数是弧度)                                       | `SELECT ATAN(2.5);`                                          |
| ATAN2(n, m)                        | 求反正切值(参数是弧度)                                       | `SELECT ATAN2(-0.8, 2);`                                     |
| AVG(expression)                    | 返回一个表达式的平均值，expression 是一个字段                | 返回 Products 表中Price 字段的平均值：`SELECT AVG(Price) AS AveragePrice FROM Products;` |
| CEIL(x)                            | 返回大于或等于 x 的最小整数                                  | `SELECT CEIL(1.5) -- 返回2`                                  |
| CEILING(x)                         | 返回大于或等于 x 的最小整数                                  | `SELECT CEILING(1.5); -- 返回2`                              |
| COS(x)                             | 求余弦值(参数是弧度)                                         | `SELECT COS(2);`                                             |
| COT(x)                             | 求余切值(参数是弧度)                                         | `SELECT COT(6);`                                             |
| COUNT(expression)                  | 返回查询的记录总数，expression 参数是一个字段或者 * 号       | 返回 Products 表中 products 字段总共有多少条记录：`SELECT COUNT(ProductID) AS NumberOfProducts FROM Products;` |
| DEGREES(x)                         | 将弧度转换为角度                                             | `SELECT DEGREES(3.1415926535898) -- 180`                     |
| n DIV m                            | 整除，n 为被除数，m 为除数                                   | 计算 10 除于 5：`SELECT 10 DIV 5; -- 2`                      |
| EXP(x)                             | 返回 e 的 x 次方                                             | 计算 e 的三次方：`SELECT EXP(3) -- 20.085536923188`          |
| FLOOR(x)                           | 返回小于或等于 x 的最大整数                                  | 小于或等于 1.5 的整数：`SELECT FLOOR(1.5) -- 返回1`          |
| GREATEST(expr1, expr2, expr3, ...) | 返回列表中的最大值                                           | 返回以下数字列表中的最大值：`SELECT GREATEST(3, 12, 34, 8, 25); -- 34`返回以下字符串列表中的最大值：`SELECT GREATEST("Google", "Runoob", "Apple"); -- Runoob` |
| LEAST(expr1, expr2, expr3, ...)    | 返回列表中的最小值                                           | 返回以下数字列表中的最小值：`SELECT LEAST(3, 12, 34, 8, 25); -- 3`返回以下字符串列表中的最小值：`SELECT LEAST("Google", "Runoob", "Apple"); -- Apple` |
| LN                                 | 返回数字的自然对数，以 e 为底。                              | 返回 2 的自然对数：`SELECT LN(2); -- 0.6931471805599453`     |
| LOG(x) 或 LOG(base, x)             | 返回自然对数(以 e 为底的对数)，如果带有 base 参数，则 base 为指定带底数。 | `SELECT LOG(20.085536923188) -- 3 SELECT LOG(2, 4); -- 2`    |
| LOG10(x)                           | 返回以 10 为底的对数                                         | `SELECT LOG10(100) -- 2`                                     |
| LOG2(x)                            | 返回以 2 为底的对数                                          | 返回以 2 为底 6 的对数：`SELECT LOG2(6); -- 2.584962500721156` |
| MAX(expression)                    | 返回字段 expression 中的最大值                               | 返回数据表 Products 中字段 Price 的最大值：`SELECT MAX(Price) AS LargestPrice FROM Products;` |
| MIN(expression)                    | 返回字段 expression 中的最小值                               | 返回数据表 Products 中字段 Price 的最小值：`SELECT MIN(Price) AS MinPrice FROM Products;` |
| MOD(x,y)                           | 返回 x 除以 y 以后的余数                                     | 5 除于 2 的余数：`SELECT MOD(5,2) -- 1`                      |
| PI()                               | 返回圆周率(3.141593）                                        | `SELECT PI() --3.141593`                                     |
| POW(x,y)                           | 返回 x 的 y 次方                                             | 2 的 3 次方：`SELECT POW(2,3) -- 8`                          |
| POWER(x,y)                         | 返回 x 的 y 次方                                             | 2 的 3 次方：`SELECT POWER(2,3) -- 8`                        |
| RADIANS(x)                         | 将角度转换为弧度                                             | 180 度转换为弧度：`SELECT RADIANS(180) -- 3.1415926535898`   |
| RAND()                             | 返回 0 到 1 的随机数                                         | `SELECT RAND() --0.93099315644334`                           |
| ROUND(x)                           | 返回离 x 最近的整数                                          | `SELECT ROUND(1.23456) --1`                                  |
| SIGN(x)                            | 返回 x 的符号，x 是负数、0、正数分别返回 -1、0 和 1          | `SELECT SIGN(-10) -- (-1)`                                   |
| SIN(x)                             | 求正弦值(参数是弧度)                                         | `SELECT SIN(RADIANS(30)) -- 0.5`                             |
| SQRT(x)                            | 返回x的平方根                                                | 25 的平方根：`SELECT SQRT(25) -- 5`                          |
| SUM(expression)                    | 返回指定字段的总和                                           | 计算 OrderDetails 表中字段 Quantity 的总和：`SELECT SUM(Quantity) AS TotalItemsOrdered FROM OrderDetails;` |
| TAN(x)                             | 求正切值(参数是弧度)                                         | `SELECT TAN(1.75); -- -5.52037992250933`                     |
| TRUNCATE(x,y)                      | 返回数值 x 保留到小数点后 y 位的值（与 ROUND 最大的区别是不会进行四舍五入） | `SELECT TRUNCATE(1.23456,3) -- 1.234`                        |

**ROUND(\*column\*|\*expression\*, \*n\*)** **函数**

ROUND 函数四舍五入列、表达式或者 n 位小数的值。如果第二个参数是 0 或者缺少，值被四舍五入为整数。如果第二个参数是 2值被四舍五入为两位小数。如果第二个参数是–2，值被四舍五入到小数点左边两位。

```sql
SELECT ROUND(45.923,2), ROUND(45.923,0),ROUND(45.923,-1); ## 45.92,46,50
```

**TRUNCATE(\*column\*|\*expression\*,\*n\*) 函数**

TRUNCATE函数的作用类似于 ROUND 函数。如果第二个参数是 0 或者缺少，值被截断为整数。如果第二个参数是 2，值被截断为两位小数。如果第二个参数是–2，值被截断到小数点左边两位。与 ROUND 最大的区别是不会进行四舍五入。

```sql
SELECT TRUNCATE(45.923,2); ## 45.92
```

**使用MOD(\*m\*,\*n\*) 函数**

MOD 函数找出m 除以n的余数。

示例：

所有job_id是SA_REP的雇员的名字，薪水以及薪水被5000除后的余数。

```sql
SELECT 
LAST_NAME,SALARY,MOD(SALARY,5000) 
FROM employees 
WHERE JOB_ID = 'SA_REP';
```

##  V、**日期函数**

在MySQL中允许直接使用字符串表示日期，但是要求字符串的日期格式必须为：‘YYYY-MM-DD HH:MI:SS’ 或者‘YYYY/MM/DD HH:MI:SS’;

| 函数名                 | 描述                                              | 实例                                                   |
| :--------------------- | :------------------------------------------------ | :----------------------------------------------------- |
| CURDATE()              | 返回当前日期                                      | `SELECT CURDATE(); -> 2018-09-19`                      |
| CURTIME()              | 返回当前时间                                      | `SELECT CURTIME(); -> 19:59:02`                        |
| CURRENT_DATE()         | 返回当前日期                                      | `SELECT CURRENT_DATE(); -> 2018-09-19`                 |
| CURRENT_TIME()         | 返回当前时间                                      | `SELECT CURRENT_TIME(); -> 19:59:02`                   |
| DATE()                 | 从日期或日期时间表达式中提取日期值                | `SELECT DATE("2017-06-15"); -> 2017-06-15`             |
| DATEDIFF(d1,d2)        | 计算日期 d1->d2 之间相隔的天数                    | `SELECT DATEDIFF('2001-01-01','2001-02-02') -> -32`    |
| DAY(d)                 | 返回日期值 d 的日期部分                           | `SELECT DAY("2017-06-15"); -> 15`                      |
| DAYNAME(d)             | 返回日期 d 是星期几，如 Monday,Tuesday            | `SELECT DAYNAME('2011-11-11 11:11:11') ->Friday`       |
| DAYOFMONTH(d)          | 计算日期 d 是本月的第几天                         | `SELECT DAYOFMONTH('2011-11-11 11:11:11') ->11`        |
| DAYOFWEEK(d)           | 日期 d 今天是星期几，1 星期日，2 星期一，以此类推 | `SELECT DAYOFWEEK('2011-11-11 11:11:11') ->6`          |
| DAYOFYEAR(d)           | 计算日期 d 是本年的第几天                         | `SELECT DAYOFYEAR('2011-11-11 11:11:11') ->315`        |
| HOUR(t)                | 返回 t 中的小时值                                 | `SELECT HOUR('1:2:3') -> 1`                            |
| LAST_DAY(d)            | 返回给给定日期的那一月份的最后一天                | `SELECT LAST_DAY("2017-06-20"); -> 2017-06-30`         |
| MONTHNAME(d)           | 返回日期当中的月份名称，如 November               | `SELECT MONTHNAME('2011-11-11 11:11:11') -> November`  |
| MONTH(d)               | 返回日期d中的月份值，1 到 12                      | `SELECT MONTH('2011-11-11 11:11:11') ->11`             |
| NOW()                  | 返回当前日期和时间                                | `SELECT NOW() -> 2018-09-19 20:57:43`                  |
| SECOND(t)              | 返回 t 中的秒钟值                                 | `SELECT SECOND('1:2:3') -> 3`                          |
| SYSDATE()              | 返回当前日期和时间                                | `SELECT SYSDATE() -> 2018-09-19 20:57:43`              |
| TIMEDIFF(time1, time2) | 计算时间差值                                      | `SELECT TIMEDIFF("13:10:11", "13:10:10"); -> 00:00:01` |
| TO_DAYS(d)             | 计算日期 d 距离 0000 年 1 月 1 日的天数           | `SELECT TO_DAYS('0001-01-01 01:01:01') -> 366`         |
| WEEK(d)                | 计算日期 d 是本年的第几个星期，范围是 0 到 53     | `SELECT WEEK('2011-11-11 11:11:11') -> 45`             |
| WEEKDAY(d)             | 日期 d 是星期几，0 表示星期一，1 表示星期二       | `SELECT WEEKDAY("2017-06-15"); -> 3`                   |
| WEEKOFYEAR(d)          | 计算日期 d 是本年的第几个星期，范围是 0 到 53     | `SELECT WEEKOFYEAR('2011-11-11 11:11:11') -> 45`       |
| YEAR(d)                | 返回年份                                          | `SELECT YEAR("2017-06-15"); -> 2017`                   |

示例一：

向 employees 表中添加一条数据，雇员ID：300，名字：kevin ，email：[kevin@sxt.cn](mailto:kevin@sxt.cn) ，入职时间：2049-5-1 8:30:30，工作部门：‘IT_PROG’。

```sql
INSERT into 
employees(EMPLOYEE_ID,LAST_NAME,EMAIL,HIRE_DATE,JOB_ID) 
VALUES(300,'kevin','kevin@sxt.cn','2049-5-1 8:30:30','IT_PROG');
```

示例二：

显示所有在部门 90 中的雇员的名字和从业的周数。雇员的总工作时间以周计算，用当前日期 (SYSDATE) 减去雇员的受顾日期，再除以 7。

```sql
SELECT 
LAST_NAME,(SYSDATE() - HIRE_DATE)/7 AS weeks 
FROM employees 
WHERE DEPARTMENT_ID = 90;
```

## VI、**转换函数**

![image-20211109150738622](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211109150738622-16364416595681.png)

**隐式数据类型转换**

隐式数据类型转换是指MySQL服务器能够自动地进行类型转换。如：可以将标准格式的字串日期自动转换为日期类型。

MySQL字符串日期格式为：‘YYYY-MM-DD HH:MI:SS’ 或 ‘YYYY/MM/DD HH:MI:SS’;

**显示数据类型转换**

显示数据类型转换是指需要依赖转换函数来完成相关类型的转换。

如：

- DATE_FORMAT(date,format) 将日期转换成字符串;
- STR_TO_DATE(str,format) 将字符串转换成日期;

**![image-20211029173950157](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211029173950157-16355003925931.png)**

示例一：

向 employees 表中添加一条数据，雇员ID：400，名字：oldlu ，email：[oldlu@sxt.cn](mailto:oldlu@sxt.cn) ，入职时间：2049 年 5 月 5 日，工作部门：‘IT_PROG’。

```sql
insert  into employees(EMPLOYEE_ID,last_name,email,HIRE_DATE,JOB_ID)  values(400,'oldlu','oldlu@sxt.cn', STR_TO_DATE('2049 年 5 月 5 日','%Y 年%m 月%d 日'),'IT_PROG');
```

示例二：

查询 employees 表中雇员名字为 King 的雇员的入职日期，要求显示格式为 yyyy 年 MM 月 dd 日。

```sql
select DATE_FORMAT(hire_date,'%Y 年%m 月%d 日') 
from employees 
where last_name = 'King';
```

 



##  VII、**通用函数**

| 函数名                                                       | 描述                                                         | 实例                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| IF(expr,v1,v2)                                               | 如果表达式 expr 成立，返回结果 v1；否则，返回结果 v2。       | `SELECT IF(1 > 0,'正确','错误') ->正确`                      |
| IFNULL(v1,v2)                                                | 如果 v1 的值不为 NULL，则返回 v1，否则返回 v2。              | `SELECT IFNULL(null,'Hello Word') ->Hello Word`              |
| ISNULL(expression)                                           | 判断表达式是否为 NULL                                        | `SELECT ISNULL(NULL); ->1`                                   |
| NULLIF(expr1, expr2)                                         | 比较两个参数是否相同，如果参数 expr1 与 expr2 相等 返回 NULL，否则返回 expr1 | `SELECT NULLIF(25, 25); ->`                                  |
| COALESCE(expr1, expr2, ...., expr_n)                         | 返回参数中的第一个非空表达式（从左向右）                     | `SELECT COALESCE(NULL, NULL, NULL, 'bjsxt.com', NULL, 'google.com'); -> bjsxt.com` |
| `CASE expression WHEN condition1 THEN result1 WHEN condition2 THEN result2 ... WHEN conditionN THEN resultN ELSE result END` | CASE 表示函数开始，END 表示函数结束。如果 condition1 成立，则返回 result1, 如果 condition2 成立，则返回 result2，当全部不成立则返回 result，而当有一个成立之后，后面的就不执行了。 | `SELECT CASE 'oldlu' WHEN 'oldlu' THEN 'OLDLU' WHEN 'admin' THEN 'ADMIN' ELSE 'kevin' END;` |

示例一：

查询部门编号是50或者80的员工信息，包含他们的名字、薪水、佣金。在income列中，如果有佣金则显示‘SAL+COMM’，无佣金则显示'SAL'。

```sql
SELECT LAST_NAME,SALARY,COMMISSION_PCT,
IF(ISNULL(COMMISSION_PCT),'SAL','SAL+COMM') income
FROM employees 
WHERE DEPARTMENT_ID in (50,80);
```

示例二：

计算雇员的年报酬，你需要用 12 乘以月薪，再加上它的佣金 (等于年薪乘以佣金

百分比)。

```sql
SELECT LAST_NAME,SALARY,IFNULL(COMMISSION_PCT,0),
(SALARY * 12) + (SALARY * 12 * IFNULL(COMMISSION_PCT,0)) AN_SAL
FROM employees;
```

示例三

查询员工表，显示他们的名字、名字的长度该列名为expr1，姓氏、姓氏的长度该列名为expr2。在result列中，如果名字与姓氏的长度相同则显示空，如果不相同则显示名字长度。

```sql
SELECT FIRST_NAME,LENGTH(FIRST_NAME) 'expr1',LAST_NAME,LENGTH(LAST_NAME) 'expr2',
NULLIF(LENGTH(FIRST_NAME),LENGTH(LAST_NAME)) result
FROM employees;
```

示例四：

查询员工表，显示他们的名字，如果 COMMISSION_PCT 值是非空，显示它。如果COMMISSION_PCT 值是空，则显示 SALARY 。如果 COMMISSION_PCT 和SALARY 值都是空，那么显示 10。在结果中对佣金列升序排序。

```sql
SELECT LAST_NAME,
COALESCE(COMMISSION_PCT,SALARY,10) 
FROM employees;
```

示例五：

查询员工表，如果 JOB_ID 是 IT_PROG，薪水增加 10%；如果 JOB_ID 是 ST_CLERK，薪水增加 15%；如果 JOB_ID 是 SA_REP，薪水增加 20%。对于所有其他的工作角色，不增加薪水。

```sql
SELECT LAST_NAME,JOB_ID,SALARY,
case JOB_ID WHEN 'IT_PROG' THEN 1.10 * SALARY
						WHEN 'ST_CLERK' THEN 1.13 * SALARY
						WHEN 'SA_REP' THEN 1.20 * SALARY
			ELSE SALARY END 'revised_salary'
FROM employees;
```

## VIII、##函数查询练习##

1.显示受雇日期在 1998 年 2 月 20 日 和 2005 年 5 月 1 日 之间的雇员的名字、岗位

和受雇日期。按受雇日期顺序排序查询结果。

```sql
SELECT LAST_NAME,JOB_ID,HIRE_DATE 
FROM employees 
WHERE HIRE_DATE BETWEEN '1998-2-20' AND '2005-5-1' 
ORDER BY HIRE_DATE ASC;
```

2.显示每一个在 2002 年受雇的雇员的名字和受雇日期。

```sql
SELECT LAST_NAME,HIRE_DATE 
FROM employees 
WHERE HIRE_DATE LIKE '2002%';
```

3.对每一个雇员，显示 employee number、last_name、salary 和 salary 增加 15%，

并且表示成整数，列标签显示为 New Salary。

```sql
SELECT 
EMPLOYEE_ID 'employee number',LAST_NAME,SALARY, 
ROUND(SALARY * 1.15) AS 'New Salary'
FROM employees;
```

4.写一个查询，显示名字的长度，对所有名字开始字母是 J、A 或 M 的雇员。用雇员的 last

name排序结果。

```sql
SELECT LAST_NAME,LENGTH(LAST_NAME) 
FROM employees 
WHERE LAST_NAME LIKE 'J%' 
OR 
LAST_NAME LIKE 'A%' 
OR 
LAST_NAME LIKE 'M%' 
ORDER BY LAST_NAME;
```

5.创建一个查询显示所有雇员的 last name 和 salary。将薪水格式化为 15 个字符长度，用 $左填充 。

```sql
SELECT 
LAST_NAME,SALARY,LPAD(SALARY,15,'$') 
FROM employees;
```

6.创建一个查询显示雇员的 last names 和 commission (佣金) 比率。如果雇员没有佣金，显示 “No Commission”，列标签 COMM。

```sql
SELECT LAST_NAME,
IFNULL(COMMISSION_PCT,'No Commission') COMM
FROM employees; 
```

7.写一个查询，按照下面的数据显示所有雇员的基于 JOB_ID 列值的级别。

| **工作**   | **级别** |
| ---------- | -------- |
| AD_PRES    | A        |
| ST_MAN     | B        |
| IT_PROG    | C        |
| SA_REP     | D        |
| ST_CLERK   | E        |
| 不在上面的 | 0        |

```sql
SELECT LAST_NAME,JOB_ID,
CASE JOB_ID
	WHEN 'AD_PRES' THEN 'A'
	WHEN 'ST_MAN' THEN 'B'
	WHEN 'IT_PROG' THEN 'C'
	WHEN 'SA_REP' THEN 'D'
	WHEN 'ST_CLERK' THEN 'E'
	ELSE 0
END  FROM employees;
```

# 四、 多表查询

## I、多表查询简介

![image-20211109210304519](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211109210304519-16364629854821.png)

## II、**笛卡尔乘积**

![image-20211109210407967](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211109210407967-16364630489612.png)

笛卡尔乘积 ：

当一个连接条件无效或被遗漏时，其结果是一个笛卡尔乘积 (*Cartesian product*)，其中所有行的组合都被显示。第一个表中的所有行连接到第二个表中的所有行。一个笛卡尔乘积会产生大量的行，其结果没有什么用。你应该在 WHERE 子句中始终包含一个有效的连接条件，除非你有特殊的需求，需要从所有表中组合所有的行。

![image-20211109210502723](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211109210502723-16364631036263.png)

**多表查询分类**

- sql92标准：内连接(等值连接 、非等值连接 、 自连接)。
- sql99标准：内连接、外连接(左外、右外、全外(MySQL不支持全外连接))、交叉连接。

**实时效果反馈**

**1**.**当一个无效或被遗漏时，其结果是一个笛卡尔乘积。**

A 运算符

B 函数运算

C 连接条件

D 排序

**答案**

1=>C

##  III、SQL92标准中的查询

### ①、等值连接

![image-20211109210650492](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211109210650492.png)

**等值连接**

为了确定一个雇员的部门名，需要比较 EMPLOYEES 表中的 DEPARTMENT_ID 列与DEPARTMENTS 表中的 DEPARTMENT_ID 列的值。在 EMPLOYEES 和DEPARTMENTS 表之间的关系是一个相等 (*equijoin*) 关系，即，两 个 表 中DEPARTMENT_ID 列的值必须相等。

**等值连接特点：**

1. 多表等值连接的结果为多表的交集部分；
2. n表连接，至少需要n-1个连接条件；
3. 多表不分主次，没有顺序要求；
4. 一般为表起别名，提高阅读性和性能；
5. 可以搭配排序、分组、筛选….等子句使用；

> 注意：
>
> ------
>
> 等值连接也被称为简单连接 (*simple joins*) 或内连接 (*inner joins*)。



#### (1）、等值连接的使用

![image-20211110160356636](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110160356636-16365314377462.png)

- **SELECT 子句指定要返回的列名：**

  − employee last name、employee number 和 department number，这些是

EMPLOYEES 表中的列

− department number、department name 和 location ID，这些

是 DEPARTMENTS 表中的列

- **FROM 子句指定数据库必须访问的两个表：**

− EMPLOYEES 表

− DEPARTMENTS 表

- **WHERE 子句指定表怎样被连接：**

  EMPLOYEES.DEPARTMENT_ID = DEPARTMENTS.DEPARTMENT_ID，因为 DEPARTMENT_ID 列是两个表的同名列，它必须用表名做前缀以避免混淆。

**增加搜索条件**

![image-20211110161209183](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110161209183-16365319302643.png)

**添加查询条件**

除连接之外，可能还要求用 WHERE 子句在连接中限制一个或多个表中的行。

**限制不能缺的列**

![image-20211110161457766](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110161457766-16365320985914.png)

**限制不明确的列名**

- 需要在 WHERE 子句中用表的名字限制列的名字以避免含糊不清。没有表前缀，DEPARTMENT_ID 列可能来自 DEPARTMENTS 表，也可能来自 EMPLOYEES 表，这种情况下需要添加表前缀来执行查询。
- 如果列名在两个表之间不相同，就不需要限定列。但是，使用表前缀可以改善性能，因为MySQL服务器可以根据表前缀找到对应的列。
- 必须限定不明确的列名也适用于在其它子句中可能引起混淆的那些列，例如 SELECT子句或 ORDER BY 子句。

#### (2）、使用表别名

![image-20211110161836968](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110161836968-16365323178325.png)

**表别名定义原则**

- 表别名不易过长，短一些更好。
- 表别名应该是有意义的。
- 表别名只对当前的 SELECT 语句有效。

#### (3）、多表连接

![image-20211110162219581](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110162219581-16365325404576.png)

示例一：

**查询雇员 King 所在的部门名称。**

```sql
SELECT
e.LAST_NAME,d.DEPARTMENT_ID,d.DEPARTMENT_NAME
FROM employees e,departments d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID AND e.LAST_NAME = 'King';
```

示例二：

**显示每个雇员的 last name、departmentname 和 city。**

```sql
SELECT
e.LAST_NAME,d.DEPARTMENT_NAME,l.CITY
FROM employees e,departments d,locations l
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID 
AND d.LOCATION_ID = l.LOCATION_ID
```

**实时效果反馈**

**1**.**n表连接，至少需要个连接条件。**

A n

B 1

C n-1

D n+1

**2**.**等值连接是使用作为连接条件。**

A 值的相等性

B 值的相反性

C 值的不同性

D 值的相似性

**答案**

1=>C 2=>A

###  ②、非等值连接

![image-20211110163639343](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110163639343-16365334003617.png)

**非等值连接**

一个非等值连接是一种不同于等值操作的连接条件。 EMPLOYEES 表 和JOB_GRADES A 表之间的关系有一个非等值连接例子。在两个表之间的关系是EMPLOYEES 表中的 SALARY 列必须是 JOB_GRADES 表的 LOWEST_SALARY 和HIGHEST_SALARY 列之间的值。使用不同于等于 (=) 的操作符获得关系。

![image-20211110163927675](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110163927675-16365335687038.png)

示例一：

创建 job_grades 表，包含 lowest_sal ，highest_sal ，grade_level。

```sql
CREATE TABLE job_grands(lowest_sal int,highest_sal int,grade_level VARCHAR(30));
```

示例二：

插入数据

1000 2999 A 2000 4999 B 5000 7999 C 8000 12000 D

```sql
INSERT into job_grands VALUES (1000,2999,'A');
INSERT into job_grands VALUES (2000,4999,'B');
INSERT into job_grands VALUES (5000,7999,'C');
INSERT into job_grands VALUES (8000,12000,'D');
```

示例三：

查询所有雇员的薪水级别。

```sql
SELECT
e.LAST_NAME,e.SALARY,j.grade_level
FROM employees e,job_grands j
WHERE e.SALARY BETWEEN j.lowest_sal AND j.highest_sal
```

**实时效果反馈**

**1**.**如下说法错误的是。**

A 一个非等值连接是一种使用等值作为连接条件。

B 一个非等值连接是一种使用大于作为连接条件。

C 一个非等值连接是一种使用小于作为连接条件。

D 一个非等值连接是一种使用不等于作为连接条件。

**答案**

1=>A

 **自连接**

![image-20211110165141357](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110165141357-16365343024909.png)

### ③、自连接

连接一个表到它自己。有时需要连接一个表到它自己。为了找到每个雇员的经理的名字，则需要连接EMPLOYEES 表到它自己，或执行一个自连接。

![image-20211110165938122](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110165938122-163653477908210.png)

图片中的例子连接 EMPLOYEES 表到它自己。为了在 FROM 子句中模拟两个表，对于相同的表 EMPLOYEES，用两个别名，分别为 worker 和 manager。在该例中，WHERE 子句包含的连接意味着 “一个工人的经理号匹配该经理的雇员号”。

示例一：

查询每个雇员的经理的名字以及雇员的名字，雇员名字列别名为W，经理列别名为M。

```sql
SELECT
worker.LAST_NAME W,manager.LAST_NAME M
FROM employees worker,employees manager
WHERE worker.MANAGER_ID = manager.EMPLOYEE_ID
```

示例二：

查询Fox的经理是谁？显示他的名字。

```sql
SELECT
worker.LAST_NAME W,manager.LAST_NAME M
FROM employees worker,employees manager
WHERE worker.MANAGER_ID = manager.EMPLOYEE_ID 
AND worker.LAST_NAME = 'fox';
```

**实时效果反馈**

**1**.**如下描述自连接正确的是。**

A 一个表不允许自己连接自己

B 连接一个表到它自己就是自连接

C 自连接不能有连接条件

D 自连接中不能使用where子句

**答案**

1=>B

##  IV、**SQL99标准中的查询**

MySQL5.7 支持部分的SQL99 标准。

### ①、SQL99中的交叉连接(CROSS JOIN)

![image-20211110172705595](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110172705595-163653642666511.png)

示例：

使用交叉连接查询 employees 表与 departments 表。

```sql
select * from employees cross join departments;
```

**实时效果反馈**

**1**.**交叉连接(CROSS JOIN)是SQL的标准。**

A 1986

B 1992

C 1999

D 2016

**答案**

1=>C

###  ②、SQL99中的自然连接(NATURAL JOIN)

![image-20211110172829809](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110172829809-163653651077512.png)

**自然连接**

连接只能发生在两个表中有相同名字和数据类型的列上。如果列有相同的名字，但

数据类型不同，NATURAL JOIN 语法会引起错误。

**自然连接查询**

![image-20211110173037723](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110173037723-163653663856813.png)

在图片例子中，LOCATIONS 表被用 LOCATION_ID 列连接到 DEPARTMENT表，这是在两个表中唯一名字相同的列。如果存在其它的同名同类型的列，自然连接会使用等值连接的方式连接他们，连接条件的关系为and。

自然连接也可以被写为等值连接：

SELECT d.department_id, d.department_name,

d.location_id , l.city

FROM

departments d , locations l

WHERE

d.location_id = l.location_id;

示例：

使用自然连接查询所有有部门的雇员的名字以及部门名称。

```sql
select 
e.last_name,d.department_name 
from employees e natural join departments d;
```

**实时效果反馈**

**1**.**自然连接中，如有多个类型与名称相同的列，在连接时连接条件的关系为。**

A OR

B IN

C NOT

D AND

**答案**

1=>D

###  ③、SQL99中的内连接(INNER JOIN)

![image-20211110203253221](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110203253221-16365475740264.png)

**语法：**

- SELECT 查询列表;
- FROM 表1 别名;
- INNER JOIN 连接表(INNER关键字可省略);
- ON 连接条件;

**用ON子句指定连接条件**

![image-20211110205055326](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110205055326-16365486564269.png)

**用ON子句指定更多的连接条件**

![image-20211110205210282](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110205210282-163654873108111.png)

示例:

查询雇员名字为 Fox 的雇员 ID ，薪水与部门名称。

```sql
SELECT
e.LAST_NAME,e.EMPLOYEE_ID,e.SALARY,d.DEPARTMENT_NAME
FROM employees e JOIN departments d ON e.DEPARTMENT_ID = d.DEPARTMENT_ID
WHERE e.LAST_NAME = 'fox';
```

**实时效果反馈**

**1**.**在内连接中使用指定连接的表，用指定连接条件。**

A INNER JOIN ON

B BETWEEN ON

C INNER JOIN IN

D BETWEEN AND

**答案**

1=>A

###  ④、外连接查询(OUTER JOIN)

![image-20211110210754164](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110210754164-163654970598815.png)

**孤儿数据(Orphan Data)**

孤儿数据是指被连接的列的值为空的数据。

#### 左外连接(LEFT OUTER JOIN)

![image-20211110203503877](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110203503877-16365477053415.png)

![image-20211110175929667](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110175929667-163653837089415.png)

**左外连接**

左边的表 (EMPLOYEES) 中即使没有与 DEPARTMENTS 表中匹配的行，该查询

也会取回 EMPLOYEES 表中所有的行。

示例：

查询所有雇员的名字以及他们的部门名称，包含那些没有部门的雇员。

```sql
select 
e.last_name,d.department_name 
from employees e LEFT OUTER JOIN departments d 
on e.dept_id = d.department_id;
```

#### 右外连接(RIGTH OUTER JOIN)

![image-20211110203632857](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110203632857-16365477935806.png)

![image-20211110211057102](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110211057102-163654985810716.png)

**右外连接**

右边的表 (DEPARTMENTS ) 中即使没有与 EMPLOYEES 表中匹配的行，该查询

也会取回 DEPARTMENTS 表中所有的行。

示例：

查询所有雇员的名字以及他们的部门名称，包含那些没有雇员的部门。

```sql
select 
e.last_name,d.department_name  
from  employees  e RIGHT  OUTER JOIN  departments  d 
on e.DEPARTMENT_ID = d.department_id;
```

**实时效果反馈**

**1**.**如下说法正确的是。**

A 左外连接会显示左表中的孤儿数据。

B 左外连接会显示右表中的孤儿数据。

C 左外连接会显示左右表中的孤儿数据。

D 左外连接不会显示表中的孤儿数据。

**答案**

1=>A

####  全外连接(FULL OUTER JOIN)

![image-20211110203750454](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211110203750454-16365478714667.png)

注意： MySQL 中不支持 FULL OUTER JOIN 连接

可以使用 union 实现全完连接。

- UNION: 可以将两个查询结果集合并，返回的行都是唯一的，如同对整个结果集合使用了 DISTINCT。
- UNION ALL: 只是简单的将两个结果合并后就返回。这样，如果返回的两个结果集中有重复的数据， 那么返回的结果集就会包含重复的数据了。

**语法结构**

```sql
(SELECT  投影列 FROM 表名 LEFT OUTER JOIN  表名 ON  连接条件) 
UNION 
(SELECT  投影列 FROM 表名 RIGHT OUTER JOIN  表名 ON  连接条件)
```

示例：

查询所有雇员的名字以及他们的部门名称，包含那些没有雇员的部门以及没有部门的雇 员。

```sql
(select e.last_name,d.department_name from employees e LEFT OUTER JOIN departments d  on  e.department_id =  d.department_id)  
UNION  
(select  e1.last_name,d1.department_name  from employees e1 RIGHT OUTER JOIN departments d1 on d1.department_id = e1.department_id)
```

**实时效果反馈**

**1**.**UNION的作用是：。**

A 合并结果集并不剔除重复数据

B 合并结果集并剔除重复数据

C 剔除重复数据

D 指定连接条件

**答案**

1=>B

## V、##多表查询练习

1.写一个查询显示所有雇员的 last name、department id、and department name。

```sql
SELECT
e.LAST_NAME,e.DEPARTMENT_ID,d.DEPARTMENT_NAME
FROM employees e,departments d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID;
```

2.创建一个在部门 80 中的所有工作岗位的唯一列表，在输出中包括部门的地点。

```sql
SELECT
e.JOB_ID,d.LOCATION_ID
FROM employees e,departments d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID
AND e.DEPARTMENT_ID = 80;
```

3.写一个查询显示所有有佣金的雇员的 last name、department name、location ID 和城

市

```sql
SELECT
e.LAST_NAME,d.DEPARTMENT_NAME,l.LOCATION_ID,l.CITY
FROM employees e,departments d,locations l
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID 
AND d.LOCATION_ID = l.LOCATION_ID
AND e.COMMISSION_PCT is NOT NULL;
```

4.显示所有在其 last names 中有一个小写 *a* 的雇员的 last name 和 department

name。

```sql
SELECT
e.LAST_NAME,d.DEPARTMENT_NAME
FROM employees e,departments d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID 
AND e.LAST_NAME LIKE '%a%';
```

5.用sql99的内连接写一个查询显示那些工作在 Toronto 的所有雇员的 last name、job、department number 和 department name。

```sql
SELECT
e.LAST_NAME,e.JOB_ID,e.DEPARTMENT_ID,d.DEPARTMENT_NAME
FROM employees e JOIN departments d ON e.DEPARTMENT_ID = d.DEPARTMENT_ID
JOIN locations l ON d.LOCATION_ID = l.LOCATION_ID
WHERE l.CITY = 'Toronto';
```

6.显示雇员的 last name 和 employee number 连同他们的经理的 last name 和manager number。列标签分别为 Employee、Emp#、Manager 和 Mgr#

```sql
SELECT
worker.LAST_NAME Employee,worker.DEPARTMENT_ID 'Emp#',manager.LAST_NAME Manager,manager.MANAGER_ID 'Mgr#'
FROM employees worker JOIN employees manager
ON worker.MANAGER_ID = manager.EMPLOYEE_ID;
```

# 五、 聚合函数

## I、聚合函数介绍

![image-20211112110228798](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112110228798-16366861499387.png)

**聚合函数**

聚合函数也称之为多行函数，组函数或分组函数。聚合函数不象单行函数，聚合函数对行的分组进行操作，对每组给出一个结果。如果在查询中没有指定分组，那么聚合函数则将查询到的结果集视为一组。

**聚合函数类型**

![image-20211112110410633](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112110410633-16366862514578.png)

聚合函数说明：

| 函数名            | 描述                                                   | 实例                                                         |
| :---------------- | :----------------------------------------------------- | :----------------------------------------------------------- |
| AVG(expression)   | 返回一个表达式的平均值，expression 是一个字段          | 返回 Products 表中Price 字段的平均值：`SELECT AVG(Price) AS AveragePrice FROM Products;` |
| COUNT(expression) | 返回查询的记录总数，expression 参数是一个字段或者 * 号 | 返回 Products 表中 products 字段总共有多少条记录：`SELECT COUNT(ProductID) AS NumberOfProducts FROM Products;` |
| MAX(expression)   | 返回字段 expression 中的最大值                         | 返回数据表 Products 中字段 Price 的最大值：`SELECT MAX(Price) AS LargestPrice FROM Products;` |
| MIN(expression)   | 返回字段 expression 中的最小值                         | 返回数据表 Products 中字段 Price 的最小值：`SELECT MIN(Price) AS MinPrice FROM Products;` |
| SUM(expression)   | 返回指定字段的总和                                     | 计算 OrderDetails 表中字段 Quantity 的总和：`SELECT SUM(Quantity) AS TotalItemsOrdered FROM OrderDetails;` |

**聚合函数使用方式**

![image-20211112110524939](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112110524939-16366863260569.png)

**使用聚合函数的原则**

- DISTINCT 使得函数只考虑不重复的值；
- 所有聚合函数忽略空值。为了用一个值代替空值，用 IFNULL 或 COALESCE 函数。

**实时效果反馈**

**1**.**聚合函数对行的进行操作，并给出结果。**

A 分组 多个。

B 分组 一个。

C 单条 多个。

D 单条 一个。

**答案**

1=>B

## II、AVG 和 SUM 函数

**AVG(arg)函数**

对分组数据做平均值运算。

arg:参数类型只能是数字类型。

**SUM(arg)函数**

对分组数据求和。

arg:参数类型只能是数字类型。

示例：

计算员工表中工作编号含有REP的工作岗位的平均薪水与薪水总和。

```sql
SELECT AVG(salary),SUM(salary)
FROM employees
WHERE job_id LIKE '%REP%';
```

**实时效果反馈**

**1**.**AVG函数是对分组数据求的运算。**

A 和

B 差

C 方差

D 平均值

**2**.**SUM函数是对分组数据求的运算。**

A 和

B 差

C 方差

D 平均值

**答案**

1=>D 2=>A

##   III、MIN 和 MAX 函数

**MIN(arg)函数**

求分组中最小数据。

arg:参数类型可以是字符、数字、 日期。

**MAX(arg)函数**

求分组中最大数据。

arg:参数类型可以是字符、数字、 日期。

示例：

查询员工表中入职时间最短与最长的员工，并显示他们的入职时间。

```sql
SELECT MIN(hire_date), MAX(hire_date) FROM employees;
```

**实时效果反馈**

**1**.**MIN函数是对分组数据求的运算。**

A 最小值

B 最大值

C 差值

D 平均值

**2**.**MAX函数是对分组数据求的运算。**

A 最小值

B 最大值

C 差值

D 平均值

**答案**

1=>A 2=>B

##  IV、**COUNT 函数**

返回分组中的总行数。

COUNT 函数有三种格式：

- COUNT(*)：返回表中满足 SELECT 语句的所有列的行数，包括重复行，包括有空值列

  的行。

- COUNT(expr)：返回在列中的由 *expr* 指定的非空值的数。

- COUNT(DISTINCT expr)：返回在列中的由 *expr* 指定的唯一的非空值的数。

**使用 DISTINCT 关键字**

- COUNT(DISTINCT expr) 返回对于表达式 *expr* 非空并且值不相同的行数
- 显示 EMPLOYEES 表中不同部门数的值

示例一：

**显示员工表中部门编号是80中有佣金的雇员人数。**

```sql
SELECT COUNT(commission_pct) FROM employees WHERE department_id = 80;
```

示例二：

**显示员工表中的部门数。**

```sql
SELECT COUNT(DISTINCT department_id) FROM employees;
```

**组函数和 Null 值**

在组函数中使用 IFNULL 函数

```sql
SELECT AVG(IFNULL(commission_pct, 0)) FROM employees;
```

**实时效果反馈**

**1**.**COUNT函数计算结果集中的。**

A 方差

B 标准差

C 均方差

D 总行数

**答案**

1=>D

##  V、**数据分组(GROUP BY)**

### 创建数据组

![image-20211112100427550](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112100427550-16366826686792.png)

**创建数据组**

在没有进行数据分组之前，所有聚合函数是将结果集作为一个大的信息组进行处理。但是，有时，则需要将表的信息划分为较小的组，可以用 GROUP BY 子句实现。

**GROUP BY 子句语法**

![image-20211112102132899](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112102132899-16366836937593.png)

**原则**

- 使用 WHERE 子句，可以在划分行成组以前过滤行。
- 如果有WHERE子句，那么GROUP BY 子句必须在WHERE的子句后面。
- 在 GROUP BY 子句中必须包含列。

**使用 GROUP BY 子句**

![image-20211112102330818](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112102330818-16366838116954.png)

**GROUP BY 子句**

下面是包含一个 GROUP BY 子句 SELECT 语句的求值过程：

- SELECT 子句指定要返回的列：

- 在 EMPLOYEES 表中的部门号

  − GROUP BY 子句中指定分组的所有薪水的平均值

  − FROM 子句指定数据库必须访问的表：EMPLOYEES 表。

- WHERE 子句指定被返回的行。因为无 WHERE 子句默认情况下所有行被返回。

- GROUP BY 子句指定行怎样被分组。行用部门号分组，所以 AVG 函数被应用于薪水列，以计算每个部门的平均薪水。

示例：

计算每个部门的员工总数。

```sql
SELECT DEPARTMENT_ID, COUNT(*) FROM employees GROUP BY DEPARTMENT_ID;
```

**实时效果反馈**

**1**.**GROUP BY 是创建的子句。**

A 数据组。

B 查询。

C 条件。

D 连接。

**答案**

1=>A

## VI、 在多列上使用分组

![image-20211112103754162](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112103754162-16366846750486.png)

**在组中分组**

可以列出多个 GROUP BY 列返回组和子组的摘要结果。可以用 GROUP BY子句中的列的顺序确定结果的默认排序顺序。下面是图片中的 SELECT 语句中包含一个 GROUP BY 子句时的求值过程：

- SELECT 子句指定被返回的列：

  − 部门号在 EMPLOYEES 表中

  − Job ID 在 EMPLOYEES 表中

  − 在 GROUP BY 子句中指定的组中所有薪水的合计

- FROM 子句指定数据库必须访问的表：EMPLOYEES 表。

- GROUP BY 子句指定你怎样分组行：

  − 首先，用部门号分组行。

  − 第二，在部门号的分组中再用 job ID 分组行。

如此 SUM 函数被用于每个部门号分组中的所有 job ID 的 salary 列。

示例：

计算每个部门的不同工作岗位的员工总数。

```sql
SELECT 
e.DEPARTMENT_ID, e.JOB_ID,COUNT(*)
FROM employees e
GROUP BY e.DEPARTMENT_ID,e.JOB_ID;
```

**实时效果反馈**

**1**.**如下说法正确的是。**

A GROUP BY 子句可以连接多表。

B GROUP BY 子句可以给定多条件。

C GROUP BY 子句可以对多列进行分组。

D GROUP BY 子句可以出现在WHERE子句的前面。

**答案**

1=>C

##  VII、**约束分组结果(HAVING)**

![image-20211112202500534](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112202500534-16367199015521.png)

**HAVING** **子句**

HAVING 子句是对查询出结果集分组后的结果进行过滤。

**约束分组结果**

用 WHERE 子句约束选择的行，用 HAVING 子句约束组。为了找到每个部门中的最高薪水，而且只显示最高薪水大于 $10,000 的那些部门，可以象下面这样做：

1. 用部门号分组，在每个部门中找最大薪水。
2. 返回那些有最高薪水大于 $10,000 的雇员的部门

```sql
SELECT 
department_id, MAX(salary) 
FROM employees 
GROUP BY department_id 
HAVING MAX(salary) > 10000 ;
```

**HAVING子句语法**

![image-20211112202826331](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112202826331-16367201074572.png)

示例：

显示那些合计薪水超过 13,000 的每个工作岗位的合计薪水。排除那些JOB_ID中含有REP的工作岗位，并且用合计月薪排序列表。

```sql
SELECT
e.JOB_ID,e.SALARY,SUM(SALARY)
FROM employees e
WHERE e.JOB_ID not LIKE '%REP%'
GROUP BY e.JOB_ID
HAVING SUM(SALARY) > 13000
ORDER BY SUM(SALARY);
```

**实时效果反馈**

**1**.**HAVING 子句是。**

A 对数据分组

B 对分组后的结果进行过滤

C 行选择的条件给定

D 给定连接条件

**答案**

1=>B

## VIII、&&&聚合函数练习

1.显示所有雇员的最高、最低、合计和平均薪水，列标签分别为：Max、Min、Sum 和 Avg。四舍五入结果为最近的整数。

```sql
SELECT
ROUND(MAX(SALARY)) Max,ROUND(MIN(SALARY)) Min,
ROUND(SUM(SALARY)) Sum,ROUND(AVG(SALARY)) Avg
FROM employees;
```

2.写一个查询显示每一工作岗位的人数。

```sql
SELECT
JOB_ID,COUNT(*)
FROM employees
GROUP BY JOB_ID;
```

3.确定经理人数，不需要列出他们，列标签是 Number of Managers。提示：用MANAGER_ID列决定经理号。

```sql
SELECT
COUNT( DISTINCT MANAGER_ID) 'Number of Managers'
FROM employees
```

4.写一个查询显示最高和最低薪水之间的差。

```sql
SELECT
MAX(SALARY),min(Salary),(max(salary)-min(salary)) 'cha'
FROM employees
```

5.显示经理号和经理付给雇员的最低薪水。排除那些经理未知的人。排除最低薪水小于等于 $6,000 的组。按薪水降序排序输出。

```sql
SELECT
e.MANAGER_ID,MIN(e.SALARY)
FROM employees e
WHERE e.MANAGER_ID is not NULL
GROUP BY e.MANAGER_ID
HAVING MIN(e.SALARY) > 6000
ORDER BY e.SALARY DESC;
```

6.写一个查询显示每个部门的名字、地点、人数和部门中所有雇员的平均薪水。四舍五入薪水到两位小数。

```sql
SELECT
d.DEPARTMENT_NAME,d.LOCATION_ID,COUNT(*),ROUND(AVG(e.SALARY),2)
FROM employees e,departments d
WHERE e.DEPARTMENT_ID = d.DEPARTMENT_ID
GROUP BY d.DEPARTMENT_NAME,d.LOCATION_ID
```

#  六、子查询

## I、子查询介绍

![image-20211112210000161](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112210000161-16367220011936.png)

**用子查询解决问题**

假如要写一个查询来找出挣钱比 Abel 的薪水还多的人。为了解决这个问题，需要两个查询：一个找出 Abel 的收入，第二个查询找出收入高于 Abel 的人。可以用组合两个查询的方法解决这个问题。内查询或子查询返回一个值给外查询或主查询。使用一个子查询相当于执行两个连续查询并且用第一个查询的结果作为第二个查询的搜索值。

**子查询语法**

![image-20211112205903977](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112205903977-16367219449945.png)

**子查询**

子查询是一个 SELECT 语句，它是嵌在另一个 SELECT 语句中的子句。使用子查询可以用简单的语句构建功能强大的语句。

可以将子查询放在许多的 SQL 子句中，包括：

- WHERE 子句
- HAVING 子句
- FROM 子句

**使用子查询**

![image-20211112210214999](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112210214999-16367221359867.png)

**使用子查询的原则**

- 子查询放在圆括号中。
- 将子查询放在比较条件的右边。
- 在单行子查询中用单行运算符，在多行子查询中用多行运算符。

**子查询类型**

![image-20211112210400074](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112210400074-16367222411588.png)

示例：

查询与Fox同一部门的同事，并显示他们的名字与部门ID。

```sql
SELECT 
e.LAST_NAME,e.DEPARTMENT_ID
FROM employees e
WHERE e.DEPARTMENT_ID = (
SELECT
e1.DEPARTMENT_ID
FROM employees e1
WHERE e1.LAST_NAME = 'fox' 
);
```

**实时效果反馈**

**1**.**子查询需要放在中。**

A 圆括号

B 大括号

C 中括号

D 书名号

**答案**

1=>A

##  II、**单行子查询**

![image-20211112210526080](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211112210526080-16367223270579.png)

**单行子查询**

单行子查询是从内查询返回一行的查询。在该子查询类型中用一个单行操作符。

示例：

查询 Fox的同事，但是不包含他自己。

```sql
SELECT
e.LAST_NAME
FROM employees e
WHERE e.DEPARTMENT_ID = (
SELECT
e1.DEPARTMENT_ID
FROM employees e1
WHERE e1.LAST_NAME = 'fox'
) AND e.LAST_NAME <> 'fox';
```

**实时效果反馈**

**1**.**单行子查询是从内查询返回的查询。**

A 空数据

B 多行数据

C 多个列数据

D 一行数据

**答案**

1=>D

##  III、**多行子查询**

![image-20211113195634870](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211113195634870-16368045959402.png)

**多行子查询**

子查询返回多行被称为多行子查询。对多行子查询要使用多行运算符而不是单行运

算符。

**使用ANY运算符**

![image-20211113195733708](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211113195733708-16368046547743.png)

**ANY 运算符**

ANY 运算符比较一个值与一个子查询返回的任意一个值。

- < ANY 意思是小于最大值。
- \> ANY 意思是大于最小值。
- = ANY 等同于 IN。

**使用ALL运算符**

![image-20211113200148446](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211113200148446-16368049094134.png)

ALL 运算符比较一个值与子查询返回的全部值。

- < ALL 意思是小于最小值。
- \> ALL 意思是大于最大值，

NOT 运算符可以与 IN运算符一起使用。

**子查询中的空值**

![image-20211113200646356](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211113200646356-16368052073025.png)

内查询返回的值含有空值，并因此整个查询无返回行，原因是用大于、小于或不等于比较Null值，都返回null。所以，只要空值可能是子查询结果集的一部分，就不能用 NOT IN 运算符。NOT IN 运算符相当于 <> ALL。

注意，空值作为一个子查询结果集的一部分，如果使用 IN 操作符的话，不是一个问题。IN 操作符相当于 =ANY。

```sql
SELECT 
emp.last_name
FROM employees emp 
WHERE emp.employee_id IN (
    SELECT mgr.manager_id 
    FROM employees mgr);
```

示例:

查找各部门收入为部门最低的那些雇员。显示他们的名字，薪水以及部门 ID。

```sql
SELECT
e.LAST_NAME,e.SALARY,e.DEPARTMENT_ID 
FROM employees e
WHERE e.SALARY in ( 
	SELECT
	MIN(e1.SALARY)
	FROM employees e1
	GROUP BY e1.DEPARTMENT_ID
) GROUP BY e.DEPARTMENT_ID;
```

**实时效果反馈**

**1**.**对多行子查询要使用比较符。**

A =、>、ALL

B IN、ANY、ALL

C IN、<>、ALL

D IN、ANY、<>

**答案**

1=>B

##  IV、子查询练习

1.写一个查询显示与 Zlotkey 在同一部门的雇员的 last name 和 hire date，结果中不包括 Zlotkey。

```sql
SELECT
e.LAST_NAME,e.HIRE_DATE
FROM employees e
WHERE e.DEPARTMENT_ID = (
	SELECT
	e1.DEPARTMENT_ID
	FROM employees e1
	WHERE e1.LAST_NAME = 'zlotkey') 
AND e.LAST_NAME <> 'zlotkey';
```

2.创建一个查询显示所有其薪水高于平均薪水的雇员的雇员号和名字。按薪水的升序排序。

```sql
SELECT
e.EMPLOYEE_ID,e.LAST_NAME,e.SALARY
FROM employees e
WHERE e.SALARY > (
	SELECT 
	AVG(e1.SALARY)
	FROM employees e1)
ORDER BY e.SALARY ASC;
```

3.写一个查询显示所有工作在有任一雇员的名字中包含一个 *u* 的部门的雇员的雇员号和名字。

```sql
SELECT
e.EMPLOYEE_ID,e.LAST_NAME
FROM employees e
WHERE e.LAST_NAME IN (
	SELECT
	e1.LAST_NAME
	FROM employees e1
	WHERE e1.LAST_NAME LIKE '%u%');
```

4.显示所有部门地点号 (department location ID ) 是 1700 的雇员的 last name、department number 和 job ID。

```sql
SELECT
e.LAST_NAME,e.DEPARTMENT_ID,e.JOB_ID
FROM employees e
WHERE e.DEPARTMENT_ID in (
	SELECT 
	d1.DEPARTMENT_ID
	FROM departments d1
	WHERE d1.LOCATION_ID = 1700 );
```

5.显示每个向 King 报告的雇员的名字和薪水。

```sql
## king是经理，雇员号为100，显示所有经理号为100的雇员名字和薪水
SELECT
e.LAST_NAME,e.SALARY
FROM employees e
WHERE e.MANAGER_ID in (
	SELECT
	e1.MANAGER_ID
	FROM employees e1
	WHERE e1.MANAGER_ID = 100);  ## 也可以根据标题，这样 WHERE e.LAST_NAME = 'King'
```

6.显示在 Executive 部门的每个雇员的 department number、last name 和 job ID。

```sql
SELECT 
e.DEPARTMENT_ID,e.LAST_NAME,e.JOB_ID
FROM employees e
WHERE e.DEPARTMENT_ID = (
	SELECT
	d.DEPARTMENT_ID
	FROM departments d
	WHERE d.DEPARTMENT_NAME = 'Executive');
```

# 七、 MySQL中的索引

![image-20211114133355831](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211114133355831-16368680367274.png)

## I、**索引介绍**

索引是对数据库表中的一列或多列值进行排序的一种结构，使用索引可以快速访问数据库表中的特定信息。索引是一种特殊的文件，它们包含着对数据表里所有记录的位置信息。更通俗的说，数据库索引好比是一本书前面的目录，能加快数据库的查询速度。MySQL 索引的建立对于MySQL 的高效运行是很重要的，索引可以大大提高 MySQL 的检索速度。

**索引的作用**

索引相当于图书上的目录，可以根据目录上的页码快速找到所需的内容，提高性能（查询速度）。

**索引优点：**

1. 通过创建唯一性索引，可以保证数据库表中的每一行数据的唯一性；
2. 可以加快数据的检索速度；
3. 可以加速表与表之间的连接；
4. 在使用分组和排序进行检索的时候，可以减少查询中分组和排序的时间；

**索引缺点**

1. 创建索引和维护索引要耗费时间，这种时间随着数据量的增加而增加；
2. 索引需要占用物理空间，数据量越大，占用空间越大；
3. 会降低表的增删改的效率，因为每次增删改索引都需要进行动态维护；

**什么时候需要创建索引**

1. 频繁作为查询条件的字段应该创建索引；
2. 查询中排序的字段创建索引将大大提高排序的速度（索引就是排序加快速查找）；
3. 查询中统计或者分组的字段；

**什么时候不需要创建索引**

1. 频繁更新的字段不适合创建索引，因为每次更新不单单是更新记录，还会更新索引，保存索引文件；
2. where条件里用不到的字段，不创建索引；
3. 表记录太少，不需要创建索引；
4. 经常增删改的表；
5. 数据重复且分布平均的字段，因此为经常查询的和经常排序的字段建立索引。注意某些数据包含大量重复数据，因此他建立索引就没有太大的效果，例如性别字段，只有男女，不适合建立索引；

**MySQL中的索引类型**

- 普通索引：

  最基本的索引，它没有任何限制。

- 唯一索引：

  索引列的值必须唯一，但允许有空值，如果是组合索引，则列值的组合必须唯一。

- 主键索引：

  特殊的索引，唯一的标识一条记录，不能为空，一般用primary key来约束。

- 联合索引：

  在多个字段上建立索引，能够加速查询到速度。

**实时效果反馈**

**1**.**索引的作用是为了提高速度。**

A 添加数据

B 修改数据

C 更新数据

D 查询数据

**答案**

1=>D

##  II、**普通索引**

是最基本的索引，它没有任何限制。在创建索引时，可以指定索引长度。length 为可选参数，表示索引的长度，只有字符串类型的字段才能指定索引长度，如果是 BLOB 和 TEXT 类型，必须指定 length。

> 创建索引时需要注意：
>
> ------
>
> 如果指定单列索引长度，length 必须小于这个字段所允许的最大字符个数。

#### 查询索引

```sql
SHOW INDEX FROM table_name;
```

#### 直接创建索引

```sql
CREATE INDEX index_name ON table(column(length));
```

示例：

为 emp3 表中的 name 创建一个索引，索引名为 emp3_name_index；

```sql
create index emp3_name_index ON emp3(name);
```

#### **修改表添加索引**

```sql
ALTER TABLE table_name ADD INDEX index_name (column(length));s
```

示例：

修改 emp3 表，为 addrees 列添加索引，索引名为 emp3_address_index；

```sql
alter table emp3 add index emp3_address_index(address);
```

#### **创建表时指定索引列**

```sql
CREATE TABLE `table` (
COLUMN TYPE ,
PRIMARY KEY (`id`),
INDEX index_name (column(length))
);
```

示例：

创建 emp4 表，包含 emp_id,name,address 列， 同时为 name 列创建索引 ，索引名为 emp4_name_index。

```sql
create  table  emp4(emp_id  int  primary  key auto_increment,name  varchar(30),address varchar(50),index emp4_name_index(name));
```

#### **删除索引**

```sql
DROP INDEX indexname ON tablename;
```

示例：

删除 mep3 表中索引名为 emp3_address_index 的索引。

```sql
drop index emp3_address_index on emp3;
```

**实时效果反馈**

**1**.**如果指定单列索引长度，length 必须这个字段所允许的最大字符个数。**

A 小于

B 大于

C 等于

D 不等于

**2**.**直接创建索引：CREATE index_name ON table(column(length));。**

A INDEXS

B TABLE

C COLUMN

D INDEX

**答案**

1=>A 2=>D

##  III、**唯一索引**

唯一索引与普通索引类似，不同的就是： 索引列的值必须唯一，但允许有空值。

#### **创建唯一索引**

```sql
CREATE UNIQUE INDEX indexName ON table(column(length));
```

示例：

为 emp 表中的 name 创建一个唯一索引，索引名为 emp_name_index。

```sql
create unique index emp_name_index on emp(name);
```

#### **修改表添加唯一索引**

```sql
ALTER TABLE table_name ADD UNIQUE indexName (column(length));
```

示例：

修改 emp 表，为 salary 列添加唯一索引，索引名为 emp_salary_index。

```sql
alter table emp add unique emp_salary_index(salary);
```

#### **创建表时指定唯一索引**

```sql
CREATE TABLE `table` (
COLUMN TYPE ,
PRIMARY KEY (`id`),
UNIQUE index_name (column(length))
);
```

示例：

创建 emp5 表，包含 emp_id,name,address 列，同时为 name 列创建唯一索引。索引名为 emp5_name_index。

```sql
CREATE TABLE emp5(emp_id int PRIMARY KEY auto_increment,
NAME VARCHAR(30),
address VARCHAR(50),
UNIQUE INDEX emp5_name_index(NAME));
```

**实时效果反馈**

**1**.**唯一索引列的值，有空值。**

A 允许不唯一 允许

B 必须唯一 允许

C 必须唯一 不允许

D 允许不唯一 不允许

**2**.**创建唯一索引：CREATEindexName ON table(column(length));**

A UNIQUE

B INDEX

C UNIQUE INDEXS

D UNIQUE INDEX

**答案**

1=>B 2=>D

##  IV、**主键索引**

主键索引是一种特殊的唯一索引，一个表只能有一个主键，不允许有空值。一般是在建表的时候同时创建主键索引。

#### **修改表添加主键索引**

```sql
ALTER TABLE  表名 ADD PRIMARY KEY(列名);
```

示例：

修改 emp 表为 employee_id 添加主键索引。

```sql
alter table emp add primary key(employee_id);
```

#### **创建表时指定主键索引**

```sql
CREATE TABLE `table` (
COLUMN TYPE ,
PRIMARY KEY(column)
);
```

示例：

创建 emp6 表，包含 emp_id,name,address 列，同时为 emp_id 列创建主键索引。

```sql
create table emp6(employee_id int primary key auto_increment,name varchar(20),address varchar(50));
```

**实时效果反馈**

**1**.**主键索引列的值，有空值。**

A 允许不唯一 允许

B 必须唯一 允许

C 必须唯一 不允许

D 允许不唯一 不允许

**答案**

1=>C

# 八、 MySQL事务

## I、事务简介

事务是指作为单个逻辑工作单元执行的一系列操作，要么完全地执行，要么完全地不执行。

事务定义(Transaction)

- 事务是一个最小的不可再分的工作单元；通常一个事务对应一个完整的业务(例如银行账户转账业务，该业务就是一个最小的工作单元)
- 一个完整的业务需要批量的DML(insert、update、delete)语句共同联合完成
- 事务只和DML语句有关，或者说DML语句才有事务。这个和业务逻辑有关，业务逻辑不同，DML语句的个数不同

**事务四大特征(ACID)**

- **原子性(ATOMICITY)**

  事务中的操作要么都不做，要么就全做。

- **一致性(CONSISTENCY)**

  一个事务应该保护所有定义在数据上的不变的属性(例如完整性约束)。在完成了一个成功的事务时，数据应处于一致的状态。

- **隔离性(ISOLATION)**

  一个事务的执行不能被其他事务干扰。

- **持久性(DURABILITY)**

  一个事务一旦提交，它对数据库中数据的改变就应该是永久性的。

**事务类型**

- **显式事务**

  需要我们手动的提交或回滚。

  DML 语言中的所有操作都是显示事务操作。

- **隐式事务**

  数据库自动提交不需要我们做任何处理，同时也不具备回滚性。DDL、DCL 语言都是隐式事务操作

**实时效果反馈**

**1**.**如下描述事务四大特征正确的是。**

A 原子性、可读性、隔离性、持久性

B 可读性、一致性、隔离性、持久性

C 可读性、一致性、可写性、持久性

D 原子性、一致性、隔离性、持久性

**答案**

1=>D

##  II、使用事务

| TCL语句           | 描述     |
| ----------------- | -------- |
| start transaction | 事务开启 |
| commit            | 事物提交 |
| rollback          | 事物回滚 |

示例一：

创建account账户表，包含id、卡号、用户名、余额。

```sql
create table account(
id int primary key auto_increment,
cardnum varchar(20) not null,
username varchar(30) not null,
balance double(10,2)
);
```

示例二：

向account表中插入两条数据。

```sql
insert into account(cardnum,username,balance) 
VALUES('123456789','张三',2000);
insert into account(cardnum,username,balance) 
VALUES('987654321','李四',2000);
```

示例三：

在一个事务中完成转账业务。

```sql
START TRANSACTION
update account set balance = balance-200 where cardnum = '123456789';
update account set balance = balance+200 where cardnum = '987654321';
select * from account;
-- 当我们关闭数据库重新打开后，张三和李四的账户余额并没发生任何变化。  
-- 这是因为当我们使用“START TRANSACTION”开启一个事务后，该事务的提交方式不再是自动的，  
-- 而是需要手动提交，而在这里，我们并没有使用事务提交语句COMMIT，  
-- 所以对account表中数据的修改并没有永久的保存到数据库中，也就是说我们的转账事务并没有执行成功  


-- 提交转账事务  
commit;


-- 事务的回滚让数据库恢复到了执行事务操作前的状态。  
-- 需要注意的是事务的回滚必须在事务提交之前，因为事务一旦提交就不能再进行回滚操作。
rollback;


```

## III、事务的并发问题

**脏读（读取未提交数据）**

指一个事务读取了另外一个事务未提交的数据。

A事务读取B事务尚未提交的数据，此时如果B事务发生错误并执行回滚操作，那么A事务读取到的数据就是脏数据。

![1](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/1.png)

**不可重复读（前后多次读取，数据内容不一致）**

在一个事务内读取表中的某一行数据，多次读取结果不同。

事务A在执行读取操作，由整个事务A比较大，前后读取同一条数据需要经历很长的时间 。而在事务A第一次读取数据，比如此时读取了小明的年龄为20岁，事务B执行更改操作，将小明的年龄更改为30岁，此时事务A第二次读取到小明的年龄时，发现其年龄是30岁，和之前的数据不一样了，也就是数据不重复了，系统不可以读取到重复的数据，成为不可重复读。

![2](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/2.png)

**幻读（前后多次读取，数据总量不一致）**

是指在一个事务内读取到了别的事务插入的数据，导致前后读取数量总量不一致。

事务A在执行读取操作，需要两次统计数据的总量，前一次查询数据总量后，此时事务B执行了新增数据的操作并提交后，这个时候事务A读取的数据总量和之前统计的不一样，就像产生了幻觉一样，平白无故的多了几条数据，成为幻读。

![3](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/3.png)

### 事务的隔离级别

事务的隔离级别用于决定如何控制并发用户读写数据的操作。数据库是允许多用户并发访问的，如果多个用户同时开启事务并对同一数据进行读写操作的话，有可能会出现脏读、不可重复读和幻读问题，所以MySQL中提供了四种隔离级别来解决上述问题。

事务的隔离级别从低到高依次为：

- READ UNCOMMITTED
- READ COMMITTED
- REPEATABLE READ
- SERIALIZABLE

隔离级别越低，越能支持高并发的数据库操作。

![image-20211115113901465](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211115113901465-16369475426591.png)

**查看MySQL默认事务隔离级别**

```sql
SELECT @@transaction_isolation;
```

**设置事务隔离级别**

对当前session有效。

```sql
set session transaction isolation level read uncommitted;
set session transaction isolation level read committed;
set session transaction isolation level repeatable read;
set session transaction isolation level serializable;
```

**实时效果反馈**

**1**.**MySQL默认事务隔离级别是。**

A uncommitted

B committed

C repeatable read

D serializable

**答案**

1=>C

#  九、MySQL的用户管理

MySQL 是一个多用户的数据库系统，按权限，用户可以分为两种： root 用户，超级管理员，和由 root 用户创建的普通用户。

### 用户管理

**创建用户**

```
1
CREATE USER username IDENTIFIED BY 'password';
```

**查看用户**

```
1
SELECT USER,HOST FROM mysql.user;
```

示例：

创建一个 u_sxt 的用户，并查看创建是否成功。

```
1
create user u_sxt IDENTIFIED by 'sxt';
2
select user,host from mysql.user;
```

### **权限管理**

新用户创建完后是无法登陆的，需要分配权限。 GRANT 权限 ON 数据库.表 TO 用户名@登录主机 IDENTIFIED BY "密码"

**登陆主机：**

| **字段**  | **含义**                                                 |
| --------- | -------------------------------------------------------- |
| %         | 匹配所有主机                                             |
| localhost | localhost 不会被解析成 IP 地址，直接通过 UNIXsocket 连接 |
| 127.0.0.1 | 会通过 TCP/IP 协议连接，并且只能在本机访问               |
| :: 1      | ::1 就是兼容支持 ipv6 的，表示同 ipv4 的 127.0.0. 1      |

**权限列表**

| **权 限**               | **作用范围**         | **作 用**                     |
| ----------------------- | -------------------- | ----------------------------- |
| all [privileges]        | 服务器               | 所有权限                      |
| select                  | 表、列               | 选择行                        |
| insert                  | 表、列               | 插入行                        |
| update                  | 表、列               | 更新行                        |
| delete                  | 表                   | 删除行                        |
| create                  | 数据库、表、索引     | 创建                          |
| drop                    | 数据库、表、视图     | 删除                          |
| reload                  | 服务器               | 允许使用flush语句             |
| shutdown                | 服务器               | 关闭服务                      |
| process                 | 服务器               | 查看线程信息                  |
| file                    | 服务器               | 文件操作                      |
| grant option            | 数据库、表、存储过程 | 授权                          |
| references              | 数据库、表           | 外键约束的父表                |
| index                   | 表                   | 创建/删除索引                 |
| alter                   | 表                   | 修改表结构                    |
| show databases          | 服务器               | 查看数据库名称                |
| super                   | 服务器               | 超级权限                      |
| create temporary tables | 表                   | 创建临时表                    |
| lock tables             | 数据库               | 锁表                          |
| execute                 | 存储过程             | 执行                          |
| replication client      | 服务器               | 允许查看主/从/二进制日志状态  |
| replication slave       | 服务器               | 主从复制                      |
| create view             | 视图                 | 创建视图                      |
| show view               | 视图                 | 查看视图                      |
| create routine          | 存储过程             | 创建存储过程                  |
| alter routine           | 存储过程             | 修改/删除存储过程             |
| create user             | 服务器               | 创建用户                      |
| event                   | 数据库               | 创建/更改/删除/查看事件       |
| trigger                 | 表                   | 触发器                        |
| create tablespace       | 服务器               | 创建/更改/删除表空间/日志文件 |
| proxy                   | 服务器               | 代理成为其它用户              |
| usage                   | 服务器               | 没有权限                      |

```sql
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password'
```

示例：

为 u_sxt 用户分配只能查询 bjsxt 库中的 emp 表，并且只能在本机登陆的权限。

```sql
grant select ON bjsxt.emp to 'u_sxt'@'localhost' IDENTIFIED by 'sxt';
```

**刷新权限**

每当调整权限后，通常需要执行以下语句刷新权限。

```sql
FLUSH PRIVILEGES;
```

**删除用户**

```sql
DROP USER username@localhost;
```

示例：

删除 u_sxt 用户。

```sql
drop user 'u_sxt'@'localhost';
```

**实时效果反馈**

**1**.**创建用户语句：CREATE username 'password';**

A USERS IDENTIFIED BY

B USER IDENTIFIED

C USER IDENTIFIED BY

D USER BY

**2**.**删除用户语句： username@localhost;**

A DELETE USER

B DELETE USERS

C DROP USERS

D DROP USER

**答案**

1=>C 2=>D

# 十、MySQL分页查询

![image-20211117162015573](https://www.itbaizhan.com/wiki/imgs/Mysql/Mysql/image-20211117162015573-16371372165874.png)

**MySQL 分页查询原则：**

- 在 MySQL 数据库中使用 LIMIT 子句进行分页查询。
- MySQL 分页中开始位置为 0。
- 分页子句在查询语句的最后侧。

### **LIMIT子句**

```sql
SELECT  投影列 FROM  表名 WHERE  条件 ORDER BY LIMIT  开始位置，查询数量;
```

示例：

查询雇员表中所有数据按 id 排序，实现分页查询，每次返回两条结果。

```sql
select * from employees order by employees_id limit 0,2;
```

### **LIMIT OFFSET子句**

```sql
SELECT  投影列 FROM  表名 WHERE  条件 ORDER BY LIMIT  查询数量 OFFSET 开始位置;
```

示例：

查询雇员表中所有数据按 id 排序，使用 LIMIT OFFSET 实现分页查询，每次返回两条结果。

```sql
select * from employees order by employees_id limit 2 offset 4;
```

**实时效果反馈**

**1**.**MySQL 分页中开始位置为。**

A -1

B 0

C 1

D 10

**2**.**分页子句在查询语句的。**

A 最前侧

B 任意位置

C 最后侧

D select子句后侧

**答案**

1=>B 2=>C

# 十一、数据库范式

## I、数据库范式简介

![image-20220217155945247](https://www.itbaizhan.com/wiki/imgs/image-20220217155945247-16450847862313.png)

**什么是范式（NF = NormalForm）**

- 范式是符合某一种设计要求的总结

**在数据库中表的设计，必须保证其合理性**

- 数据库表的设计关系整个系统的架构，关系到后续的开发效率和运行效率

**如何设计合理的数据库表**

- 结构合理
- 冗余数据少
- 尽量避免插入删除修改异常
- 遵循一定的规则，在关系型数据库中这种规则就称为范式

**关系型数据库有六种常见范式：**

- 第一范式（1NF）
- 第二范式（2NF）
- 第三范式（3NF）
- 巴斯-科德范式（BCNF）
- 第四范式（4NF）
- 第五范式（5NF）

**各个范式是依次嵌套包含的：**

在第一范式的基础上进一步满足更多规范要求的称为第二范式（2NF），其余范式以此类推。

![image-20211215142204632](https://www.itbaizhan.com/wiki/imgs/%E8%8C%83%E5%BC%8F%E5%B5%8C%E5%A5%97.png)

范式越高，设计质量越高，在现实设计中也越难实现

一般数据库设计，达到**第三范式**就足够了

**数据库范式中的概念**

元组：可以理解为一张表中的每条记录，也就是每一行数据。

属性：可以看作是“表的一列”。

- 主属性：

  在一个关系中，如一个属性是构成某一个候选关键字的属性集中的一个属性，则称它为主属性。

  例如：在关系——学生（学号，姓名，年龄，性别，班级）中，主属性是“学号”，那么其他的“姓名”、“年龄”、“性别”、“班级”就都可以称为非主属性。

- 非主属性：

不包含在候选码中的属性称为非主属性，相对于主属性来定义的。

**实时效果反馈**

**1. 什么是数据库范式？**

A 是关系型数据库表的设计规则。

B 是关系型数据库中对象的使用规则

C 是关系型数据库中内存分配规则

D 是数据文件定义的规则

**答案**

1=>A  

## II、第一范式（1NF）

![image-20211215152331899](https://www.itbaizhan.com/wiki/imgs/image-20211215152331899.png)

- 最基本的范式，是其他范式的基础

- 数据库表每列都是不可分割的基本数据项，同一列中不能有多个值，

  确保每列保持原子性

![image-20220216152629454](https://www.itbaizhan.com/wiki/imgs/image-20220216152629454-16449963910593.png)

**根据第一范式设计表**

![image-20220216152558060](https://www.itbaizhan.com/wiki/imgs/image-20220216152558060-16449963593072.png)

**第一范式存在的问题**

1. 数据冗余

   ![image-20220216153359441](https://www.itbaizhan.com/wiki/imgs/image-20220216153359441-16449968407417.png)

2. 插入数据异常

   ![image-20220216153806709](https://www.itbaizhan.com/wiki/imgs/image-20220216153806709-16449970882138.png)

3. 修改数据复杂

   ![image-20220216154059101](https://www.itbaizhan.com/wiki/imgs/image-20220216154059101-16449972602689.png)

4. 删除异常

   ![image-20220216154404951](https://www.itbaizhan.com/wiki/imgs/image-20220216154404951-164499744627611.png)

**实时效果反馈**

**1. 第一范式要求确保每列保持**

A 结构性

B 松散性

C 原子性

D 状态性

**答案**

1=>C

## III、第二范式（2NF）

![image-20211215182142698](https://www.itbaizhan.com/wiki/imgs/2NF1.png)

第二范式在第一范式的基础之上更进一层。第二范式需要确保数据库表中的每一列都和主键相关，而不能只与主键的某一部分相关（主要针对联合主键而言）。也就是说在一个数据库表中，一个表中只能保存一种数据，不可以把多种数据保存在同一张数据库表中。

![image-20220217145139611](https://www.itbaizhan.com/wiki/imgs/image-20220217145139611-16450807008895.png)

![image-20220217145317822](https://www.itbaizhan.com/wiki/imgs/image-20220217145317822-16450807989606.png)

![image-20220217145359925](https://www.itbaizhan.com/wiki/imgs/image-20220217145359925-16450808412177.png)

**根据第二范式设计表**

![image-20220216180700538](https://www.itbaizhan.com/wiki/imgs/image-20220216180700538-164500602176813.png)

**第二范式存在问题**

1. 插入异常

   ![image-20220217092851272](https://www.itbaizhan.com/wiki/imgs/image-20220217092851272-16450613324811.png)

2. 删除异常

![image-20220217093046235](https://www.itbaizhan.com/wiki/imgs/image-20220217093046235-16450614474642.png)

**实时效果反馈**

**1.第二范式需要确保数据库表中的每一列都和___相关：**

A 主属性

B 非主属性

**答案**

1=>A

## IV、第三范式（3NF）

![image-20211215191316125](https://www.itbaizhan.com/wiki/imgs/3NF1.png)

- 必须满足第二范式
- 确保数据表中的每一列数据都和**主键直接相关**，而不能间接相关

![image-20220218101753963](https://www.itbaizhan.com/wiki/imgs/image-20220218101753963-16451506750941.png)

![image-20220217141210808](https://www.itbaizhan.com/wiki/imgs/image-20220217141210808-16450783319783.png)

**根据第三范式设计表**

![image-20220217141943982](https://www.itbaizhan.com/wiki/imgs/image-20220217141943982-16450787850804.png)

符合3NF要求的数据库设计，基本上解决了数据冗余过大，插入异常，修改异常，删除异常的问题。

**实时效果反馈**

**1.第三范式需要确保数据库表中的每一列都和主属性___**

A 间接相关

B 直接相关

C 不相关

D 部分相关

**答案**

1=>B

## V、数据库设计范式总结

![image-20211215205856502](https://www.itbaizhan.com/wiki/imgs/%E6%80%BB%E7%BB%93.png)

数据库设计范式**优点**：

- 结构合理
- 冗余较小
- 尽量避免插入删除修改异常

数据库设计范式**缺点**：

- 性能降低，多表查询比单表查询速度慢

在实际设计中，要整体遵循范式理论

如果在某些特定的情况下还死死遵循范式也是不可取的，

因为可能降低数据库的效率，此时可以适当增加冗余而提高性能

- 第一范式（1NF）：字段不能再分

- 第二范式（2NF）：不存在部分依赖

  ![image-20220218104941685](https://www.itbaizhan.com/wiki/imgs/image-20220218104941685-16451525827202.png)

- 第三范式（3NF）：不存在间接依赖

  ![image-20220218105026569](https://www.itbaizhan.com/wiki/imgs/image-20220218105026569-16451526275663.png)

使用范式可以减少冗余，但是会降低性能

特定表的的设计可以违反第三范式，增加冗余提高性能

# 十二、数据库表关系

![image-20220218160156825](https://www.itbaizhan.com/wiki/imgs/image-20220218160156825-16451713179664.png)

## I、表关系简介

设计关系数据库的一个重要部分是将数据元素划分为相关的表，我们可以根据数据本身的关联性，将不同表之间的数据聚合在一起。

> **注意：**
>
> 无论在表与表之间建立了什么样的关系，决定数据之间是否有关系的不是表，而是数据本身。

**表与表的关系类型**

表与表之存在三种关系（relation），即一对一，一对多，多对多关系。

- **一对一**（one-to-one）：一种对象与另一种对象是一一对应关系，比如一个学生只能在一个班级里。
- **一对多**（one-to-many）： 一种对象可以属于另一种对象的多个实例，比如一个班级里有很多学生。
- **多对多**（many-to-many）：两种对象彼此都是"一对多"关系，比如一个歌单里包含多首歌，同时一首歌可以属于多个歌单。

**实时效果反馈**

**1. 决定数据之间是否有关系的是**

A 表关系

B 数据本身

C SQL语句

D 数据文件

**答案**

1=>B

## II、一对多关系

一种对象可以属于另一种对象的多个实例。

![image-20220218161711212](https://www.itbaizhan.com/wiki/imgs/image-20220218161711212-16451722321866.png)

一对多关系是建立在两张表之间的关系。一个表中的一条数据可以对应另一个表中的多条数据。

可以添加外键约束保证数据的参照完整性，外键永远在多方。外键允许重复，允许含有空值。

> **注意：**
>
> 如果添加的外键约束，那么删除数据时，一定是先删除有外键一方的数据。

## III、一对一关系

一种对象与另一种对象是一一对应关系。

![image-20220218162304309](https://www.itbaizhan.com/wiki/imgs/image-20220218162304309-16451725854347.png)

一对一关系是建立在一对多的基础之上，一个表中的一条数据只能对应另一个表中的一条数据。

可以添加外键约束保证数据的参照完整性，外键可以在任何一方，需要让外键具备唯 一约束。

> **注意：**
>
> 如果添加的外键约束，那么删除数据时，一定是先删除有外键一方的数据。

## IV、多对多关系

两种对象彼此都是"一对多"关系

![image-20220218165153497](https://www.itbaizhan.com/wiki/imgs/image-20220218165153497-16451743145389.png)

需要建立一个中间表，中间表里建立两个列，然后需要用这两个列作为这个表的联合主键，然后每个列在作为外键参照各自的表的主键。

> **注意：**
>
> 存数据：先两侧，再中间表。
>
> 删数据：先中间表（即有外键的表），再两侧。

# 十三、##JDBC

## I、JDBC概述

**数据的持久化**

- 持久化(persistence)：将内存中的数据保存到可永久保存的存储设备中（如磁盘）。

- 持久化的主要应用是将内存中的数据存储在关系型数据库中，当然也可以存储在磁盘文件、XML数据文件中。

  ![image-20211021144339852](https://www.itbaizhan.com/wiki/imgs/JDBC%E6%A6%82%E8%BF%B01.png)

**什么是** **JDBC**

- JDBC（Java DataBase Connectivity）java 数据库连接
- 是 JavaEE 平台下的技术规范
- 定义了在 Java 语言中连接数据库，执行 SQL 语句的标准 API
- 可以为多种关系数据库提供统一访问

**什么是数据库驱动程序**

- 数据库驱动就是直接操作数据库的一个程序
- 不同数据产品的数据库驱动名字有差异
- 在程序中需要依赖数据库驱动来完成对数据库的操作

**Java中访问数据库技术**

- 基于JDBC标准访问数据库
- 使用第三方ORM 框架，如Hibernate, Mybatis 等访问数据库

**程序操作数据库流程**

如果没有JDBC，那么Java程序访问数据库时是这样的：

![image-20220224113653854](https://www.itbaizhan.com/wiki/imgs/image-20220224113653854-164567381511110.png)

有了JDBC，Java程序访问数据库时是这样的：

![image-20220224113645120](https://www.itbaizhan.com/wiki/imgs/image-20220224113645120-16456738061779.png)

**实时效果反馈**

**1. JDBC是 Java 语言中的标准 。**

A 创建对象

B 操作磁盘

C 操作数据库

D 连接网络

**答案**

1=>C

## II、JBDC中常用的类与接口

1. **Driver** **接口**

   Driver 接口的作用是来定义数据库驱动对象应该具备的一些能力。比如与数据库建立连

   接的方法的定义，该接口是提供给数据库厂商使用的，所有支持 java 语言连接的数据库都实现了该接口，实现该接口的类我们称之为数据库驱动类。

2. **DriverManager** **类**

   DriverManager是驱动程序管理器，是负责管理数据库驱动程序的。驱动注册以后，会保存在DriverManager中的已注册列表中。 DriverManager 通过实例化的数据库驱动对象，能够建立应用程序与数据库之间建立连 接。并返回 Connection 接口类型的数据库连接对象。

   - getConnection(String jdbcUrl, String user, String password)

     该方法通过访问数据库的 url、用户以及密码，返回对应的数据库的 Connection 对象。

   - JDBC URL

     与数据库连接时，用来连接到指定数据库标识符。在 URL 中包括了该数据库的类型、 地址、端口、库名称等信息。不同品牌数据库的连接 URL 不同。

     - 连接 MySql 数据库：

       ```java
       Connection conn = DriverManager.getConnection("jdbc:mysql://host:port/database", "user", "password");
       ```

     - 连接 Oracle 数据库：

       ```java
       Connection conn = DriverManager.getConnection("jdbc:oracle:thin:@host:port:database", "user", "password");
       ```

3. **Connection** **接口**

   Connection 是数据库的连接（会话）对象。对数据库的一切操作都是在这个连接基础之上进行的，我们可以通过该对象执行 sql 语句并返回结果。

   **常用方法**

   - createStatement()

     创建向数据库发送 sql 的 Statement 接口类型的对象。

   - preparedStatement(sql)

     创建向数据库发送预编译 sql 的 PrepareSatement 接口类型的对象。

   - setAutoCommit(boolean autoCommit)

     设置事务是否自动提交。

   - commit()

     在链接上提交事务。

   - rollback()

     在此链接上回滚事务。

4. **Statement** **接口**

   用于执行静态 SQL 语句并返回它所生成结果的对象。 由 createStatement 创建，用于发送简单的 SQL 语句（不支持动态绑定）。

   **常用方法**

   - execute(String sql)

     执行参数中的 SQL，返回是否有结果集。

   - executeQuery(String sql)

     运行 select 语句，返回 ResultSet 结果集。

   - executeUpdate(String sql)

     运行 insert/update/delete 操作，返回更新的行数。

   - addBatch(String sql)

     把多条 sql 语句放到一个批处理中。

   - executeBatch()

     向数据库发送一批 sql 语句执行。

5. **PreparedStatement接口**

   继承自 Statement 接口，由 preparedStatement 创建，用于发送含有一个或多个参数的 SQL 语句。PreparedStatement 对象比 Statement 对象的效率更高，由于实现了动态的参数绑定，所以可以防止 SQL 注入，所以我们一般都使用 PreparedStatement。

   **常用方法**

   - addBatch()

     把当前 sql 语句加入到一个批处理中。

   - execute()

     执行当前 SQL，返回个 boolean 值

   - executeUpdate()

     运行 insert/update/delete 操作，返回更新的行数。

   - executeQuery()

     执行当前的查询，返回一个结果集对象

   - setDate(int parameterIndex, Date x)

     向当前SQL语句中的指定位置绑定一个java.sql.Date值

   - setDouble(int parameterIndex, double x)

     向当前 SQL 语句中的指定位置绑定一个 double值

   - setFloat(int parameterIndex, float x)

     向当前 SQL 语句中的指定位置绑定一个 float 值

   - setInt(int parameterIndex, int x)

     向当前 SQL 语句中的指定位置绑定一个 int 值

   - setString(int parameterIndex, String x)

     向当前 SQL 语句中的指定位置绑定一个 String 值

6. **ResultSet** **接口**

   ResultSet 用来暂时存放数据库查询操作获得结果集。

   **常用方法**

   - getString(int index)、getString(String columnName)

     获得在数据库里是 varchar、char 等类型的数据对象。

   - getFloat(int index)、getFloat(String columnName)

     获得在数据库里是 Float 类型的数据对象。

   - getDate(int index)、getDate(String columnName)

     获得在数据库里是 Date 类型的数据。

   - getBoolean(int index)、getBoolean(String columnName)

     获得在数据库里是 Boolean 类型的数据。

   - getObject(int index)、getObject(String columnName)

     获取在数据库里任意类型的数据。

**实时效果反馈**

**1. DriverManager是负责管理 。**

A RDBMS的

B 数据库连接程序的

C 数据库驱动程序的

D 数据库启动与关闭程序的

**2. Connection 是数据库 。**

A 连接对象

B 管理对象

C 执行SQL语句的对象

D 处理结果集对象

**答案**

1=>C 2=>A

## III、JDBC编写步骤

![image-20220720145751622](../AppData/Roaming/Typora/typora-user-images/image-20220720145751622.png)

**注**：ODBC(**Open Database Connectivity**，开放式数据库连接)，是微软在Windows平台下推出的。使用者在程序中只需要调用ODBC API，由 ODBC 驱动程序将调用转换成为对特定的数据库的调用请求。

**实时效果反馈**

**1. 使用JDBC操作数据库时，需要依赖哪个包?**

A java.util

B java.lang

C java.sql

D java.math

**2. 在使用JDBC执行一个SQL语句时，需要创建以下哪个对象：**

A Statement

B Connection

C ResultSet

D Scanner

**答案**

1=>C 2=>A

## IV、获取连接

![image-20220224113620018](https://www.itbaizhan.com/wiki/imgs/image-20220224113620018-16456737811688.png)

**环境：**

数据库Mysql5.7

数据库驱动版本5.1.48

数据库名itbz

**准备工作：**

新建JavaProject工程

添加数据库驱动jar包

获取数据库连接对象

**下载数据库驱动**

https://downloads.mysql.com/archives/c-j/

### 获取数据库连接

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

/**
 * 获取数据库连接测试类
 */
public class JDBCtest {
    public static void main(String[] args) throws ClassNotFoundException, SQLException {
        // 连接Mysql数据库的url
        String url = "jdbc:mysql://localhost:3306/itbz?useSSL=false";
        // 连接数据库的用户名
        String name = "root";
        // 连接数据库的密码
        String pwd = "root";
        // 通过反射实现数据库驱动的加载与注册
        Class.forName("com.mysql.jdbc.Driver");
        // 通过DriverManager对象获取数据库的连接对象
        Connection connection = DriverManager.getConnection(url,name,pwd);
        System.out.println(connection);
    }
}
```

1. 注：在加载com.mysql.jdbc.Driver类信息时，会执行静态块中的代码。在静态块中 ，数据库驱动会实例化自己并通过DriverManager的registerDriver方法，将自己注册DriverManager驱动管理器中。

![image-20220720152856046](../AppData/Roaming/Typora/typora-user-images/image-20220720152856046.png)

## V、Properties文件的使用

![image-20220224113607796](https://www.itbaizhan.com/wiki/imgs/image-20220224113607796-16456737688337.png)

**properties文件介绍**

后缀properties的文件是一种属性文件。这种文件以key=value格式存储内容。Java中可以使用Properties工具类来读取这个文件。项目中会将一些配置信息放到properties文件中，所以properties文件经常作为配置文件来使用。

**Properties工具类**

Properties工具类，位于java.util包中，该工具类继承自Hashtable<Object,Object>。通过Properties工具类可以读取.properties类型的配置文件。

**Properties工具类中常用方法**

load(InputStream is)

通过给定的输入流对象读取properties文件并解析

getProperty(String key)

根据key获取对应的value

**注意：**

如果properties文件中含有中文那么需要对idea进行设置。

![image-20220224113555137](https://www.itbaizhan.com/wiki/imgs/image-20220224113555137-16456737562666.png)

**properties文件**

```properties
#我是中国人
key1=ITBZ
key2=BJSXT
key3=我是中国人
```

**操作properties文件**

```java
package com.itshihao;

import java.io.IOException;
import java.io.InputStream;
import java.util.Properties;

/**
 *  读取properties配置文件的测试类
 */
public class PropertiesTest {
    public static void main(String[] args) throws IOException {
        // 实例化Properties对象
        Properties properties = new Properties();
        // 获取读取properties文件的输入流对象
        InputStream is = PropertiesTest.class.getClassLoader().getResourceAsStream("test.properties");
        // 通过给定的输入流对象读取properties文件并解析
        properties.load(is);
        // 获取properties文件中的内容
        String value1 = properties.getProperty("key1");
        String value2 = properties.getProperty("key2");
        String value3 = properties.getProperty("key3");
        System.out.println(value1 + " " + value2 + " " + value3);
    }
}
```

**问：**

```java
// 获取读取properties文件的输入流对象
InputStream is = PropertiesTest.class.getClassLoader().getResourceAsStream("test.properties");
```

为什么要用类类加载器的方式获取IO，读取配置文件？自己尝试自定义InputStream is = new FileInputStream("test.properties"),这样就报错呢（找不到文件的错）？这里必须是使用类加载器的这种方式吗？

**答：*****properties文件的获取是需要这样去获取的，有三种方式****

1. **1、基于ClassLoder读取配置文件**

**注意**：该方式只能读取类路径下的配置文件，有局限但是如果配置文件在类路径下比较方便。

```java
Properties properties = new Properties();
    // 使用ClassLoader加载properties配置文件生成对应的输入流
    InputStream in = PropertiesMain.class.getClassLoader().getResourceAsStream("config/config.properties");
    // 使用properties对象加载输入流
    properties.load(in);
    //获取key对应的value值
    properties.getProperty(String key);
```

1. **2、基于 InputStream 读取配置文件**

**注意**：该方式的优点在于可以读取任意路径下的配置文件

```java
 Properties properties = new Properties();
         
  // 使用InPutStream流读取properties文件
  BufferedReader bufferedReader = new BufferedReader(new FileReader("E:/config.properties"));
   properties.load(bufferedReader);
   // 获取key对应的value值6     properties.getProperty(String key);
```

1. **3、通过 java.util.ResourceBundle 类来读取，这种方式比使用 Properties 要方便一些**

　　1>通过 ResourceBundle.getBundle() 静态方法来获取（ResourceBundle是一个抽象类），这种方式来获取properties属性文件不需要加.properties后缀名，只需要文件名即可

```java
properties.getProperty(String key);
//config为属性文件名，放在包com.test.config下，如果是放在src下，直接用config即可 
ResourceBundle resource = ResourceBundle.getBundle("com/test/config/config");
 String key = resource.getString("keyWord");
```

## VI、通过properties文件来优化获取数据库连接

将连接数据库时所需要的信息存放到properties文件中，可以解决**硬编码**的问题。

**properties文件内容**

```properties
#连接Mysql数据库的URL
url=jdbc:mysql://localhost:3306/itbz?useSSL=false
#连接数据库的用户名
username=root
#连接数据库的密码
pwd=root
#数据库驱动名称
driver=com.mysql.jdbc.Driver
```

**获取连接**

```java
package com.itshihao;

import java.io.IOException;
import java.io.InputStream;
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
import java.util.Properties;

/**
 * 优化获取数据库连接
 */
public class JdbcTest2 {
    public static void main(String[] args) throws IOException, SQLException, ClassNotFoundException {
        // 实例化Properties对象
        Properties prop = new Properties();
        // 获取读取Properties文件的字节输入流对象
        InputStream is = JdbcTest2.class.getClassLoader().getResourceAsStream("jdbc.properties");
        // 读取Properties文件并解析
        prop.load(is);
        // 获取连接数据库的url
        String url = prop.getProperty("url");
        // 获取连接数据库的用户名
        String name = prop.getProperty("username");
        // 获取连接数据库的密码
        String pwd = prop.getProperty("pwd");
        // 获取数据库驱动全名
        String drivername = prop.getProperty("driver");
        // 加载并注册驱动
        Class.forName(drivername);
        // 通过驱动管理器对象获取连接对象
        Connection connection = DriverManager.getConnection(url, name, pwd);
        System.out.println(connection);
    }
}
```

## VII、 封装JDBC工具类

![image-20220224113540078](https://www.itbaizhan.com/wiki/imgs/image-20220224113540078-16456737413155.png)

**properties文件**

```properties
#连接Mysql数据库的URL
url=jdbc:mysql://localhost:3306/itbz?useSSL=false
#连接数据库的用户名
username=root
#连接数据库的密码
pwd=root
#数据库驱动名称
driver=com.mysql.jdbc.Driver
```

**JdbcUtil工具类**

```java
package com.itshihao;

import java.io.InputStream;
import java.sql.*;
import java.util.Properties;

/**
 * JDBC工具类
 */
public class JdbcUtils {
    private static String url;
    private static String name;
    private static String pwd;
    static {
        try {
            // 实例化Properties对象
            Properties prop = new Properties();
            // 获取读取Properties文件的字节输入流对象
            InputStream is = JdbcTest2.class.getClassLoader().getResourceAsStream("jdbc.properties");
            // 读取Properties文件并解析
            prop.load(is);
            // 获取连接数据库的url
            url = prop.getProperty("url");
            // 获取连接数据库的用户名
            name = prop.getProperty("username");
            // 获取连接数据库的密码
            pwd = prop.getProperty("pwd");
            // 获取数据库驱动全名
            String drivername = prop.getProperty("driver");
            // 加载并注册驱动
            Class.forName(drivername);
        }catch (Exception e){
            e.printStackTrace();
        }
    }
    // 获取数据库连接对象
    public static Connection getConnection(){
        Connection connection = null;
        try {
            connection = DriverManager.getConnection(url,name,pwd);
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        return connection;
    }
    // 关闭连接对象
    public static void closeConnection(Connection connection){
        try {
            connection.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 提交事务
    public static void commit(Connection connection){
        try {
            connection.commit();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 事务回滚
    public static void rollback(Connection connection){
        try {
            connection.rollback();
        }catch (Exception e){
            e.printStackTrace();
        }
    }
    // 关闭Statement对象
    public static void closeStatement(Statement statement){
        try {
            statement.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 关闭ResultSet
    public static void closeResultSet(ResultSet resultSet){
        try {
            resultSet.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // DML操作时关闭资源
    public static void closeResource(Statement statement,Connection connection){
        // 先关闭Statement对象
        closeStatement(statement);
        // 再关闭Connection对象
        closeConnection(connection);
    }
    // 查询时关闭资源
    public static void closeResource(ResultSet resultSet,Statement statement,Connection connection){
        // 先关闭ResultSet对象
        closeResultSet(resultSet);
        // 再关闭Statement对象
        closeStatement(statement);
        // 最后关闭Connection对象
        closeConnection(connection);
    }
}

```

# 十四、##Statement的使用



## I、Statement简介

**Statement接口特点**

用于执行静态 SQL 语句并返回它所生成结果的对象。 由 createStatement 创建，用于发送简单的 SQL 语句（不支持动态绑定）。

> **注意：**
>
> 由于Statement对象是一个执行静态SQL语句的对象，所以该对象存在SQL注入风险。

**JDBC中三种Statement对象**

- Statement：用于执行静态 SQL 语句。
- PreparedStatement：用于执行预编译SQL语句。
- CallableStatement：用于执行数据库存储过程。

![image-20220224113519587](https://www.itbaizhan.com/wiki/imgs/image-20220224113519587-16456737206634.png)

**实时效果反馈**

**1. Statement对象是一个的对象。**

A 加载数据库驱动

B 创建数据库连接

C 执行动态sql语句

D 执行静态sql语句

**答案**

1=>D

## II、通过Statement添加数据

**创建表**

```sql
CREATE TABLE `users` (
  `userid` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(30) DEFAULT NULL,
  `userage` int(11) DEFAULT NULL,
  PRIMARY KEY (`userid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

**添加数据**

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.Statement;

/**
 * Statement对象的使用
 */
public class StatementTest {
    /**、
     * 添加用户
     */
    public void insertUsers(String username,int userage){
        Connection connection = null;
        Statement statement = null;
        try {
            // 获取Connection对象
            connection = JdbcUtils.getConnection();
            // 获取Statement对象
            statement = connection.createStatement();
            // 定义需要执行的SQL语句
            String sql = "insert into users values(default,'"+username+"',"+userage+") ";
            // 执行SQL,返回boolean值，如果sql有结果集返回，那么返回值为true，如果没有结果集返回，则返回false。
            boolean execute = statement.execute(sql);
            System.out.println(execute);
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(statement,connection);
        }
    }
}

```

Test类：

```java
package com.itshihao;

public class Test {
    public static void main(String[] args) {
        StatementTest statementTest = new StatementTest();
        statementTest.insertUsers("oldli",18);
    }
}
// false
```

## III、通过Statement修改数据

```java
/**
 * 修改用户信息
 */
public void updateUser(int userid,String username,int userage){
    Connection connection = null;
    Statement statement = null;
    try {
        // 获取连接对象
        connection = JdbcUtils.getConnection();
        // 获取Statement对象
        statement = connection.createStatement();
        // 定义sql语句
        String sql = "update users set username = '"+username+"',userage = "+userage+" where userid = " + userid;
        // 执行sql语句
        int i = statement.executeUpdate(sql);
        System.out.println(i);
    }catch (Exception e){
        e.printStackTrace();
    }finally {
        JdbcUtils.closeResource(statement,connection);
    }
}
```

Test类：

```java
public class Test {
    public static void main(String[] args) {
        StatementTest statementTest = new StatementTest();
//        statementTest.insertUsers("oldli",18);
        statementTest.updateUser(1,"Kevin",20);
    }
}
// 1
```

## IV、通过Statement删除数据

```java
/**
 * 根据用户id删除用户
 */
public void deleteUserbyId(int userid){
    Connection connection = null;
    Statement statement = null;
    try {
        // 获取数据库连接
        connection = JdbcUtils.getConnection();
        // 获取Statement对象
        statement = connection.createStatement();
        // 定义删除sql语句
        String sql = "delete from users where userid = " + userid;
        // 执行sql语句
        int i = statement.executeUpdate(sql);
        System.out.println(i);
    }catch (Exception e){
        e.printStackTrace();
    }finally {
        JdbcUtils.closeResource(statement,connection);
    }
}
```

Test类：

```java
package com.itshihao;

public class Test {
    public static void main(String[] args) {
        StatementTest statementTest = new StatementTest();
//        statementTest.insertUsers("oldli",18);
//        statementTest.updateUser(1,"Kevin",20);
        statementTest.deleteUserbyId(1);
    }
}
// 1
```

# 十五、PreparedStatement的使用(重点)

![image-20220224113506800](https://www.itbaizhan.com/wiki/imgs/image-20220224113506800-16456737080463.png)

## I、 PreparedStatement对象简介

继承自 Statement 接口，由 preparedStatement方法创建。PreparedStatement具有预编译SQL语句能力，所以PreparedStatement 对象比 Statement 对象的效率更高，由于实现了动态的参数绑定，所以可以防止 SQL 注入，所以我们一般都使用 PreparedStatement。

**PreparedStatement对象的特点：**

- PreparedStatement 接口继承 Statement 接口
- PreparedStatement 效率高于 Statement
- PreparedStatement 支持动态绑定参数
- PreparedStatement 具备 SQL 语句预编译能力
- 使用 PreparedStatement 可防止出现 SQL 注入问题

### PreparedStatement 的预编译能力

**语句的执行步骤**

- 语法和语义解析
- 优化 sql 语句，制定执行计划
- 执行并返回结果

但是很多情况，我们的一条 sql 语句可能会反复执行，或者每次执行的时候只有个别的值不同（比如 select 的 where 子句值不同，update 的 set 子句值不同,insert 的 values 值不同）。 如果每次都需要经过上面的词法语义解析、语句优化、制定执行计划等，则效率就明显不行 了。所谓预编译语句就是将这类语句中的值用占位符替代，可以视为将 sql 语句模板化或者说参数化预编译语句的优势在于：一次编译、多次运行，省去了解析优化等过程；此外预编译语 句能防止 sql 注入

**实时效果反馈**

**1. PreparedStatement对象是一个的对象。**

A 加载数据库驱动

B 创建数据库连接

C 执行动态sql语句

D 具有预编译sql语句

**答案**

1=>D

## II、通过PreparedStatement添加数据

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;

/**
 * Statement对象的使用
 */
public class StatementTest {
    /**、
     * 添加用户
     */
    public void insertUsers(String username,int userage){
        Connection connection = null;
        Statement statement = null;
        try {
            // 获取Connection对象
            connection = JdbcUtils.getConnection();
            // 获取Statement对象
            statement = connection.createStatement();
            // 定义需要执行的SQL语句
            String sql = "insert into users values(default,'"+username+"',"+userage+") ";
            // 执行SQL,返回boolean值，如果sql有结果集返回，那么返回值为true，如果没有结果集返回，则返回false。
            boolean execute = statement.execute(sql);
            System.out.println(execute);
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(statement,connection);
        }
    }

    /**
     * 修改用户信息
     */
    public void updateUser(int userid,String username,int userage){
        Connection connection = null;
        Statement statement = null;
        try {
            // 获取连接对象
            connection = JdbcUtils.getConnection();
            // 获取Statement对象
            statement = connection.createStatement();
            // 定义sql语句
            String sql = "update users set username = '"+username+"',userage = "+userage+" where userid = " + userid;
            // 执行sql语句
            int i = statement.executeUpdate(sql);
            System.out.println(i);
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(statement,connection);
        }
    }
    /**
     * 根据用户id删除用户
     */
    public void deleteUserbyId(int userid){
        Connection connection = null;
        Statement statement = null;
        try {
            // 获取数据库连接
            connection = JdbcUtils.getConnection();
            // 获取Statement对象
            statement = connection.createStatement();
            // 定义删除sql语句
            String sql = "delete from users where userid = " + userid;
            // 执行sql语句
            int i = statement.executeUpdate(sql);
            System.out.println(i);
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(statement,connection);
        }
    }
}

```

Test类：

```java
package com.itshihao;

public class Test {
    public static void main(String[] args) {
        PreparedStatementTest pst = new PreparedStatementTest();
        pst.insertUsers("oldli",18);
    }
}
// 1
```

## III、通过PreparedStatement修改数据

```java
/**
 * 根据用户ID修改用户姓名与年龄
 */
public void updateUsersById(int userid,String username,int userage){
    Connection connection = null;
    PreparedStatement ps = null;
    try {
       //获取数据库连接对象
        connection = JdbcUtils.getConnection();
        //创建PreparedStatement对象
        ps = connection.prepareStatement("update users set username = ?,userage = ? where userid = ?");
        ps.setString(1,username);
        ps.setInt(2,userage);
        ps.setInt(3,userid);
        int i = ps.executeUpdate();
        System.out.println(i);
    }catch (Exception e){
        e.printStackTrace();
    }finally {
        JdbcUtils.closeResource(ps,connection);
    }
}
```

Test类：

```java
package com.itshihao;

public class Test {
    public static void main(String[] args) {
        PreparedStatementTest pst = new PreparedStatementTest();
        pst.updateUsersById(2,"oldshao",17);
    }
}
// 1
```

## IV、通过PreparedStatement删除数据

```java
/**
 * 根据用户ID删除指定用户
 */
public void deleteUsersById(int userid){
    Connection connection = null;
    PreparedStatement ps = null;
    try {
        //获取数据库连接对象
        connection = JdbcUtils.getConnection();
        //创建PreparedStatement对象
        ps = connection.prepareStatement("delete from users where userid = ?");
        // 绑定参数
        ps.setInt(1,userid);
        int i = ps.executeUpdate();
        System.out.println(i);
    }catch (Exception e){
        e.printStackTrace();
    }finally {
        JdbcUtils.closeResource(ps,connection);
    }
}
```

Test类：

```java
package com.itshihao;

public class Test {
    public static void main(String[] args) {
        PreparedStatementTest pst = new PreparedStatementTest();
        pst.deleteUsersById(2);
    }
}
// 1
```

# 十六、ResultSet的使用



## I、ResultSet简介

**ResultSet接口的特点**

ResultSet用来存放数据库查询操作获得结果集，通过对ResultSet的操作可以获取查询到的结果集数据。

> **注意：**
>
> ResultSet 对象中存放的并不是我们查询到的所有的结果集。它采用分块加载的方式来载入结果集数据。

**ResultSet特点**

- ResultSet 对象具有指向其当前数据行的指针。最初，指针被置于第一行之前。next 方法将指针移动到下一行；因为该方法在 ResultSet 对象中没有下一行时返回 false，所以可以在 while 循环中使用它来迭代结果集。
- 默认的 ResultSet 对象仅有一个向前移动的指针。因此，只能迭代它一次，并且只能按从第一行到最后一行的顺序进行。
- ResultSet 接口提供用于获取当前行检索列值的获取方法（getBoolean、getLong 等）。可以使用列的索引位置或列的名称检索值。

**ResultSet使用原理**

![image-20220224113444646](https://www.itbaizhan.com/wiki/imgs/image-20220224113444646-16456736865352.png)

**实时效果反馈**

**1. ResultSet获取下一行数据的方法是：**

A getnext()

B getrow()

C nextrow()

D next()

**答案**

1=>D

## II、通过ResultSet获取查询结果

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;

/**
 * 获取结果集测试类
 */
public class ResultSetTest {
    /**
     * 查询所有用户
     */
    public void selectUsersAll(){
        Connection connection = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        try {
            // 获取数据库连接
            connection = JdbcUtils.getConnection();
            // 创建PrepareStatement对象
            ps = connection.prepareStatement("select * from users");
            // 执行查询
            rs = ps.executeQuery();
            //操作ResultSet对象获取查询的结果集
            while (rs.next()){
                //获取列中的数据
                int userid = rs.getInt("userid");
                String username = rs.getString("username");
                int userage = rs.getInt("USERAGE");
                System.out.println(userid + " " + username + " " + userage);
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(rs,ps,connection);
        }
    }
}
```

Test类：

```java
public class Test {
    public static void main(String[] args) {
        ResultSetTest rst = new ResultSetTest();
        rst.selectUsersAll();
    }
}
// 1 oldli 28
// 2 Kevin 29
```

# 十七、ORM编程思想



## I、ORM简介

对象关系映射（英语：Object Relational Mapping，简称ORM，或O/R mapping）是一种为了解决面向对象语言与关系数据库存在的互不匹配的现象。

![image-20220224113428704](https://www.itbaizhan.com/wiki/imgs/image-20220224113428704-16456736703411.png)

**实体类**

实体类就是一个定义了属性，拥有getter、setter、无参构造方法（基本必备）的一个类。实体类可以在数据传输过程中对数据进行封装，相当于一个“工具”、“容器”、“载体”，能存储、传输数据，能管理数据。

**实体类特点：**

1. 实体类名，尽量和数据库中的表名一一对应
2. 实体类中的属性对应数据库表中的字段，相关的命名最好也一一对应
3. 实体类内方法主要有，getter、setter方法，用于设置、获取数据
4. 实体类属性一般为private类型，方法为public类型
5. 实体类应该有，无参、有参构造方法

**实时效果反馈**

**1. ORM是一种为了解决存在的互不匹配的现象。**

A 对象与关系型数据库

B 对象与对象

C 对象与方法

D 对象与属性

**2. 实体类的作用是。**

A 处理数据

B 存储数据

C 持久化数据

D 销毁数据

**答案**

1=>A 2=>B

## II、ORM使用

**Users实体类**

```java
package com.itshihao;

public class Users {
    private int userid;
    private String username;
    private int userage;

    public int getUserid() {
        return userid;
    }

    public void setUserid(int userid) {
        this.userid = userid;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public int getUserage() {
        return userage;
    }

    public void setUserage(int userage) {
        this.userage = userage;
    }
}
```

**ORM映射**

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.ArrayList;
import java.util.List;

/**
 * 获取结果集测试类
 */
public class ResultSetTest {
    /**
     * 查询所有用户
     */
    public List<Users> selectUsersAll(){

        Connection connection = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        List<Users> list = new ArrayList<>();
        try {
            // 获取数据库连接
            connection = JdbcUtils.getConnection();
            // 创建PrepareStatement对象
            ps = connection.prepareStatement("select * from users");
            // 执行查询
            rs = ps.executeQuery();
            //操作ResultSet对象获取查询的结果集
            while (rs.next()){
                //获取列中的数据
                int userid = rs.getInt("userid");
                String username = rs.getString("username");
                int userage = rs.getInt("USERAGE");
//                System.out.println(userid + " " + username + " " + userage);
                Users users = new Users();
                users.setUserid(userid);
                users.setUsername(username);
                users.setUserage(userage);
                list.add(users);
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(rs,ps,connection);
        }
        return list;
    }
}
```

Test类：

```java
package com.itshihao;

import java.util.List;

public class Test {
    public static void main(String[] args) {
        ResultSetTest rst = new ResultSetTest();
        List<Users> list = rst.selectUsersAll();
        for (Users users : list) {
            System.out.println(users.getUserid() + " " + users.getUsername() + " " + users.getUserage());
        }
    }
}
```

# 十八、SQL注入

![1226](https://www.itbaizhan.com/wiki/imgs/1226.jpg)

## I、什么是SQL注入

所谓 SQL 注入，就是通过把含有 SQL 语句片段的参数插入到需要执行的 SQL 语句中，

最终达到欺骗数据库服务器执行恶意操作的 SQL 命令。

## II、SQL注入案例

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.ResultSet;
import java.sql.Statement;
/**
 * SQL注入测试类
 */
public class SqlInject {
    /**
     * 体现sql注入
     */
    public void selectByUsernameAndUserage(String username,int userage){
        Connection connection = null;
        Statement statement = null;
        ResultSet resultSet = null;
        try {
            //获取连接
            connection = JdbcUtils.getConnection();
            //创建Statement对象
            statement = connection.createStatement();
            //定义sql语句
            String sql = "select * from users where username = '"+username+"' and userage = "+userage;
            System.out.println(sql);
            //执行sql语句
            resultSet = statement.executeQuery(sql);
            //处理结果集
            while (resultSet.next()){
                int userid = resultSet.getInt("userid");
                String name = resultSet.getString("username");
                int age = resultSet.getInt("userage");
                System.out.println(userid + " " + name + " " + age);
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(resultSet,statement,connection);
        }
    }

    public static void main(String[] args) {
        SqlInject sqlInject = new SqlInject();
        sqlInject.selectByUsernameAndUserage("oldli' or 1=1  -- ",28);
    }
}

```

## III、##解决SQL注入

```java
    /**
     * 解决sql注入
     */
    public void noSqlInject(String username,int userage){
        Connection connection = null;
        PreparedStatement ps = null;
        ResultSet resultSet = null;
        try {
            //获取连接
            connection = JdbcUtils.getConnection();
            //创建PreparedStatement对象
            ps = connection.prepareStatement("select * from users where username = ? and userage = ?");
            //绑定参数
            ps.setString(1,username);
            ps.setInt(2,userage);
            //执行sql
            resultSet = ps.executeQuery();
            //处理结果集
            while (resultSet.next()){
                int userid = resultSet.getInt("userid");
                String name = resultSet.getString("username");
                int age = resultSet.getInt("userage");
                System.out.println(userid + " " + name + " " + age);
            }

        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(resultSet,ps,connection);
        }
    }
    public static void main(String[] args) {
        SqlInject sqlInject = new SqlInject();
//        sqlInject.sqlInject("oldli' or 1=1  -- ",28);
        sqlInject.noSqlInject("oldli",28);
    }
}
```

# 十九、JDBC批量添加数据



## I、批量添加数据简介

在JDBC中通过PreparedStatement的对象的addBatch()和executeBatch()方法进行数据的批量插入。

- addBatch()把若干SQL语句装载到一起，然后一次性传送到数据库执行，即是批量处理sql数据的。
- executeBatch()会将装载到一起的SQL语句执行。

> **注意：**
>
> MySql默认情况下是不开启批处理的。
>
> 数据库驱动从5.1.13开始添加了一个对rewriteBatchStatement的参数的处理，该参数能够让MySql开启批处理。在url中添加该参数：rewriteBatchedStatements=true

**Mysql的URL参数说明**

|                          |                       |                                                    |
| ------------------------ | --------------------- | -------------------------------------------------- |
| useUnicode               | [true \| false]       | 是否使用编码集,需配合 characterEncoding 参数使用。 |
| characterEncoding        | [utf-8 \| gbk \| ...] | 编码类型。                                         |
| useSSL                   | [true \| false]       | 是否使用SSL协议。                                  |
| rewriteBatchedStatements | [true \| false]       | 可以重写向数据库提交的SQL语句。                    |

**实时效果反馈**

**1. 在JDBC中，完成批量添加时需要依赖的方法是**。

A batch()和executeBatch()

B addBatch()和batch()

C addBatch()和executeBatch()

D add()和execute()

**2. JDBC中，向Mysql数据库批量添加数据时，需要在URL中添加哪个参数？**

A useUnicode

B characterEncoding

C rewriteBatchedStatements

D useSSL

**答案**

1=>C 2=>C

## II、实现数据的批量添加

**在url中开启批量添加**

```properties
rewriteBatchedStatements=true
```

**实现数据的批量添加方式一**

```java
public class AddBatchTest {
    /**
     * 批量添加数据方式一
     */
    public void addBatch1(){
        //创建连接
        Connection connection = null;
        //创建PreparedStatement
        PreparedStatement ps = null;
        try {
            connection = JdbcUtils.getConnection();
            ps = connection.prepareStatement("insert into users values (default,?,?)");
            //参数绑定
            for (int i = 0; i < 1000; i++) {
                //绑定username
                ps.setString(1,"itbz"+i);
                //绑定userage
                ps.setInt(2,20);
                //缓存sql
                ps.addBatch();
            }
            //执行sql
            ps.executeBatch();
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(ps,connection);
        }
    }
    public static void main(String[] args) {
        AddBatchTest a = new AddBatchTest();
        a.addBatch1();
    }
}
```

**实现数据的批量添加方式二**

```java
/**
 * 批量添加数据方式二
 */
public void addBatch2(){
    Connection connection = null;
    PreparedStatement ps = null;
    try {
        //创建连接
        connection = JdbcUtils.getConnection();
        //创建PreparedStatement
        ps = connection.prepareStatement("insert into users values (default,?,?)");
        //参数绑定
        for (int i = 1; i <= 1000; i++) {
            //绑定username
            ps.setString(1,"itbz"+i);
            //绑定userage
            ps.setInt(2,20);
            //缓存sql
            ps.addBatch();
            if (i % 500 == 0){
                //执行sql
                ps.executeBatch();
                // ******清除缓存******
                ps.clearBatch();
            }
        }
    }catch (Exception e){
        e.printStackTrace();
    }finally {
        JdbcUtils.closeResource(ps,connection);
    }
}
public static void main(String[] args) {
        AddBatchTest a = new AddBatchTest();
        a.addBatch2();
    }
```

# 二十、JDBC事务处理

![image-20211025101205148](https://www.itbaizhan.com/wiki/imgs/image-20211025101205148.png)

## I、事务简介

1. 事务：

   事务是指作为单个逻辑工作单元执行的一系列操作，要么完全地执行，要么完全地不执行。

2. 事务操作流程：

   - 开启事务
   - 提交事务
   - 回滚事务

**JDBC中事务处理特点**

在JDBC中，使用Connection对象来管理事务，默认为自动提交事务。可以通过setAutoCommit(boolean autoCommit)方法设置事务是否自动提交，参数为boolean类型，默认值为true，表示自动提交事务，如果值为false则表示不自动提交事务，需要通过commit方法手动提交事务或者通过rollback方法回滚事务。

**实时效果反馈**

**1. 如下哪项操作不属于事务操作流程：**

A 开启事务

B 提交事务

C 回滚事务

D 删除事务

**答案**

1=>D

## II、JDBC事务处理实现

```java
public void addBatch2(){
    Connection connection = null;
    PreparedStatement ps = null;
    try {
        //创建连接
        connection = JdbcUtils.getConnection();
        // 设置事务的提交方式，将自动提交修改为手动提交
        connection.setAutoCommit(false);
        //创建PreparedStatement
        ps = connection.prepareStatement("insert into users values (default,?,?)");
        //参数绑定
        for (int i = 1; i <= 1000; i++) {
            //绑定username
            ps.setString(1,"itbz"+i);
            //绑定userage
            ps.setInt(2,20);
            //缓存sql
            ps.addBatch();
            if (i % 500 == 0){
                //执行sql
                ps.executeBatch();
                //清除缓存
                ps.clearBatch();
            }
            if (i == 501){
                String str = null;
                str.length();
            }
        }
        // 提交事务
        JdbcUtils.commit(connection);
    }catch (Exception e){
        e.printStackTrace();
        JdbcUtils.rollback(connection);
    }finally {
        JdbcUtils.closeResource(ps,connection);
    }
}

public static void main(String[] args) {
    AddBatchTest a = new AddBatchTest();
    a.addBatch2();
}
```

# 二十一、Blob类型的使用

![image-20211025094729633](https://www.itbaizhan.com/wiki/imgs/image-20211025094729633.png)

## I、**MySql Blob类型简介**

Blob(全称：Binary Large Object 二进制大对象)。在MySql中，Blob是一个二进制的用来存储图片，文件等数据的数据类型。操作Blob类型的数据必须使用PreparedStatement，因为Blob类型的数据无法使用字符串拼接。大多数情况，并不推荐直接把文件存放在 MySQL 数据库中，但如果应用场景是文件与数据高度耦合，或者对文件安全性要求较高的，那么将文件与数据存放在一起，即安全，又方便备份和迁移。

**Mysql中的Blob类型**

MySql中有四种Blob类型，它们除了在存储的最大容量上不同，其他是一致的。

|    类型    |    大小     |
| :--------: | :---------: |
|  TinyBlob  | 最大255字节 |
|    Blob    |   最大65K   |
| MediumBlob |   最大16M   |
|  LongBlob  |   最大4G    |

**Blob类型使用的注意事项**

- 实际使用中根据需要存入的数据大小定义不同的Blob类型。
- 如果存储的文件过大，数据库的性能会下降。

**实时效果反馈**

**1. 在MySql中，以下类型不属于Blob数据类型的是。**

A TinyBlob

B MediumBlob

C varchar

D LongBlob

**2.在JDBC中，需要使用 对象操作Blob类型的数据？**

A Statement

B PreparedStatement

C Batch

D ResultSet

**答案**

1=>C 2=>B

## II、**插入Blob类型数据**

**创建表**

```sql
CREATE TABLE `movie` (
  `movieid` int(11) NOT NULL AUTO_INCREMENT,
  `moviename` varchar(30) DEFAULT NULL,
  `poster` mediumblob,
  PRIMARY KEY (`movieid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

**通过PreparedStatement存储Blob类型数据**

```java
package com.itshihao;

import java.io.File;
import java.io.FileInputStream;
import java.io.InputStream;
import java.sql.Connection;
import java.sql.PreparedStatement;
/**
 * Blob类型操作测试类
 */
public class BlobTest {
    /**
     * 向Movie表中插入数据
     */
    public void insertMovie(String moviename, InputStream is){
        Connection connection = null;
        PreparedStatement ps = null;
        try {
            //获取连接
            connection = JdbcUtils.getConnection();
            // 获取preparedStatement对象
            ps = connection.prepareStatement("insert into movie values (default ,?,?)");
            //绑定参数
            ps.setString(1,moviename);
            ps.setBlob(2,is);
            ps.executeUpdate();
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(ps,connection);
        }
    }

    public static void main(String[] args) throws Exception{
        BlobTest b = new BlobTest();
        InputStream is = new FileInputStream(new File("F:/1.jpg"));
        b.insertMovie("战狼",is);
    }
}
```

## III、读取Blob类型数据

```java
/**
     * 根据影片ID查询影片信息
     */
    public void selectByMovieId(int movieId){
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        try {
            //获取连接
            conn = JdbcUtils.getConnection();
            //创建PreparedStatement对象
            ps = conn.prepareStatement("select * from movie where movieid = ?");
            //绑定参数
            ps.setInt(1,movieId);
            //执行sql
            rs = ps.executeQuery();
            while (rs.next()){
                int id = rs.getInt("movieid");
                String name = rs.getString("moviename");
                System.out.println(id + " " + name);
                //获取blob类型的数据
                Blob blob = rs.getBlob("poster");
                // 获取能够从blob类型的列中读取数据的io流
                InputStream is = blob.getBinaryStream(); // 获取一个二进制流（读取图片）
                // 创建文件输出字节流对象
                OutputStream os = new FileOutputStream(id + "_" + name + ".jpg");
                // 操作流完成文件的输出处理
                byte[] buff = new byte[1024];
                int len;
                while ((len = is.read(buff)) != -1){
                    os.write(buff,0,len);
                }
                os.flush();
                is.close();
                os.close();
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(rs,ps,conn);
        }
    }

    public static void main(String[] args) throws Exception{
        BlobTest b = new BlobTest();
//        InputStream is = new FileInputStream(new File("F:/1.jpg"));
//        b.insertMovie("战狼",is);
        b.selectByMovieId(1);

    }

```

![image-20220721184904555](../AppData/Roaming/Typora/typora-user-images/image-20220721184904555.png)

# 二十二、JDBC其他查询方式

## I、模糊查询

![image-20220227153245167](https://www.itbaizhan.com/wiki/imgs/image-20220227153245167-16459471662745.png)

**实现模糊查询**

```java
/**
 * 模糊查询测试类
 */
public class FuzzyQueryTest {
    /**
     * 根据用户名称模糊查找用户信息
     */
    public List<Users> fuzzyQuery(String username){
        List<Users> list= new ArrayList<>();


        Connection conn =null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        try{
            //获取数据库连接
            conn = JdbcUtils.getConnection();
            //创建PreparedStatement对象
            ps = conn.prepareStatement("select * from users where username like ?");
            //参数绑定
            ps.setString(1,username);
            //执行sql语句
            rs = ps.executeQuery();
            while(rs.next()){
                Users user = new Users();
                user.setUserid(rs.getInt("userid"));
                user.setUsername(rs.getString("username"));
                user.setUserage(rs.getInt("userage"));
                list.add(user);
            }
        }catch(Exception e){
            e.printStackTrace();
        }finally{
            JdbcUtils.closeResource(rs,ps,conn);
        }
        return list;
    }


    public static void main(String[] args) {
        FuzzyQueryTest ft = new FuzzyQueryTest();
        List<Users> users = ft.fuzzyQuery("%d%");
        for(Users user1:users){
            System.out.println(user1.getUserid()+" "+user1.getUsername()+" "+user1.getUserage());
        }
    }
}

```

## II、动态条件查询



**动态条件查询实现**

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.ArrayList;
import java.util.List;

/**
 * 动态条件查询测试类
 */
public class DynamicConditionQueryTest {
    /**
     * 动态条件查询Users
     */
    public List<Users> queryUsers(Users users){
        List<Users> list = new ArrayList<>();
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        try {
            //获取数据库连接
            conn = JdbcUtils.getConnection();
           // 拼接sql语句
            String sql = this.generateSql(users);
            System.out.println(sql);
            // 创建PreparedStatement对象
            ps = conn.prepareStatement(sql);
            // 执行sql语句
            rs = ps.executeQuery();
            while (rs.next()) {
                Users user = new Users();
                user.setUserid(rs.getInt("userid"));
                user.setUsername(rs.getString("username"));
                user.setUserage(rs.getInt("userage"));
                list.add(user);
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(rs,ps,conn);
        }
        return list;
    }

    /**
     * 生成动态条件查询sql
     */
    private String generateSql(Users users){
        StringBuffer sb = new StringBuffer("select * from users where 1=1 ");
        if (users.getUserid() > 0){
            sb.append(" and userid = ").append(users.getUserid());
        }
        if (users.getUsername() != null && users.getUsername().length() > 0){
            sb.append(" and username = '").append(users.getUsername()).append("'");
        }
        if (users.getUserage() > 0){
            sb.append(" and userage = ").append(users.getUserage());
        }
        return sb.toString();
    }

    public static void main(String[] args) {
        DynamicConditionQueryTest dt = new DynamicConditionQueryTest();
        Users users = new Users();
//        users.setUsername("oldli");
//        users.setUserid(2);
        List<Users> list = dt.queryUsers(users);
        for (Users users1 : list) {
            System.out.println(users1.getUserid() + " " + users1.getUsername() + " " + users1.getUserage());
        }
    }
}
```

## III、分页查询



### 1、**分页查询简介**

当一个操作数据库进行查询的语句返回的结果集内容如果过多，那么内存极有可能溢出，所以在查询中含有大数据的情况下分页是必须的。

**分页查询分类：**

1. 物理分页：
   - 在数据库执行查询时（实现分页查询），查询需要的数据—依赖数据库的SQL语句
   - 在SQL查询时，从数据库只检索分页需要的数据
   - 通常不同的数据库有着不同的物理分页语句
   - MySql物理分页采用limit关键字
2. 逻辑分页：

- 在sql查询时，先从数据库检索出所有数据的结果集，在程序内，通过逻辑语句获得分页需要的数据

**如何在MySql中实现物理分页查询**

使用limit方式。

**limit的使用**

```sql
select * from tableName limit m,n
```

其中m与n为数字。n代表需要获取多少行的数据项，而m代表从哪开始(以0为起始)。

例如我们想从users表中先获取前两条数据SQL为：

```sql
select * from users limit 0,2;
```

那么如果要继续看下两条的数据则为：

```sql
select * from users limit 2,2;
```

以此类推

分页公式：(当前页-1)*每页大小

**实时效果反馈**

**1. MySql实现分页的关键字是**

A order

B top

C limit

D limit page

**答案**

1=>C

### 2、创建Page模型

![image-20220309150249929](https://www.itbaizhan.com/wiki/imgs/image-20220309150249929-16468093713094.png)

**Page**

```java
package com.itshihao;

import java.util.List;

/**
 * 分页查询实体类
 * @param <T>
 */
public class Page<T>{
    // 当前页
    private int currentPage;
    // 每页显示的条数
    private int pageSize;
    // 总条数
    private int totalCount;
    // 总页数
    private int totalPage;
    // 结果集
    private List<T> result;

    public int getCurrentPage() {
        return currentPage;
    }

    public void setCurrentPage(int currentPage) {
        this.currentPage = currentPage;
    }

    public int getPageSize() {
        return pageSize;
    }

    public void setPageSize(int pageSize) {
        this.pageSize = pageSize;
    }

    public int getTotalCount() {
        return totalCount;
    }

    public void setTotalCount(int totalCount) {
        this.totalCount = totalCount;
    }

    public int getTotalPage() {
        return totalPage;
    }

    public void setTotalPage(int totalPage) {
        this.totalPage = totalPage;
    }

    public List<T> getResult() {
        return result;
    }

    public void setResult(List<T> result) {
        this.result = result;
    }
}

```

### 3、实现分页查询

**分页实现**

```java
package com.itshihao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.ArrayList;
import java.util.List;

/**
 * 分页查询测试类
 */
public class PageTest {
    /**
     * 分页查询Users
     */
    public Page<Users> selectPage(Page page){
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        List<Users> list = new ArrayList<>();
        try {
            // 获取连接对象
            conn = JdbcUtils.getConnection();
            // 创建PreparedStatement对象
            ps = conn.prepareStatement("select  * from users limit ?,?");
            // 绑定m参数：m的值 = (当前页-1)*每页显示的条数
            ps.setInt(1,(page.getCurrentPage() - 1)*page.getPageSize());
            // 绑定n参数：n的值为每页显示的条数
            ps.setInt(2,page.getPageSize());
            // 执行查询
            rs = ps.executeQuery();
            // 处理结果集
            while (rs.next()) {
                // 完成ORM映射
                Users users = new Users();
                users.setUserid(rs.getInt("userid"));
                users.setUsername(rs.getString("username"));
                users.setUserage(rs.getInt("userage"));
                list.add(users);
            }
            // 将结果集存放到Page对象中
            page.setResult(list);
            // 查询总条数
            ps = conn.prepareStatement("select count(*) from users");
            // 执行总条数
            rs = ps.executeQuery();
            // 处理结果集
            while (rs.next()) {
                // 总条数
                int count = rs.getInt(1);
                // 保存总条数
                page.setTotalCount(count);
                // 换算 总页数=总条数/每页显示的条数 向上取整
                int totalpage  = (int) Math.ceil(1.0 * page.getTotalCount() / page.getPageSize());
                // 保存总页数
                page.setTotalPage(totalpage);
            }
        }catch (Exception e){
            e.printStackTrace();
        }finally {
            JdbcUtils.closeResource(rs,ps,conn);
        }
        return page;
    }

    public static void main(String[] args) {
        PageTest pt = new PageTest();
        Page page = new Page();
        page.setCurrentPage(1);
        page.setPageSize(2);
        Page page1 = pt.selectPage(page);
        System.out.println("总条数：" + page1.getTotalCount());
        System.out.println("总页数：" + page1.getTotalPage());
        System.out.println("当前页：" + page1.getCurrentPage());
        System.out.println("每页显示的条数：" + page1.getPageSize());
        List<Users> list = page1.getResult();
        for (Users users : list) {
            System.out.println(users.getUserid() + " " + users.getUsername() + " " + users.getUserage());
        }
    }
}
```

;



# 二十三、##数据库连接池

![image-20211025102445560](https://www.itbaizhan.com/wiki/imgs/image-20211025102445560.png)

## I、数据库连接池简介

**什么是数据库连接池**

数据库连接池（Connection pooling）是程序启动时建立足够的数据库连接，并将这些连接组成一个连接池，由程序动态地对池中的连接进行申请，使用，释放。

它允许应用程序重复使用一个现有的数据库连接，而不是再重新建立一个；释放空闲时间超过最大空闲时间的数据库连接来避免因为没有释放数据库连接而引起的数据库连接遗漏。这项技术能明显提高对数据库操作的性能。

**不使用数据库连接池存在的问题**

- 普通的JDBC数据库连接使用 DriverManager 来获取，每次向数据库建立连接的时候都要将 Connection加载到内存中，再验证用户名和密码，所以整个过程比较耗时。
- 需要数据库连接的时候，就向数据库要求一个，执行完成后再断开连接。这样的方式将会消耗大量的资源和时间。数据库的连接资源并没有得到很好的重复利用。若同时有几百人甚至几千人在线，频繁的进行数据库连接操作将占用很多的系统资源，严重的甚至会造成服务器的崩溃。
- 对于每一次数据库连接，使用完后都得断开。否则，如果程序出现异常而未能关闭，将会导致数据库系统中的内存泄漏，最终将导致重启数据库。

**JDBC数据库连接池的必要性**

- **数据库连接池的基本思想：**为数据库连接建立一个“缓冲池”。预先在缓冲池中放入一定数量的连接，当需要建立数据库连接时，只需从“缓冲池”中取出一个，使用完毕之后再放回去。
- **数据库连接池**负责分配、管理和释放数据库连接，它允许应用程序重复使用一个现有的数据库连接，而不是重新建立一个。
- **数据库连接池在初始化时**将创建一定数量的数据库连接放到连接池中，这些数据库连接的数量是由最小数据库连接数来设定的。无论这些数据库连接是否被使用，连接池都将一直保证至少拥有这么多的连接数量。连接池的最大数据库连接数量限定了这个连接池能占有的最大连接数，当应用程序向连接池请求的连接数超过最大连接数量时，这些请求将被加入到等待队列中。 ![image-20220227103609498](https://www.itbaizhan.com/wiki/imgs/image-20220227103609498-16459293704583.png)

**数据库连接池的优点**

1. **资源重用：**由于数据库连接得以重用，避免了频繁创建，释放连接引起的大量性能开销。在减少系统消耗的基础上，另一方面也增加了系统运行环境的平稳性。
2. **更快的系统反应速度：**数据库连接池在初始化过程中，往往已经创建了若干数据库连接置于连接池中备用。此时连接的初始化工作均已完成。对于业务请求处理而言，直接利用现有可用连接避免了数据库连接初始化和释放过程的时间开销，从而减少了系统的响应时间。
3. **新的资源分配手段：**对于多应用共享同一数据库的系统而言，可在应用层通过数据库连接池的配置实现某一应用最大可用数据库连接数的限制避免某一应用独占所有的数据库资源.
4. **统一的连接管理：**避免数据库连接泄露在较为完善的数据库连接池实现中，可根据预先的占用超时设定，强制回收被占用连接，从而避免了常规数据库连接操作中可能出现的资源泄露。

**常用的数据库连接池**

- c3p0：是一个开源组织提供的数据库连接池，速度相对较慢，稳定性还可以。
- DBCP：是Apache提供的数据库连接池。速度相对c3p0较快，但自身存在bug。
- Druid：是阿里提供的数据库连接池，据说是集DBCP、c3p0优点于一身的数据库连接池，目前经常使用。

**实时效果反馈**

**1. 数据库连接池是程序建立足够的数据库连接。**

A 闲置时

B 关闭时

C 启动时

D 运行时

**答案**

1=>C

## II、基于Druid封装工具类

```java
package com.itshihao;

import com.alibaba.druid.pool.DruidDataSourceFactory;

import javax.sql.DataSource;
import java.io.InputStream;
import java.sql.*;
import java.util.Properties;

/**
 * 基于Druid连接池获取数据库连接工具类
 */
public class JdbcDruidUtils {
    // 数据库连接对象
    private static DataSource dataSource;
    static {
        try {
            // 获取读取配置文件的字节输入流对象
            InputStream is = JdbcDruidUtils.class.getClassLoader().getResourceAsStream("druid.properties");
            // 创建Properties对象
            Properties pop = new Properties();
            // 加载配置文件
            pop.load(is);
            // 创建连接池对象
            dataSource = DruidDataSourceFactory.createDataSource(pop);
        }catch (Exception e){
            e.printStackTrace();
        }
    }
    // 获取数据库连接对象
    public static Connection getConnection(){
        Connection connection = null;
        try {
            connection = dataSource.getConnection();
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
        return connection;
    }
    // 关闭连接对象
    public static void closeConnection(Connection connection){
        try {
            connection.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 提交事务
    public static void commit(Connection connection){
        try {
            connection.commit();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 事务回滚
    public static void rollback(Connection connection){
        try {
            connection.rollback();
        }catch (Exception e){
            e.printStackTrace();
        }
    }
    // 关闭Statement对象
    public static void closeStatement(Statement statement){
        try {
            statement.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // 关闭ResultSet
    public static void closeResultSet(ResultSet resultSet){
        try {
            resultSet.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
    // DML操作时关闭资源
    public static void closeResource(Statement statement,Connection connection){
        // 先关闭Statement对象
        closeStatement(statement);
        // 再关闭Connection对象
        closeConnection(connection);
    }
    // 查询时关闭资源
    public static void closeResource(ResultSet resultSet,Statement statement,Connection connection){
        // 先关闭ResultSet对象
        closeResultSet(resultSet);
        // 再关闭Statement对象
        closeStatement(statement);
        // 最后关闭Connection对象
        closeConnection(connection);
    }
}
```

# 二十四、应用程序分层

![image-20220311151333621](https://www.itbaizhan.com/wiki/imgs/image-20220311151333621-16469828146022.png)

## I、**应用程序分层简介**

应用程序分层是指通过创建不同的包来实现项目的分层，将项目中的代码根据功能做具体划分，并存放在不同的包下。

**三层结构**

三层结构就是将整个业务应用划分为：表述层、业务逻辑层 、数据访问层。区分层次的目的即为了“高内 聚低耦合”的思想。在软件体系架构设计中，分层式结构是最常见，也是最重要的一种结构。

![image-20220311154638109](https://www.itbaizhan.com/wiki/imgs/image-20220311154638109-16469847992003.png)

**分层优点**

1. 分层结构将应用系统划分为若干层，每一层只解决问题的一部分，通过各层的协作提供整体解决方案。大的问题被分解为一系列相对独立的子问题，局部化在每一层中，这样就有效的降低了单个问题的规模和复杂度，实现了复杂系统的第一步也是最为关键的一步分解。
2. 分层结构具有良好的可扩展性，为应用系统的演化增长提供了一个灵活的支持，具有良好的可扩展性。增加新的功能时，无须对现有的代码做修改，业务逻辑可以得到最大限度的重用。
3. 分层结构易于维护。在对系统进行分解后，不同的功能被封装在不同的层中，层与层之间的耦合显著降低。因此在修改某个层的代码时，只要不涉及层与层之间的接口，就不会对其他层造成严重影响。

**分层命名**

表述层：web或controller

业务层：service

数据访问层：dao (Data Access Object)

**实时效果反馈**

**1. 应用程序分层是指通过创建不同的来实现项目的分层。**

A 工程

B 类

C 方法

D 包

**答案**

1=>D

## II、应用程序分层实现

![image-20220312142616605](https://www.itbaizhan.com/wiki/imgs/image-20220312142616605-16470663775575.png)

 ![image-20220722190934418](../AppData/Roaming/Typora/typora-user-images/image-20220722190934418.png)

## III、在分层项目中实现查询业务

UserDao接口

```java
public interface UserDao {
    /**
     * 根据用户id查询用户
     */
    Users selectUsersById(int userid);
}
```

UserDaoImpl接口实现类

```java
import com.itshihao.common.JdbcDruidUtils;
import com.itshihao.common.JdbcUtils;
import com.itshihao.dao.UserDao;
import com.itshihao.exception.ApplicationException;
import com.itshihao.pojo.Users;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;

public class UserDaoImpl implements UserDao {
    /**
     * 根据用户id查询用户
     * @param userid
     * @return
     */
    @Override
    public Users selectUsersById(int userid) {
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        Users users = null;
        try {
            conn = JdbcDruidUtils.getConnection();
            ps = conn.prepareStatement("select * from users where userid = ?");
            ps.setInt(1,userid);
            rs = ps.executeQuery();
            while (rs.next()) {
                // 手动ORM映射
                users = new Users();
                users.setUserid(rs.getInt("userid"));
                users.setUsername(rs.getString("username"));
                users.setUserage(rs.getInt("userage"));
            }
        }catch (Exception e){
            e.printStackTrace();
            // 通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally {
            JdbcDruidUtils.closeResource(rs,ps,conn);
        }
        return users;
    }
}
```

UserService接口

```java
import com.itshihao.pojo.Users;

public interface UsersService {
    Users findUsersById(int userid);
}
```

UserServiceImpl接口实现类

```java
import com.itshihao.dao.UserDao;
import com.itshihao.dao.impl.UserDaoImpl;
import com.itshihao.pojo.Users;
import com.itshihao.service.UsersService;

public class UserServiceImpl implements UsersService {
    /**
     * 根据用户ID查询用户业务
     * @param userid
     * @return
     */
    @Override
    public Users findUsersById(int userid) {
        UserDao ud = new UserDaoImpl();
        return ud.selectUsersById(userid);
    }
}
```

web

```java
import com.itshihao.pojo.Users;
import com.itshihao.service.UsersService;
import com.itshihao.service.impl.UserServiceImpl;

public class Test {
    public static void main(String[] args) {
        UsersService us = new UserServiceImpl();
        Users u = us.findUsersById(1);
        System.out.println(u);
    }
}
```

## IV、封装通用的BaseDao

### 封装通用的DML操作

BaseDao接口

```java
/**
 * 通用接口
 */
public interface BaseDao {
    /**
     * 通用的DML操作方法
     */
    int executeUpdate(String sql,Object[] param);
}
```

BaseDaoImpl接口实现类

```java
/**
 * 通用接口实现类
 */
public class BaseDaoImpl implements BaseDao {
    /**
     * 通用的DML操作方法
     */
    @Override
    public int executeUpdate(String sql, Object[] param) {
        Connection conn = null;
        PreparedStatement ps = null;
        int row;
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement(sql);
            //得到参数的个数
            ParameterMetaData pd = ps.getParameterMetaData();
            for(int i =0;i<pd.getParameterCount();i++){
                ps.setObject(i+1,param[i]);
            }
            row = ps.executeUpdate();
        }catch (Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(ps,conn);
        }
        return row;
    }
}

```

UsersDao接口

```java
public interface UsersDao extends BaseDao {
    /**
     * 根据用户ID查询用户
     *
     */
    Users selectUsersById(int userid);


    /**
     * 修改用户信息
     */
    int updateUsersById(Users users);
}



```

UsersDaoImpl接口实现类

```java
public class UsersDaoImpl extends BaseDaoImpl implements UsersDao {
    /**
     * 根据用户ID查询用户
     * @param userid
     * @return
     */
    @Override
    public Users selectUsersById(int userid) {
        Connection conn =null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        Users users = null;
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement("select * from users where userid = ?");
            ps.setInt(1,userid);
            rs = ps.executeQuery();
            while(rs.next()){
                //手动orm映射
                users = new Users();
                users.setUserid(rs.getInt("userid"));
                users.setUsername(rs.getString("username"));
                users.setUserage(rs.getInt("userage"));
            }
        }catch(Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(rs,ps,conn);
        }
        return users;
    }
    /**
     * 修改用户信息
     */
    @Override
    public int updateUsersById(Users users) {
        String sql = "update users set userage = ? where userid = ? ";
        Object[] param = new Object[]{users.getUserage(),users.getUserid()};
        return this.executeUpdate(sql,param);
    }
}

```

UsersService接口

```java
import com.itshihao.pojo.Users;

public interface UsersService {
    Users findUsersById(int userid);
    int modifyUsersById(Users users);
}
```

UserServiceImpl实现类

```java
public class UserServiceImpl implements UsersService {
    /**
     * 根据用户ID查询用户业务
     * @param userid
     * @return
     */
    @Override
    public Users findUsersById(int userid) {
        UserDao ud = new UserDaoImpl();
        return ud.selectUsersById(userid);
    }

    @Override
    public int modifyUsersById(Users users) {
        UserDao ud = new UserDaoImpl();
        return ud.updateUsersById(users);
    }
}
```

Web：

```java
public class Test2 {
    public static void main(String[] args) {
        UsersService us = new UserServiceImpl();
        Users users = new Users();
        users.setUserage(23);
        users.setUserid(3);
        int i = us.modifyUsersById(users);
        System.out.println(i);
    }
}
```





### 封装通用的查询操作

BaseDao接口

```java
/**
 * 通用接口
 */
public interface BaseDao {
    /**
     * 通用的DML操作方法
     */
    int executeUpdate(String sql,Object[] param);


    /**
     * 通用查询方法
     * 要求：实体类的属性名必须要与表的列名相同。
     */
    <T> List<T> select(String sql,Object[] param,Class<T> clazz);
}

```

BaseDaoImpl接口实现类

```java
/**
 * 通用接口实现类
 */
public class BaseDaoImpl implements BaseDao {
    /**
     * 通用的DML操作方法
     */
    @Override
    public int executeUpdate(String sql, Object[] param) {
        Connection conn = null;
        PreparedStatement ps = null;
        int row;
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement(sql);
            //得到参数的个数
            ParameterMetaData pd = ps.getParameterMetaData();
            for(int i =0;i<pd.getParameterCount();i++){
                ps.setObject(i+1,param[i]);
            }
            row = ps.executeUpdate();
        }catch (Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(ps,conn);
        }
        return row;
    }


    /**
     * 通用查询方法
     */
    @Override
    public <T> List<T> select(String sql, Object[] param, Class<T> clazz) {
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        List<T> list = new ArrayList<>();
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement(sql);
            //得到参数的个数
            ParameterMetaData pd = ps.getParameterMetaData();
            for(int i =0;i<pd.getParameterCount();i++){
                ps.setObject(i+1,param[i]);
            }
            rs = ps.executeQuery();
            //获取结果集信息
            ResultSetMetaData rm = rs.getMetaData();
            while(rs.next()){
                //OMR映射
                //通过反射实例化实体类对象
              T bean = clazz.newInstance();
              //实体类的属性名必须要和表的列名相同。
                for(int i=0;i<rm.getColumnCount();i++){
                    //得到列名
                    String columnName = rm.getColumnName(i+1);
                    //获取列的值
                    Object value = rs.getObject(columnName);
                    //通过BeanUtil工具类讲值映射到对象中
                    BeanUtils.setProperty(bean,columnName,value);
                }
                list.add(bean);
            }


        }catch (Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(rs,ps,conn);
        }
        return list;
    }
}

```

UsersDao接口

```java
public interface UsersDao extends BaseDao {
    /**
     * 根据用户ID查询用户
     *
     */
    Users selectUsersById(int userid);


    /**
     * 修改用户信息
     */
    int updateUsersById(Users users);


    /**
     * 根据用户姓名模糊查询
     */
    List<Users> selectUsersByLikeName(String username);
}



```

UsersDaoImpl接口实现类

```java
public class UsersDaoImpl extends BaseDaoImpl implements UsersDao {
    /**
     * 根据用户ID查询用户
     * @param userid
     * @return
     */
    @Override
    public Users selectUsersById(int userid) {
        Connection conn =null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        Users users = null;
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement("select * from users where userid = ?");
            ps.setInt(1,userid);
            rs = ps.executeQuery();
            while(rs.next()){
                //手动orm映射
                users = new Users();
                users.setUserid(rs.getInt("userid"));
                users.setUsername(rs.getString("username"));
                users.setUserage(rs.getInt("userage"));
            }
        }catch(Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(rs,ps,conn);
        }
        return users;
    }
    /**
     * 修改用户信息
     */
    @Override
    public int updateUsersById(Users users) {
        String sql = "update users set userage = ? where userid = ? ";
        Object[] param = new Object[]{users.getUserage(),users.getUserid()};
        return this.executeUpdate(sql,param);
    }

    /**
    根据用户名查询用户
    */
    @Override
    public List<Users> selectUsersByLikeName(String username) {
        String sql = "select * from users where username like ?";
        Object[] param = new Object[]{"%"+username+"%"};
        return this.select(sql,param,Users.class);
    }
}

```

UsersService接口：

```java
public interface UsersService {
    Users findUsersById(int userid);
    int modifyUsersById(Users users);
    List<Users> findUsersByLikeName(String username);
}
```

UsersServiceImpl实现类：

```java
public class UserServiceImpl implements UsersService {
    /**
     * 根据用户ID查询用户业务
     * @param userid
     * @return
     */
    @Override
    public Users findUsersById(int userid) {
        UserDao ud = new UserDaoImpl();
        return ud.selectUsersById(userid);
    }

    @Override
    public int modifyUsersById(Users users) {
        UserDao ud = new UserDaoImpl();
        return ud.updateUsersById(users);
    }

    @Override
    public List<Users> findUsersByLikeName(String username) {
        UserDao ud = new UserDaoImpl();
        return ud.selectUsersByLikeName(username);
    }
}
```

Web:

```java
public class Test3 {
    public static void main(String[] args) {
        UsersService us = new UserServiceImpl();
        List<Users> list = us.findUsersByLikeName("l");
        for (Users users : list) {
            System.out.println(users);
        }
    }
}
```

# 二十五、对象的关联关系

![image-20220313145357369](https://www.itbaizhan.com/wiki/imgs/image-20220313145357369-16471544383304.png)

## I、关联关系简介

关联关系(Association)，是一种拥有的关系，它使一个对象知道另一个对象的属性和方法。关联可以是双向的，也可以是单向的。在Java语言中，关联关系一般使用成员变量来实现。



**对象的关联关系解决了什么问题**

在多表查询时，使用对象关联关系能够更合理的存放查询到的结果集数据。

**关联关系的方向性**

- 单向

  只在一侧关联了对方。

- 双向

  两侧相互关联了对方。

**实时效果反馈**

**1. 关联关系在代码中一般使用来实现。**

A 成员变量

B 局部变量

C 方法

D 静态块

**答案**

1=>A

## II、使用对象关联关系存放查询数据

需求：查询用户ID为1的用户信息他的订单信息，以及订单中所包含的商品信息。

SQL语句

```sql
select * 
from users u,orders o, orders_items oi, items i 
WHERE u.userid = o.user_id 
	and o.orderid = oi.order_id 
	and oi.item_id = i.itemid 
	and u.userid =1;
```

UserDao接口

```java
public interface UserDao extends BaseDao{
 
    /**
     * 查询用户ID为1的用户信息和它的订单信息
     * 以及订单中所包含的商品信息
     */
    Users selectUsers(int userid);
}
```

UsersDaoImpl接口实现类

```java
public class UserDaoImpl extends BaseDaoImpl implements UserDao { 
/**
     * 查询用户ID为1的用户信息他的订单信息，
     * 以及订单中所包含的商品信息。
     */
    @Override
    public Users selectUsers(int userid) {
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet rs = null;
        Users users =new Users();
        try{
            conn = JdbcDruidUtil.getConnection();
            ps = conn.prepareStatement("select * from users u,orders o, orders_items oi, items i WHERE\n" +
                    "u.userid = o.user_id and o.orderid = oi.order_id and oi.item_id = i.itemid \n" +
                    "and u.userid =?");
            ps.setInt(1,userid);
            rs = ps.executeQuery();
            while(rs.next()){
                //Users对象的ORM映射
                users.setUserid(rs.getInt("userid"));
                users.setUsername(rs.getString("username"));
                users.setUserage(rs.getInt("userage"));


                //Orders对象的ORM映射
                Orders orders = new Orders();
                orders.setOrderid(rs.getInt("orderid"));
                orders.setOrderprice(rs.getDouble("orderprice"));
                users.getOrders().add(orders);


                //Items对象的ORM映射
                Items items = new Items();
                items.setItemid(rs.getInt("itemid"));
                items.setItemname(rs.getString("itemname"));
                items.setItemprice(rs.getDouble("itemprice"));
                items.setItemnum(rs.getInt("itemnum"));
                orders.getItems().add(items);
            }
        }catch (Exception e){
            e.printStackTrace();
            //通过自定义异常解决异常耦合问题
            throw new ApplicationException(e.getMessage());
        }finally{
            JdbcDruidUtil.closeResource(rs,ps,conn);
        }
        return users;
    }
}
```

UsersService接口

```java
public interface UsersService {
    Users findUsers(int userid);
}
```

UsersService接口实现类

```java
  public class UserServiceImpl implements UsersService {
    @Override
    public Users findUsers(int userid) {
        UserDao ud = new UserDaoImpl();
        return ud.selectUsers(userid);
    }
}
```

Web：

```java
import com.itshihao.pojo.Items;
import com.itshihao.pojo.Orders;
import com.itshihao.pojo.Users;
import com.itshihao.service.UsersService;
import com.itshihao.service.impl.UserServiceImpl;

import java.util.List;

public class Test4 {
    public static void main(String[] args) {
        UsersService us = new UserServiceImpl();
        Users users = us.findUsers(1);
        System.out.println("Users:" + users.getUserid() + " " + users.getUsername() + " " + users.getUserage());
        List<Orders> list = users.getOrders();
        for (Orders orders : list) {
            System.out.println("Orders:" + orders.getOrderid() + " " + orders.getOrderprice());
            List<Items> items = orders.getItems();
            for (Items item : items) {
                System.out.println("Items:" + item.getItemid() + " " + item.getItemname() + " " + item.getItemprice() + " " + item.getItemnum());
            }
        }
    }
}
```











