# 关于

每次想要找工作, 都得重新准备面试相关的知识点.
说明之前每次准备过程的结果没有很好的整理下来.
以后都要学乖, 所有整理的内容都应该要形成文字.
未来还可以整理到自己的对话机器人中.

当然, 这个提纲主要为个人服务, 带有鲜明的个人性.

- [更新随笔](/docs/thoughts.md)

# 职业理解

现在的业界往往以开发语言作为职业方向. 这是不对的.
开发语言只是一种工具, 君子不器.
关键在于开发者通过工具进入了哪一种开发领域,
需要具备怎样的技能, 又获得了怎样的开发能力.

我个人的经验主要在服务端开发, 使用语言 PHP/JS/Java, 最熟悉 PHP.
工作内容偏向于互联网业务.
这里主要记录互联网服务端业务的知识点.

# 职业规划

尽管行业仍然以语言作为开发技能的划分, 但个人立场应该有超越语言的成长方向.
我个人考虑主要有以下几个方向:

- 语言底层: 围绕语言工具本身开发, 例如 PHP 新版本/特性, 或 Swoole 这类能扩展生态的插件
- 工程架构: 为某种业务类型开发通用的架构工具, 包括 Laravel 这类全栈框架, 或者 PRedis 这样的包.
- 基础架构: 业务往往涉及多个领域, 需要针对业务特点设计跨领域的架构. 例如 Web/即时通讯/视频直播等, 对业务对接/通讯协议/高可用/性能 等有不同的要求.
- 业务专精: 对某一个具体的业务形态有充分的认识, 并给出解决方案; 比如支付/打车/运营活动/交易流程 等.
- 开发管理: 结合以上几个方向的知识, 但偏重于管理本身

个人的 [CommuneChatbot](https://github.com/thirdgerb/chatbot) 项目偏重于以下三个方向:

- 工程架构
- 基础架构
- 业务专精

# 知识要点提纲

这里记录一些我个人更重视的知识点, 随手更新.

提纲本身是一个知识结构, 结构树会不断更新, 每个节点内容需要掌握细节, 不断积累.
但相关链接只打算记录和面试有关的要点.

相信会有许多阶段性的认识错误, 希望在学习和工作中不断改进.


## Web 开发

+ 操作系统
    + 防火墙
    + 用户权限管理
    + 包管理
+ 网络通信
    + [IP](interview/network_ip.md)
    + DNS
    + [TCP](interview/network_tcp.md)
    + UDP
    + Http
        + KeepAlive
        + Https
    + Http 2.0
    + [CGI & Fast-cgi]((interviw/network_cgi.md))
+ 常用工具
    + 服务搭建
        + Linux 主从
        + [Nginx](interview/tools_nginx.md)
    + 非关系型数据库
        + Redis
        + MongoDB
        + HBase
    + 关系型数据库
        + [Mysql](/interview/database_mysql.md)
    + 图数据库
        + Neo4j
    + 搜索
        + ElasticSearch
    + 消息中间件
        + Redis
        + Kafka
        + RabbitMQ
    + 监控工具
        + ELK
        + Open-falcon
        + Sentry
    + 网关
        + Kong
    + 分布式配置
        + ZooKeeper
        + Etcd
    + 容器化
        + Docker
        + K8S
+ 数据格式
    + json
    + protobuf
+ 规范
    + OAuth 2
    + Restful
    + GraphQL
    + JsonAPI
    + JWT

## 功能模块

+ IoC容器与依赖注入
+ 任务队列
+ 定时任务
+ 原子化操作
+ 状态机
+ 事件机制

## 业务架构

+ 订单 & 支付
+ 运营活动
+ CMS
+ 物联网
+ 商城
+ 用户增长
    + AB 测试系统
+ 召回
+ 即时通讯

## 基础架构

+ 应用架构
    + 微服务
    + 网关
    + 监控
        + 监控数据存储
        + 链路追踪
        + 异常追踪
        + 服务器监控
    + 通信
        + 协议
            + RPC
    + 任务管理
    + CDN
+ 数据库知识
    + 分库分表
    + 事务
    + 索引
    + 集群
    + 高可用
    + 容灾
+ 运维思路
    + 容器化部署
    + 自动化部署


## PHP

+ PHP 基础
    + [语法要点](/interviw/php_lang.md)
    + [PHP-FPM](/interview/php_fpm.md)
    + [PHP 生命周期](/interview/php_lifecircle.md)
    + 重要参数
    + 数据结构
+ [常用扩展](/interview/php_modules.md)
    + Opcache 原理
    + Xdebug
    + PDO
    + Xprof
    + APC
+ Swoole
+ 开发框架
    + Laravel
    + Swoole 协程框架
        + Hyperf
        + Swoft
        + EasySwoole
    + 经典框架
        + Yii
        + CI
        + Yaf
        + ThinkPHP
+ 常用包
    + Composer
    + Symfony
+ 框架技术要点
    + 通信模型
    + 生命周期规划
    + IoC 容器与依赖注入
    + 配置化/组件化
    + 异常体系


## 算法 & 数据结构 应用

算法和数据结构主要还是放在具体的应用场景中才有意义.
这里更新的主要和应用场景相关.

- 面试专用算法
    - 排序算法
    - 树操作
- 哈希算法
    - 雪花算法
- 加密算法
- 搜索技术
    - 哈夫曼树
    - 倒排索引
    - 词频算法
- 集群
    - 选举算法
    - 一致性 Hash

## 开发管理

+ 迭代策略
+ 发布策略
+ 版本控制
    + git
+ 自动化测试
    + 代码自动化测试
    + 架构自动化测试
+ 代码质量管理
+ 压力测试


