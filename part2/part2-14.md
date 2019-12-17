## 2.14 重启操作系统后USB网卡需要重新配置
### 问题描述
部分环境下，配置USB网卡后，无论Ubuntu主机重启还是Atlas 200 DK重启都要重新配置，主机重启后是存在配置信息的，但USB网卡的IP地址未生效，需要删掉之前配置，重新配置，请问有什么解决办法吗？
### 解决方法
因为网络配置文件中配置信息是存在的，所以不需要重新给USB虚拟网卡配置IP，执行如下命令重启网卡即可。
sudo service network-manager restart
重启后执行ifconfig -a命令查看USB虚拟网卡的IP地址是否显示。