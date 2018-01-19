# 使用Elasticsearch,Logstash和Kibana管理Spring Boot日志
[查看原文](http://knes1.github.io/blog/2015/2015-08-16-manage-spring-boot-logs-with-elasticsearch-kibana-and-logstash.html)

当部署一个新项目时，我们需要反复查看的是日志管理。ELK(Elasticsearch, Logstash, Kibana)除了其它功能之外，还是一个强大而灵活的日志管理方案。本文讲解如何安装和配置ELK并且管理默Spring Boot应用的默认格式。
本文使用一个Spring Boot应用演示，该应用使用了Logstash进行了日志配置，将日志发送给Elasticsearch.演示代码是一个很简单的[任务列表](https://github.com/knes1/todo),可以在这里[下载](https://github.com/knes1/todo)

应用存储日志到日志文件,Logstash读取解析日志文件，并且将日志入口发送给一个Elasticsearch实例.最后，我们使用Kibaba4(Elasticsearch web前端)搜索和分析日志。

##### 步骤一.安装Elasticsearch
- 下载Elasticsearch压缩文件,下载地址[ https://www.elastic.co/downloads/elasticsearch](https://www.elastic.co/downloads/elasticsearch)
- 解压到某个文件夹.
- 执行bin/elasticsearch命令，windows下执行bin/elasticsearch.bat
- 检查elasticsearch是否运行,curl -XGET http://localhost:9200

##### 步骤二.安装kibana 4
##### 步骤三.安装Logstash
##### 步骤四.配置Spring Boot日志文件
##### 步骤五.配置Logstash理解Spring Boot日志文件格式




