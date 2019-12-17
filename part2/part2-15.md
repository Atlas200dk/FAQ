## 2.15 Atlas 200 DK如何实现SSH免密登录
### 背景信息
每个用户的家目录下都存在一个隐藏目录.ssh目录，保存有关SSH的配置信息。
### 操作步骤
1. 在Ubuntu主机中执行如下命令生成密钥文件。
如果Ubuntu主机中的登录用户家目录下的.ssh目录下已经存在密钥文件，则不需要执行此命令，否则原来的密钥文件会被覆盖。
ssh-keygen
根据提示信息进行配置，命令执行完成后会在.ssh目录下自动生成SSH公钥id_rsa.pub文件和私钥id_rsa文件。
2. 执行如下命令将Ubuntu主机中的公钥文件保存到Atlas 200 DK中。
ssh-copy-id -p 22 HwHiAiUser@192.168.1.2
