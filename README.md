一、下载 axel-2.17.9.tar.gz
安装命令：
1、下载源码包：
2、解压进入目录：
3、安装gcc编译器：
yum -y install gcc
4、配置，编译并安装：
./configure --without-ssl
make && make install
【axel-2.17.9安装完成】

+++++++++++++++++++++++++++++++++++++

二、安装：
1. 下载axel-2.17.9.tar.gz
2. 解压：
tar -xvf axel-2.17.9.tar.gz
5. cd axel-2.17.9
6.安装gcc编译器：
yum -y install gcc 
8. 配置，编译并安装：
./configure
make && make install 

+++++++++++++++++++++++++++++++++++++

三、让yum、wget使用axel加速插件：
1、复制 axelget.conf 到 /etc/yum/pluginconf.d/ 目录；

cd /etc/yum/pluginconf.d/
wget https://github.com/ihuangke/install_axel/blob/master/axelget.conf

2、复制 axelget.py 到 /usr/lib/yum-plugins/ 目录；

cd /usr/lib/yum-plugins/
wget https://github.com/ihuangke/install_axel/blob/master/axelget.py

3、编辑/etc/yum.conf 文件，修改线程数：

vi /etc/yum.conf 确认 /etc/yum.conf 文件中 piugins=1

4、更改默认线程数量：
vi /usr/lib/yum-plugins/axelget.py 
修改如下将10改为20
maxconn=20  （或者更大30）

————————————————————————————————————————

参考网址： 
网址：https://blog.csdn.net/zwjzqqb/article/details/79203574?tdsourcetag=s_pcqq_aiomsg
https://blog.csdn.net/lijiachang8/article/details/77334665
