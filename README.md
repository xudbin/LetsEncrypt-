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
 
