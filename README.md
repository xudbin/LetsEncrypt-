# LetsEncrypt-

#程序默认安装目录：

#centos 6 64位 首先安装 epel
sudo yum install epel-release


Apache：/usr/local/apache
PHP：/usr/local/php
MySQL：/usr/local/mysql


wget https://dl.eff.org/certbot-auto
chmod a+x certbot-auto

# 链接到 默认变量

# ln -s /usr/local/apache/bin/* /usr/local/bin/
 
 #添加 apachectl 默认变量路径，终端关闭后消失
 
 export PATH=/usr/local/apache/bin:$PATH
 
 echo $PATH 
 
 
 ./certbot-auto --help apache  #查看帮助
 ./certbot-auto --apache-server-root /usr/local/apache
 
 
 lamp add #添加虚拟主机
 
  #添加虚拟主机后找到域名的默认下面的配置
 ll /usr/local/apache/conf/vhost #编辑配置文件
 
 
 #不添加虚拟主机时默认
 /usr/local/apache/conf/httpd.conf
 #添加虚拟主机后找不到域名的默认下面的配置
 /usr/local/apache/conf/extra/httpd-vhosts.conf
 
 
 
 
 
