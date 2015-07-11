# MongoDB

MongoDB 是一个高性能、开源、无 Schema 的 NoSQL 数据库管理系统，常被用于高流量网站，在线游戏网站和搜索引擎的大规模数据管理和分类。它支持的数据结构非常松散，是类似 json 的 bson 格式，因此可以存储比较复杂的数据类型。

本镜像源自于 Docker Hub 镜像 **[tutum/mongodb](https://registry.hub.docker.com/u/tutum/mongodb/)**。

## 版本

当前版本 MongoDB 3.0

## 说明

该容器会给您部署一个 MongoDB。您可以使用如下命令登陆

```shell
user$ mongo --host <映射的地址> --port <映射的端口号>
```  

如果你想启动 MongoDB 并需要密码登录，你可以设置环境变量 `AUTH` 为 `yes`（默认为 `no`）。

容器启动后会自动创建一个具有所有权限的 `admin` 用户，并自动生成随机密码。如果你想为 `admin` 用户设置一个特定的密码，你可以将环境变量 `MONGODB_PASS` 设置为您需要的密码。

你也可以通过查看容器日志获得密码，比如

```
========================================================================
Please remember to change the above password as soon as possible!

    mongo admin -u admin -p 67u6kjiy6ll --host <host> --port <port>

========================================================================
```

在上面的例子中，`67u6kjiy6ll` 就是 `admin` 用户的密码。






