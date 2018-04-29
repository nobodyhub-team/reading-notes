# Chapter 1: 概述

## 大型网站软件系统的特点
* 高并发, 大吞吐(High Concurrency, Large Throughput)
* 高可用(High Availability)
* 海量数据(Massive Data)
* 用户分布广泛, 网络情况复杂(Widely Distributed Users and Complex Network Conditions)
* 安全环境恶劣(Poor Security Environment)
* 需求快速变更, 发布频繁(Rapidly Changed Requirement and Frequent Release)
* 渐进式发展(Progressive Development)

## 大型网站架构演化发展历程
```
应用服务器
-------
+ 文件服务器
+ 数据库服务器
-------
+ 分布式缓存服务器
+ 应用服务器本地缓存
-------
+ 集群应用服务器
+ 负载均衡服务器
-------
+ 数据库主服务器(写)
+ 数据库从服务器(读)
-------
+ 反向代理服务器
+ CDN服务器
-------
+ 分布式文件系统
+ 分布式数据库系统
-------
+ NoSQL
+ 搜索引擎
-------
+ 拆分业务应用服务器
+ 消息队列服务器
-------
+ 分布式服务
```

## 大型网站架构演化的价值观
* 大型网站架构技术的核心价值: 随网站所需灵活应对
* 驱动大型网站技术发展的主要力量: 业务发展
