---
title: Docker笔记
date: 2019-08-19 09:35:00
tags:
- Docker
- 部署

---

### 概念

容器

镜像

### 常用命令

```shell
# 查看当前运行的容器
> docker ps
# 查看所有（包括停掉的）容器
> docker ps -a 
# 查看本地存在哪些镜像
> docker images 
# -f参数，强制删除包含正在运行的容器
> docker rm 容器ID 
# 删除某个镜像
> docker rmi 镜像名 
> docker pull 镜像名
> docker search 镜像名
# 查看某个容器端口与宿主端口映射
> docker port 容器ID 
# 在容器中执行命令
> docker exec
# 启动一个容器，如：nginx
> docker run -i -d -p 8080:80 nginx
```



