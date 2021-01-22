# 如何使用

切换用户
su - gpadmin  

执行命令行
psql
查看帮助
\h
创建数据库
create database idis;
查看数据库
\l
创建表
create table test(id int primary key,name varchar(128));
插入数据
insert into test values (1,'111');
查看数据
select * from test;
查看表结构
 \dt
 
## 实例代码
``` 
[root@greenplum-n4hrq /]# su - gpadmin  
-bash-4.1$ psql
psql (8.2.15)
Type "help" for help.

gpadmin=# create database idis;
CREATE DATABASE
gpadmin=# create table test(id int primary key,name varchar(128));
NOTICE:  CREATE TABLE / PRIMARY KEY will create implicit index "test_pkey" for table "test"
CREATE TABLE
gpadmin=# insert into test values (1,'111');
INSERT 0 1
gpadmin=# select * from test;
 id | name 
----+------
  1 | 111
(1 row)

gpadmin=#  \dt
             List of relations
 Schema | Name | Type  |  Owner  | Storage 
--------+------+-------+---------+---------
 public | test | table | gpadmin | heap
(1 row)

gpadmin=#  
```