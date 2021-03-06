# myDemo01

# 技术架构：
  1.Spring Boot + Spring Cloud + Spring Data整体搭建
  
  2.Redis + RabbitMQ + Elasticsearch 中间件
  
  3.MySQL 存储核心信息 + MongoDB 存储CMS配置信息 + Druid 连接池 
  
  4.Euereka 微服务注册与发现 + Feign 微服务远程调用
  
  5.Spring Security 用户认证授权 
  
  6.FastDFS分布式系统 图片服务器
  
# 项目描述：
  1.老师上传视频、更新课程信息
  
  2.学生选购课程、观看课程视频
  
  3.后台CMS系统管理页面布局
  
  4.社交系统方便学生与老师间的交流
 
 # 业务流程
 1、用户可以通过pc、手机等客户端访问系统进行在线学习。 
 
 2、 系统应用CDN技术，对一些图片、CSS、视频等资源从CDN调度访问。 
 
 3、所有的请求全部经过负载均衡器。 
 
 4、对于PC、H5等客户端请求，首先请求UI层，渲染用户界面。 
 
 5、客户端UI请求服务层获取进行具体的业务操作。 
 
 6、服务层将数据持久化到数据库。
  
# 各项职责
1、用户层 

  用户层描述了本系统所支持的客户端用户有哪些，本项目目前为各用户提供服务，包括H5、PC、Android和IOS 等。
  
2 CDN

  全称Content Delivery Network，即内容分发网络，本系统所有静态资源全部通过CDN加速来提高访问速 度。系统静态资源包括：html页面、js文件、css文件、image图片、pdf和ppt及doc教学文档、video视频等。
  
3 负载均衡 

   系统的CDN层、UI层、服务层及数据层均设置了负载均衡服务，系统采用LVS+Nginx实现负载均衡均 衡。
   
4 UI层 

   UI层描述了系统向pc用户、app用户、h5用户提供的产品界面。本项目在PC和H5端采用vue.js+elementUI 实现。
   
5 微服务层

   将系统服务分类三类：前端服务、后端服务及系统服务。 前端服务：主要为学习用户提供学习服务。 后端服务：主要为管理用户提供教学管理服务。 系统服务：公共服务，为系统的所有微服务提供公共服务功能。 
   
6 外部系统接口 

  包括如下接口： 
  
  1）第三方登录接口，如QQ、微博、微信等。
  
  2）支付宝、微信支付接口 
  
  3）短信接口 （阿里大于）
  
  4）邮件接 口，通过smpt邮件服务器对外发送电子邮件。 
  
  5）微信公众号 
  
  6）点播、直播。 
  
  7）OSS存储 
  
  8）CDN，使用最里 云CDN服务加速视频访问速度。 
  
7 DevOps提供了本系统开发、运营、维护支撑的系统，包括如下内容： 

  Eureka服务治理中心：提供服务治理服务，包括：服务注册、服务获取等。 
  
  Docker容器化部署服务：将本系统所有服务采用容器化部署方式。 
  
  Maven项目管理工具：提供管理项目所有的Java包依赖、项目工程打包服务。 
  
  Git/GitLab代码管理服务:提供git代码管理服务。 
  
  Spring Boot Admin服务健康监控：监控微服务的健康状态、会话数量、并发数等。
  
