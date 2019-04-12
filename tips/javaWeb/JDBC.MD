## 数据库的类型
- 文件型数据库，SQLite
- 关系型数据库(SQL 数据库)，Oracle, MySQL, SQLServer
- NoSQL 数据库，Redis, HBase, MongoDB

## MySQL www.mysql.com
- 传统的关系型数据库（RDS）
- 支持千万级数据量 -> orcal -> BigData
- 免费开源，中小企业首选
- 支持多个操作系统 Linux / Windows

Enterprise 版（收费版）
Community 版 （免费版，GPL 授权）

## 命令行工具
在 bin 目录下面有一些命令行工具，
- `mysqladmin` : MySQL 服务器管理工具
- `mysql` : MySQL 客户端连接工具
- `mysqldump` : ...

```
// 每条语句后面都加分号
// 连接到服务器 host=127.0.0.1 用户名root，密码为空
mysql.exe -h 127.0.0.1 -u root
// 切换到 test 数据库
> use test; 
// 从 example 表中选择
> select * from example;
// 退出
> quit;
```

## 常用的客户端工具
- mysql.exe MySQL 自带，命令行界面
- SQLyog
- Navicat 

## SQL (Structured Query Language) 的写法
SQL 语句：客户端用来操作数据库的语句
1. 创建数据库 ` CREATE DATABASE af_sample; `
2. 删除数据库 ` DROP DATABASE af_sample; `
3. 切换数据库 ` USE af_sample;`

## 创建表
```sql
DROP TABLE IF EXISTS `student`;
CREATE TABLE `student` (
    `id` int(11) NOT NULL COMMENT `学号`,
    `name` varchar(64) NOT NULL COMMENT `姓名`,
    `phone` varchar(16) NOT NULL COMMENT `电话`,
    `birthday` date DEFAULT NULL COMMENT `生日`,
    PRIMARY KEY(`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf-8;

```

## SQL 插入语句
```sql
USE af_sample.`student`

INSERT INTO `student`
	( `id`, `name`, `phone`, `birthday` )
VALUES
	( "20180002", "杨志立", "13008800699", "1990-02-07" )
```

