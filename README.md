# RedSeaOSS非结构化对象存储平台

## 功能简介：
### 优点：
	独立服务：减少原有应用服务的请求连接压力，分解出文件上传与文件下载的服务器压力 
	非结构化存储：基于对象存储，⼀站式地完成日志处理、图片处理、文档、附件、⾳视频处理 
	开放性访问：通过RESTful API 可以在互联网任何位置存储和访问，容量和处理能力弹性扩展 
	异步消息日志持久化：保证高并发业务的可用性与可靠性
### 存储技术的优势：
	文件服务器致力于小型文件的存储，比如业务中图片、普通文档等。由于MongoDB 支持多种数据格式的存储，对于二进制的存储自然也是不
	在话下，所以可以很方便的用于存储文件。由于 MongoDB 的 BSON 文档对于数据量大小的限制（每个文档不超过16M），所以本文件服务
	器主要针对的是小型文件的存储。对于大型文件的存储（比如超过16M），MongoDB 官方已经提供了成熟的产品 GridFS
### 基本功能：
	针对当前业务系统中功能服务包含：头像、文件、附件、日志信息
### 扩展功能：
	实现网盘功能，可以管理目录与文件
## 2 技术构建
	Spring Boot、SpringMVC、log4j2、SpringData、RabbitMQ、Druid、Mysql、MongoDB、FastJson、Swagger2
	基于Log4j2+MongoDB实现日志管理
	基于SrpingDataMongoDB+MongoDB实现文件存储
	基于SpringMVC+SpringDataJPA+Druid+MYSQL实现网盘目录管理
	基于RESTful API实现实时查询接口
	基于RabbitMQ实现异步消息日志存储
	基于Swagger2实现构建RESTful APIs
![](https://raw.githubusercontent.com/yangty2010/RedSeaOSS/master/RedSeaOSS.png)  
