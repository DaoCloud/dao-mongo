# MongoDB

MongoDB是一个高性能、开源、无Schema的NoSQL数据库管理系统，常被用于高流量网站，在线游戏网站和搜索引擎的大规模数据管理和分类。它支持的数据结构非常松散，是类似json的bson格式，因此可以存储比较复杂的数据类型。

本镜像源自于DockerHub镜像[tutum/mongodb](https://registry.hub.docker.com/u/tutum/mongodb/)。

## 版本

当前版本 MongoDB 3.0

## 说明

改容器会给您部署一个MongoDB。您可以使用如下命令登陆

> ========================================================================

>     You can now connect to this MongoDB server using:

>        mongo --host <host> --port <port>

>    ========================================================================
>    

如果你想启动MongoDB并需要密码登录，你可以设置环境变量 *AUTH* 为 *yes*, 默认为 *no* 。


容器启动后会自动创建一个具有所有权限的admin用户，并自动生成随机密码。如果你想为admin用户设置一个特定的密码，你可以设置环境变量 *MONGODB_PASS* 为您需要的密码。

你可以通过查看容器日志获得密码，比如

> ========================================================================

>     You can now connect to this MongoDB server using:

>        mongo admin -u admin -p 67u6kjiy6ll --host <host> --port <port>

>    Please remember to change the above password as soon as possible!

>    ========================================================================

在上面的例子中，*67u6kjiy6ll* 就是admin用户的密码。






