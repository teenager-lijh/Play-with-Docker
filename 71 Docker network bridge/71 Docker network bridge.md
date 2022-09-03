## 71 Docker network bridge

![](/Users/blueberry/git-Library/Play-with-Docker/71 Docker network bridge/71 Docker network bridge.assets/image-20220831090234259.png)

Docker 服务默认会创建一个 docker0 网桥（其上有一个 docker0 内部 接口）， 该桥接网络的名称为 docker0，它在内核层连同了其他的物理或虚拟网卡，这就将所有容器和本地主机放到同一个物理网络。Docker 默认指定了 docker0 接口的 IP 地址和子网掩码，让主机和容器之间可以通过网桥相互通信。

就把 网桥理解为交换机即可

![](/Users/blueberry/git-Library/Play-with-Docker/71 Docker network bridge/71 Docker network bridge.assets/image-20220831090721254.png)



ubuntu 安装网络工具：

安装 ifconfig : `apt install net-tools` 

安装 ip 命令 ： `apt install iproute2`

安装 ping 命令 ：  `apt install iputils-ping`

通过 -p 进行端口映射 

![](/Users/blueberry/git-Library/Play-with-Docker/71 Docker network bridge/71 Docker network bridge.assets/image-20220831091619891.png)





在容器中是网卡 `eth0`：

![](/Users/blueberry/git-Library/Play-with-Docker/71 Docker network bridge/71 Docker network bridge.assets/image-20220831092626871.png)



在宿主机中是 `veth` : （33 和 34 形成一对 ） 

![](/Users/blueberry/git-Library/Play-with-Docker/71 Docker network bridge/71 Docker network bridge.assets/image-20220831092752712.png)