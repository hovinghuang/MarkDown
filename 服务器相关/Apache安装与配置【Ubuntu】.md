#配置Apache服务器【Ubuntu】

1.安装

~~~shell
sudo apt-get install apache2
~~~

在本地浏览器输入服务器ip，会显示“It works!”，说明服务器已经启动成功了。

2.基本操作

~~~shell
开启：service apache2 start

关闭：service apache2 stop

重启：service apache2 restart

版本：apachectl -v
~~~

3.配置反向代理(待验证)

（1）加载模块

~~~shell
a2enmod proxy proxy_ajp proxy_balancer proxy_connect proxy_ftp proxy_http
~~~

（2）修改配置 

~~~shell
sudo vim /etc/apache2/mods-enabled/proxy.conf
输入内容：
ProxyRequests Off
<Proxy *>
    Order deny,allow
    Deny from all
    #Allow from .your_domain.com
</Proxy>
~~~

（3）

~~~shell
vim /etc/apache2/sites-enabled/default
输入内容：
<VirtualHost *:80>
         ServerName niuyufu.iokokok.cn
         ServerAlias niuyufu.iokokok.cn
         ProxyPass / http://www.baidu.com/
         ProxyPassReverse / http://www.baidu.com/
</VirtualHost>
~~~

（4）重启

~~~shell
service apache2 restart
~~~

（5）

~~~
#查看占用80端口的程序
root@hovinghuang:~# lsof -i :80
COMMAND    PID     USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
AliYunDun  807     root   16u  IPv4  14135      0t0  TCP hovinghuang:33722->100.100.30.25:http (ESTABLISHED)
nginx     1163     root    6u  IPv4  17383      0t0  TCP *:http (LISTEN)
nginx     1163     root    7u  IPv6  17384      0t0  TCP *:http (LISTEN)
nginx     1164 www-data    6u  IPv4  17383      0t0  TCP *:http (LISTEN)
nginx     1164 www-data    7u  IPv6  17384      0t0  TCP *:http (LISTEN)

#杀掉进程
kill -9 进程号PID

~~~

