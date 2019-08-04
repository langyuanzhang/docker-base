# docker-base

docker的基础命令

##### docker run流程：
客户端向docker daemon发送一条pull命令，docker daemon会先在本机查找镜像，如果没找到则去远程仓库里找，然后把镜像下载到本地，下载回来后通过一定的方式将镜像运行起来，变成docker容器。

![流程](./liucheng.jpg)搜索下载相关资源


###### win10系统去docker官网下载，一路next安装即可

###### 可去[官网仓库](https://hub.docker.com/)搜索下载相关资源


##### 拉取镜像	
```
docker pull nginx
```


##### 查看本机的镜像  

```
docker images
```


##### 查看正在运行的容器（进程）

```
docker ps
```


##### 运行docker容器

```
docker run nginx
```


##### 后台运行

```
docker run -d nginx
```


##### 进入运行容器中执行命令

```
docker exec -it 7ab811911057(容器id) bash
```


##### 停止运行容器

```
docker stop 7ab811911057(容器id)
```


##### 主机8080端口 映射到 docker容器 80端口 (-P 所有端口跟主机端口进行随机映射)

```
docker run -d -p 8888:80 nginx
```


###### win10查看端口情况
```
netstat
```

