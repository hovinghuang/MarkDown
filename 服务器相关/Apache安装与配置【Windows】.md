

#### 一、安装

##### 1.下载软件包，解压到指定路径

~~~
C：\Apache24
~~~

2.打开Apache24/conf下的httpd.conf

~~~xml
Define SRVROOT "C：\Apache24"
ServerRoot "${SRVROOT}"
~~~

#####3.命令行下进入到apache下面的bin目录，输入

~~~shell
httpd -k install #把apache安装成windows后台服务
~~~

##### 4.运行ApacheMonitor

#### 二、配置

1.打开Apache24/conf下的httpd.conf，去掉注释

~~~
# Virtual hosts
Include "conf/extra/httpd-vhosts.conf"
~~~

1.打开conf/extra/httpd-vhosts.conf ,添加虚拟主机配置

~~~
<VirtualHost *:80>
  ServerAdmin hovinghuang@qq.com
  DocumentRoot "C:\Product\qyy\ROOT"
  ServerName www.cdjrkg.com
  ErrorLog "logs\abc.localhost-error.log"
  CustomLog "logs\abc.localhost.access.log" combined
</VirtualHost>
--------------------- 
各个参数含义说明:
ServerAdmin  管理员邮箱
DocumentRoot 所需指向路径
ServerName   域名名称
ServerAlias  域名别名 可要可不要
ErrorLog     错误日志
CustomLog    访问日志
~~~



