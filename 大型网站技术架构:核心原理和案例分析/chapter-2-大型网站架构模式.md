# Chapter 2: 大型网站架构模式

## 什么是模式
每一个模式描述了一个在我们周围不断重复发生问题及该问题解决方案的核心.
Each pattern describes a problem that recurs constantly around us and the core of the solution to that problem.

## 网站架构模式 
* 分层(横向)
* 分割(纵向)
* 分布式
    - 分布式应用和服务
    - 分布式静态资源
    - 分布式数据和存储
    - 分布式计算
* 集群
    - 负载均衡
    - 任意添加新服务器
* 缓存(前提: 数据访问热点不均衡和数据短时间内不失效)
    - CDN
    - 反向代理
    - 本地缓存
    - 分布式缓存
* 异步
    - 提高系统可用性
    - 加快网站相应速度
    - 消除并发高峰
* 冗余
* 自动化
    - 自动化代码管理
    - 自动化测试
    - 自动化安全监测
    - 自动化部署
    - 自动化监测
    - 自动化报警
    - 自动化失效转移
    - 自动化失效恢复
    - 自动化降级
    - 自动化分配资源
* 安全

[Home](README.md), [Previous](chapter-1-概述.md), [Next](chapter-3-大型网站核心要素.md)