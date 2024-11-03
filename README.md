

## 一、项目简介

PmHub 包括认证、流程、项目管理、用户、网关等服务。包含了 Redis 缓存、RocketMQ 消息队列、Docker 容器化、Jenkins 自动化部署、Spring Security 安全框架、Nacos 服务注册和发现、Sentinel 熔断限流、Seata 分布式事务、Spring Boot Actuator 服务监控、SkyWalking 链路追踪、OpenFeign 服务调用，Vue3 前端框架等互联网开发中需要用到的主流技术栈，可以帮助同学们快速掌握微服务/分布式项目的核心知识点。

并且同时 PmHub 也是一套企业工作流的开发框架，您可以根据自身需求，快速定制出适合自己公司的企业工作流系统。





## 三、项目详情
### 3.1、技术架构

下面这张系统架构图可以帮助大家快速了解 PmHub 项目的系统架构，从前端到网关、从服务应用到基础服务组件、从存储技术到运维部署，可以说是一目了然。

![pmhub-系统架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240708113736.png)

下面这张架构选型图可以帮助大家快速了解 PmHub 项目的技术选型，以及在[官方手册](https://laigeoffer.cn/pmhub/tech-architecture/)中会更详细的说明我们为什么选择该技术，毕竟授人以鱼不如授人以渔嘛。

![pmhub-架构选型](https://cdn.tobebetterjavaer.com/stutymore/PmHub%E6%9E%B6%E6%9E%84%E9%80%89%E5%9E%8B.png)

下面这张技术架构图可以帮助大家快速了解 PmHub 项目的技术架构，以及各个模块之间的交互关系。

![pmhub-技术架构图](https://cdn.tobebetterjavaer.com/stutymore/01.什么是PmHub-20240702103552.png)

优质的项目，离不开一张清晰的鸟瞰图（😄）。

### 3.2、项目演示

![首页展示](https://cdn.tobebetterjavaer.com/stutymore/20240407163006.png)
![项目概览页](https://cdn.tobebetterjavaer.com/stutymore/202404071500496.png)
![任务编辑页](https://cdn.tobebetterjavaer.com/stutymore/20240407163256.png)
![PmHub表单设计](https://cdn.tobebetterjavaer.com/stutymore/1719456780250-d60beb66-7cd3-4dc5-95c1-893d364ab56a.png)
![PmHub流程设计页面](https://cdn.tobebetterjavaer.com/stutymore/1719458145592-0d855810-b4ca-44c8-a8cc-04b1ac4baa2d.png)

### 3.3、代码展示
![pmhub代码展示](https://cdn.tobebetterjavaer.com/stutymore/20240529152747.png)

### 3.4、代码结构

```
com.laigeoffer.pmhub     
├── pmhub-ui              // 前端框架 [1024]
├── pmhub-gateway         // 网关模块 [6880]
├── pmhub-auth            // 认证中心 [6800]
├── pmhub-api             // 接口模块
│       └── pmhub-api-system                          // 系统接口
│       └── pmhub-api-workflow                        // 流程接口
├── pmhub-base          // 通用模块
│       └── pmhub-base-core                           // 核心模块组件
│       └── pmhub-base-datasource                     // 多数据源组件
│       └── pmhub-base-seata                          // 分布式事务组件
│       └── pmhub-base-security                       // 安全模块组件
│       └── pmhub-base-swagger                        // 系统接口组件
│       └── pmhub-base-notice                         // 消息组件组件
├── pmhub-modules         // 业务模块
│       └── pmhub-system                              // 系统模块 [6801]
│       └── pmhub-gen                                 // 代码生成 [6802]
│       └── pmhub-job                                 // 定时任务 [6803]
│       └── pmhub-project                             // 项目服务 [6806]
│       └── pmhub-workflow                            // 流程服务 [6808]
├── pmhub-monitor             						  // 监控中心 [6888]                 
├──pom.xml                                            // 公共依赖
```





## 四、技术选型

后端技术栈

|         技术          | 说明                   | 官网                                                                                                                         |
|:-------------------:|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Spring & SpringMVC  | Java全栈应用程序框架和WEB容器实现 | [https://spring.io/](https://spring.io/)                                                                                   |
|     SpringBoot      | Spring应用简化集成开发框架     | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                                           |
|     SpringCloud     | 微服务框架                | [https://spring.io/projects/spring-cloud](https://spring.io/projects/spring-cloud)                                         |
|    mybatis-plus     | 数据库orm框架             | [https://baomidou.com/](https://baomidou.com/)                                                                             |
| mybatis PageHelper  | 数据库翻页插件              | [https://github.com/pagehelper/Mybatis-PageHelper](https://github.com/pagehelper/Mybatis-PageHelper)                       |
|    elasticsearch    | 近实时文本搜索              | [https://www.elastic.co/cn/elasticsearch/service](https://www.elastic.co/cn/elasticsearch/service)                         |
|        redis        | 内存数据存储               | [https://redis.io](https://redis.io)                                                                                       |
|      rocketmq       | 消息队列                 | [https://rocketmq.apache.org/](https://rocketmq.apache.org/)                                                               |
|       mongodb       | NoSql数据库             | [https://www.mongodb.com/](https://www.mongodb.com/)                                                                       |
|        nginx        | 服务器                  | [https://nginx.org](https://nginx.org)                                                                                     |
|       docker        | 应用容器引擎               | [https://www.docker.com](https://www.docker.com)                                                                           |
|      hikariCP       | 数据库连接                | [https://github.com/brettwooldridge/HikariCP](https://github.com/brettwooldridge/HikariCP)                                 |
|         oss         | 对象存储                 | [https://help.aliyun.com/document_detail/31883.html](https://help.aliyun.com/document_detail/31883.html)                   |
|        https        | 证书                   | [https://letsencrypt.org/](https://letsencrypt.org/)                                                                       |
|         jwt         | jwt登录                | [https://jwt.io](https://jwt.io)                                                                                           |
|       lombok        | Java语言增强库            | [https://projectlombok.org](https://projectlombok.org)                                                                     |
|        guava        | google开源的java工具集     | [https://github.com/google/guava](https://github.com/google/guava)                                                         |
|      thymeleaf      | html5模板引擎            | [https://www.thymeleaf.org](https://www.thymeleaf.org)                                                                     |
|       swagger       | API文档生成工具            | [https://swagger.io](https://swagger.io)                                                                                   |
|     quick-media     | 多媒体处理                | [https://github.com/liuyueyi/quick-media](https://github.com/liuyueyi/quick-media)                                         |
|      liquibase      | 数据库版本管理              | [https://www.liquibase.com](https://www.liquibase.com)                                                                     |
|       jackson       | json/xml处理           | [https://www.jackson.com](https://www.jackson.com)                                                                         |
|      ip2region      | ip地址                 | [https://github.com/zoujingli/ip2region](https://github.com/zoujingli/ip2region)                                           |
|      websocket      | 长连接                  | [https://docs.spring.io/spring/reference/web/websocket.html](https://docs.spring.io/spring/reference/web/websocket.html)   |
|   sensitive-word    | 敏感词                  | [https://github.com/houbb/sensitive-word](https://github.com/houbb/sensitive-word)                                         |
|       chatgpt       | chatgpt              | [https://openai.com/blog/chatgpt](https://openai.com/blog/chatgpt)                                                         |



## 七、环境搭建

### 开发工具

|        工具        | 说明           | 官网                                                                                                                       | 
|:----------------:|--------------|--------------------------------------------------------------------------------------------------------------------------|
|       IDEA       | java开发工具     | [https://www.jetbrains.com](https://www.jetbrains.com)                                                                   |
|   visualstudio   | web开发工具      | [https://code.visualstudio.com/](https://code.visualstudio.com/)                                                         |
|      Chrome      | 浏览器          | [https://www.google.com/intl/zh-CN/chrome](https://www.google.com/intl/zh-CN/chrome)                                     |
|   ScreenToGif    | gif录屏        | [https://www.screentogif.com](https://www.screentogif.com)                                                               |
|     SniPaste     | 截图           | [https://www.snipaste.com](https://www.snipaste.com)                                                                     |
|     PicPick      | 图片处理工具       | [https://picpick.app](https://picpick.app)                                                                               |
|     MarkText     | markdown编辑器  | [https://github.com/marktext/marktext](https://github.com/marktext/marktext)                                             |
|       curl       | http终端请求     | [https://curl.se](https://curl.se)                                                                                       |
|     Postman      | API接口调试      | [https://www.postman.com](https://www.postman.com)                                                                       |
|     draw.io      | 流程图、架构图绘制    | [https://www.diagrams.net/](https://www.diagrams.net/)                                                                   |
|      Axure       | 原型图设计工具      | [https://www.axure.com](https://www.axure.com)                                                                           |
|     navicat      | 数据库连接工具      | [https://www.navicat.com](https://www.navicat.com)                                                                       |
|     DBeaver      | 免费开源的数据库连接工具 | [https://dbeaver.io](https://dbeaver.io)                                                                                 |
|      iTerm2      | mac终端        | [https://iterm2.com](https://iterm2.com)                                                                                 |
| windows terminal | win终端        | [https://learn.microsoft.com/en-us/windows/terminal/install](https://learn.microsoft.com/en-us/windows/terminal/install) |
|   SwitchHosts    | host管理       | [https://github.com/oldj/SwitchHosts/releases](https://github.com/oldj/SwitchHosts/releases)                             |


### 开发环境

|      工具       | 版本        | 下载                                                                                                                     |
|:-------------:|:----------|------------------------------------------------------------------------------------------------------------------------|
|      jdk      | 1.8+      | [https://www.oracle.com/java/technologies/downloads/#java8](https://www.oracle.com/java/technologies/downloads/#java8) |
|     maven     | 3.4+      | [https://maven.apache.org/](https://maven.apache.org/)                                                                 |
|     mysql     | 5.7+/8.0+ | [https://www.mysql.com/downloads/](https://www.mysql.com/downloads/)                                                   |
|     redis     | 5.0+      | [https://redis.io/download/](https://redis.io/download/)                                                               |
| elasticsearch | 8.0.0+    | [https://www.elastic.co/cn/downloads/elasticsearch](https://www.elastic.co/cn/downloads/elasticsearch)                 |
|     nginx     | 1.10+     | [https://nginx.org/en/download.html](https://nginx.org/en/download.html)                                               |
|   rocketmq    | 5.0.4+    | [https://www.rabbitmq.com/news.html](https://www.rabbitmq.com/news.html)                                               |
|    ali-oss    | 3.15.1    | [https://help.aliyun.com/document_detail/31946.html](https://help.aliyun.com/document_detail/31946.html)               |
|      git      | 2.34.1    | [http://github.com/](http://github.com/)                                                                               |
|    docker     | 4.10.0+   | [https://docs.docker.com/desktop/](https://docs.docker.com/desktop/)                                                   |
|    freessl    | https证书   | [https://freessl.cn/](https://freessl.cn/)                                                                             |

## 八、内置功能

1.  用户管理：用户是系统操作者，该功能主要完成系统用户配置。
2.  部门管理：配置系统组织机构（公司、部门、小组），树结构展现支持数据权限。
3.  岗位管理：配置系统用户所属担任职务。
4.  菜单管理：配置系统菜单，操作权限，按钮权限标识等。
5.  角色管理：角色菜单权限分配、设置角色按机构进行数据范围权限划分。
6.  字典管理：对系统中经常使用的一些较为固定的数据进行维护。
7.  参数管理：对系统动态配置常用参数。
8.  通知公告：系统通知公告信息发布维护。
9.  操作日志：系统正常操作日志记录和查询；系统异常信息日志记录和查询。
10. 登录日志：系统登录日志记录查询包含登录异常。
11. 在线用户：当前系统中活跃用户状态监控。
12. 定时任务：在线（添加、修改、删除)任务调度包含执行结果日志。
13. 代码生成：前后端代码的生成（java、html、xml、sql）支持CRUD下载 。
14. 系统接口：根据业务代码自动生成相关的api接口文档。
15. 服务监控：监视当前系统CPU、内存、磁盘、堆栈等相关信息。
16. 缓存监控：对系统的缓存信息查询，命令统计等。
17. 在线构建器：拖动表单元素生成相应的HTML代码。
18. 连接池监视：监视当前系统数据库连接池状态，可进行分析SQL找出系统性能瓶颈。




