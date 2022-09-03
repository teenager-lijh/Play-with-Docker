## 72 Docker network host

host : 

直接使用宿主机的 ip 地址与外界通信，不再进行 NAT 转换

没有自己的网关 和 ip 地址



会产生警告：并不会对端口进行映射（会和主机共用相同的端口）

![image-20220831093622618](/Users/blueberry/git-Library/Play-with-Docker/72 Docker network host/72 Docker network host.assets/image-20220831093622618.png)



正确的做法：直接就不写端口映射 

![image-20220831093853946](/Users/blueberry/git-Library/Play-with-Docker/72 Docker network host/72 Docker network host.assets/image-20220831093853946.png)



![image-20220831102006562](/Users/blueberry/git-Library/Play-with-Docker/72 Docker network host/72 Docker network host.assets/image-20220831102006562.png)