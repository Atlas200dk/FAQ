## 6.8 如何查看在开发者板上运行的应用程序的日志
### 问题描述
修改完/etc/network/interfaces文件后，在root用户下使用service networking restart失败。
![img](https://gitee.com/Atlas200DK/FAQ/raw/master/part6/img/6-9-1.png)
### 问题思路
可以尝试切换到普通用户下去执行命令：sudo service NetworkManager restart。之后网络服务重启，配置文件生效。
