问题：

容器的 ip 发生变化的时候，可以直接通过服务名进行通信，从而不收到影响

使用自定义网络来解决这个问题

![image-20220831230407429](/Users/blueberry/git-Library/Play-with-Docker/75-77 Docker 自定义 network/75-77 Docker 自定义 network.assets/image-20220831230407429.png)

 

1. 不使用自定义网络，通过 ip 地址是可以 ping 通的，但是使用服务名是不行的
2.  使用自定义网络 `docker network create <network-name>` 默认的 driver 是 bridge

![image-20220831231314663](/Users/blueberry/git-Library/Play-with-Docker/75-77 Docker 自定义 network/75-77 Docker 自定义 network.assets/image-20220831231314663.png)

指定容器到自定义网络：

![image-20220831231510431](/Users/blueberry/git-Library/Play-with-Docker/75-77 Docker 自定义 network/75-77 Docker 自定义 network.assets/image-20220831231510431.png)

 

apt update && apt upgrade && apt install net-tools -y && apt install iputils-ping -y

当两个容器位于同一个 `network` 中的时候，可以使用服务名（容器名）来代替 ip 地址

![image-20220901001031983](/Users/blueberry/git-Library/Play-with-Docker/75-77 Docker 自定义 network/75-77 Docker 自定义 network.assets/image-20220901001031983.png)