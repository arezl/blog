# 客户端连接腾讯云服务总是自动断开连接解决办法

#### 1.找到sshd_config配置文件

输入以下命令：

```javascript
vim /etc/ssh/sshd_config
```

在此文件中找到以下配置项：

```javascript
#ClientAliveInterval 0
#ClientAliveCountMax 3
```

去掉注释，改成

```javascript
ClientAliveInterval 30
ClientAliveCountMax 86400
```

这两行的意思分别是

1、服务端每隔多少秒向客户端发送一个心跳数据

2、客户端多少次没有相应，服务器自动断掉连接

### 2.重启sshd服务

输入以下命令重启ssh配置：

```javascript
service sshd restart
```