# Mysql

## 面试常见要点

- B+ 树
- 数据表引擎
- 常用索引
- 锁
- 关联查询
- 容灾
- 高可用
- 分库分表
- 数据类型
- 字符集

## 引擎

- InnoDB
- MyISAM
- Memory
- Merge

## 锁

- 行锁
- 表锁
- 乐观锁

## 索引

### 常用索引

- Index
- Unique
- 空间索引
- 全文索引

### 长字段索引问题

> 在非常长的字段上建立索引影响性能
> innodb索引单字段（utf8）只能取前767bytes

### 相关命令

略

## 容灾

- 主从复制 : binlog
- 备份
- 日志恢复




## B+ 树

> 他们认为数据库索引采用B+树的主要原因是：B树在提高了IO性能的同时并没有解决元素遍历的我效率低下的问题，正是为了解决这个问题，B+树应用而生。B+树只需要去遍历叶子节点就可以实现整棵树的遍历。而且在数据库中基于范围的查询是非常频繁的，而B树不支持这样的操作或者说效率太低。


## 事务隔离级别

### 事务隔离要素(ACID)

1. 原子性（Atomicity）；事务开始后所有操作，要么全部做完，要么全部不做，不能停滞在中间环节。
1. 一致性（Consistency）：事务开始前和结束后，数据库的完整性约束没有被破坏。
1. 隔离性（Isolation）：同一时间，只允许一个事务请求同一数据，不同的事务之间彼此没有任何干扰。
1. 持久性（Durability）：事务完成后，事务对数据库的所有更新将被保存到数据库，不能回滚。

### 并发问题

- 脏读：事务B修改数据但未提交，事务A读数据，然后B回滚，则A读到的是脏数据。
- 不可重复读：事务A第一次读取数据，事务B修改数据提交，事务A第二次读数据，两次数据不一致。
- 幻读：事务A update表的全部行，事务B插入一行，事务A就会发现表中还有未修改的行。（一般加间隙锁）

### 事务隔离级别

- 读未提交
- 读已提交
- 可重复读
- 串行话

### InnoDB 锁

1. 共享锁: 读锁，读取操作创建的锁。一旦上锁，任何事物无法对其修改，但可以并发读取数据，也可以对此数据再加共享锁。
1. 排他锁: 又称写锁，如果事务对数据A加上排他锁后，则其他事物不可并发读取数据，也不能再对A加任何类型的锁。获准排他锁的事务既能读取数据，又能修改数据
1. 意向锁:

### MVCC 多版本并发控制

### 并发插入（Concurrent Inserts）

## 引用

* [1] [Mysql 事务隔离级别](https://www.cnblogs.com/chafanbusi/p/10657478.html)
* [2] [Mysql 中的锁详解](https://www.cnblogs.com/jpfss/p/8890250.html)
* [3] [Mysql 索引为什么选择B+树](https://www.cnblogs.com/tiancai/p/9024351.html)
* [4] [B树和B+树的区别](https://www.cnblogs.com/xueqiuqiu/articles/8779029.html)
* [5] [Mysql 表引擎的选择](https://www.cnblogs.com/jswang/p/6923911.html)
* [6] [Mysql 索引](https://www.cnblogs.com/Aiapple/p/5693239.html)
* [7] [Mysql 主从复制](https://www.cnblogs.com/jianmingyuan/p/10903682.html)
* [8] [Mysql 高可用方案对比](https://blog.csdn.net/yzj5208/article/details/81288436)