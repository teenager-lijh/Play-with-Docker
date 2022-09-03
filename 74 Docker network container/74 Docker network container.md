##  74 Docker network container

新创建的容器和已经存在的一个容器共享一个网络 ip 配置而不是和宿主机共享。新创建的容器不会创建自己的网卡，配置自己的 ip，而是和一个指定的容器共享 ip 和 端口。同样，这两个容器除了网络配置方面，其他的如文件系统，进程列表等还是隔离的。

![image-20220831201046352](/Users/blueberry/git-Library/Play-with-Docker/74 Docker network container/74 Docker network container.assets/image-20220831201046352.png)

错误案例： 

因为 `tomcat85` 和 `tomcat86` 共用 同一个网络配置，

所以不应该这样做端口映射

![image-20220831201134912](/Users/blueberry/git-Library/Play-with-Docker/74 Docker network container/74 Docker network container.assets/image-20220831201134912.png)



正确案例：

若 alpine2 想要和 alpine1 共用一个 ip 和端口范围，就要求 alpine1 是运行状态，否则 alpine2 的网络状态是不可用的：

![image-20220831201613383](/Users/blueberry/git-Library/Play-with-Docker/74 Docker network container/74 Docker network container.assets/image-20220831201613383.png)









