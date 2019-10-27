---
layout: post
title: "knowledge"
subtitle:   " \"PHP technology stack backend knowledge reserve warehouse\""
date:       2018-11-26 09:10:00
author:     "吴庆宝"
header-img: "img/post-bg-2015.jpg"
catalog: true
tags:
    - 知识
    - php
---

> php技术栈后端程序员的知识储备仓库

## 前言

基础不牢，地动山摇，谨以此句提醒自己。

## 备注

状态        | 含义
--------- | -------
not-start | 当前未开始总结
doing     | 总结中
α         | 目前仅供参考未修正和发布
done      | 总结完毕
fixing    | 查漏补缺修改中

## 目录

- PHP基础学习(done)

  - 符合PSR的PHP编程规范

    - [实例](/2018/11/27/PHP-technical-examples)
    - [文档](/2018/11/27/PHP-coding-specifications-and-recommendations)
    - [经验](/2018/11/27/PHP-experience)

  - 基础知识[读(R)好(T)文(F)档(M)]
    - [数据类型](http://php.net/manual/zh/language.types.php)

    - [运算符优先级](http://php.net/manual/zh/language.operators.precedence.php)
    - [string函数](http://php.net/ref.strings.php)
    - [array函数](http://php.net/manual/zh/ref.array.php)
    - [math函数](http://php.net/manual/zh/ref.math.php)
    - [面向对象](http://php.net/manual/zh/language.oop5.php)
    - 版本新特性

      - [7.2](http://php.net/manual/zh/migration72.new-features.php)
      - [7.1](http://php.net/manual/zh/migration71.new-features.php)
      - [7.0](http://php.net/manual/zh/migration70.new-features.php)
      - [5.6](http://php.net/manual/zh/migration56.new-features.php)
      - [5.5](http://php.net/manual/zh/migration55.new-features.php)
      - [5.4](http://php.net/manual/zh/migration54.new-features.php)
      - [5.3](http://php.net/manual/zh/migration53.new-features.php)
       
- PHP深入学习(doing)
 
- 网络编程(doing)

- 问题排查(doing)
 
- Mysql(doing)

  - [常用sql语句](/2018/11/29/Common-sql-statement) 
  - [引擎](/2018/11/29/Mysql-engine)  
  - [事务](/2018/11/29/Mysql-engine#事务)    
  - [索引](/2018/11/29/Mysql-engine#索引)    
    + 建立表结构时添加的索引
      * 主键唯一索引
      * 唯一索引
      * 普通索引
      * 联合索引
        - 最左匹配原则
    + 依据是否聚簇区分
      * 聚簇索引
      * 非聚簇索引
    + 索引底层数据结构
      * hash索引
      * b-tree索引
      * b+tree索引
    
  - [锁](/2018/11/29/Mysql-engine#锁)     
    - 悲观锁
    - 乐观锁
  - 分表
    - 垂直分表
    - 水平分表
  - sql优化
  - 主从配置

- Redis(doing)
  - 常用命令
  - 实现原理&与memcache区别
  - 常见用途
    - [缓存](/2018/12/03/Redis-Cache) 
    - [队列](/2018/12/03/Redis-queue) 
    - [悲观锁](/2018/12/03/Redis-pessimistic-lock) 
    - [乐观锁](/2018/12/03/Redis-optimistic-lock) 
    - [订阅/推送](/2018/12/03/Redis-subscribe-publish) 
  - 常见业务实际使用
  - redis的基础数据结构

- Docker(doing)
  - [redis主从搭建]
  - [mysql主从搭建]
  - [codis环境]
  - mysql多主环境
  - kafka的环境搭建和使用
  - rabbitMQ的环境搭建和使用
  - zookeeper的环境搭建和使用
  - etcd的环境搭建和使用
  - ELK的环境搭建和使用
  - 网关服务kong的环境搭建和使用
  - 我所理想的架构

- 设计模式(done/fixing)

  - [概念]

  - 创建型模式实例

    - [单例模式] 
    - [工厂模式] 
    - [抽象工厂模式]
    - [原型模式]
    - [建造者模式]

  - 结构型模式实例

  - 行为型模式实例


- [数据结构(doing)]

  - 数组
  - 堆/栈
  - 树
  - 队列
  - 链表
  - 图
  - 散列表

- 算法(doing)

  - 算法分析

    - 时间复杂度/空间复杂度/正确性/可读性/健壮性

  - 算法实战

    - 排序算法(α)

      - [冒泡排序](/2018/11/26/PHP-algorithms-practice-bubble) 
      - [快速排序](/2018/11/26/PHP-algorithms-practice-quick-sort)
      - [选择排序](/2018/11/28/PHP-algorithms-practice-select) 
      - [插入排序](/2018/11/28/PHP-algorithms-practice-insert) 
      - [归并排序](/2018/11/28/PHP-algorithms-practice-merge) 
      - [希尔排序](/2018/11/28/PHP-algorithms-practice-shell) 
      - [基数排序](/2018/11/28/PHP-algorithms-practice-radix) 

- 网络基础(doing)

  - [互联网协议概述](/2018/11/30/Internet-protocol)
  - [client和nginx简易交互过程](/2018/11/30/Internet-protocol-simple-interaction-process) 
  - [nginx和php-fpm简易交互过程](/2018/11/30/Internet-protocol-simple-interaction-process)
  - [http](/2018/11/30/HTTP-concept) 
    - 报文
      - 报文头部
      - 报文体
    - 常见13种状态码
    - 方法method
    - https
    - http2
    - websocket

- 计算机基础(doing)

  - [linux常用命令](/2018/11/29/Linux-common-command) 
  - shell

- 高并发相关(not-start)

---

## PHP基础学习
[php.net](http://php.net/manual/zh/)

[慕课网](https://www.imooc.com/course/list?c=php)
```
composer install
php -S localhost:8000
# 浏览器
http://localhost:8000/php/index.php
# 命令行
php index.php
```

### 符合PSR的PHP编程规范
[PHP 标准规范](https://psr.phphub.org/)

#### [实例](/2018/11/27/PHP-technical-examples)

#### [文档](/2018/11/27/PHP-coding-specifications-and-recommendations)

#### [经验](/2018/11/27/PHP-experience)

## Mysql

### [常用sql语句](/2018/11/29/Common-sql-statement) 

### [引擎](/2018/11/29/Mysql-engine)  

### [事务](/2018/11/29/Mysql-engine#事务)   

### [索引](/2018/11/29/Mysql-engine#索引) 

### [锁](/2018/11/29/Mysql-engine#锁)  

## [Redis](/tags/#redis)

### 常见用途 
 