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
 
 
#升级python 2.7  
 
yum groupinstall "Development tools"
 
 
yum install zlib-devel bzip2-devel openssl-devel ncurses-devel
 
 
cd /opt

wget https://www.python.org/ftp/python/2.7.13/Python-2.7.13.tgz

tar xf Python-2.7.13.tgz
cd Python-2.7.13
./configure
make install

#配置默认连接
#cd /usr/local/bin
#ls -ltr python*
#ln -s /usr/local/bin/python2.7 /usr/local/bin/python

添加letsencrypt 自动续期



./certbot-auto renew
echo "0 0 2 * * root /root/renew.sh >/dev/null 2>&1"
 
 
