---
title: docker
date: 2021-11-22 00:16:53
tags: docker
---

## 安装

- 打开 Hyper-V
- [doker desktop 安装](https://www.docker.com/get-started)

      WSL 2 installation is incomplete.
         cmd > wsl --update

---

## 使用

1. 创建镜像
   - `docker build -t docker-vue-test .`

      -t ：指定 image 文件的名字

      . ：文件范围

2. 查看镜像
   - `docker iamges`

      ![查看镜像](images.png)

3. 运行镜像
   - `docker run -d -p 8080:8080 -v /src:/docker-vue-test/src docker-vue-test`

      -d : 后台运行容器，并返回容器ID

      -it : (常用) i : 以交互模式运行容器，t : 为容器重新分配一个伪输入终端

      -p : 指定端口映射，格式为：主机(宿主)端口:容器端口

      -v : 挂载，绑定一个卷

      ![运行镜像](imagesRun.png)
