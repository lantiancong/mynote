# docker

## docker下载

Linux下载安装docker环境(Ubuntu为例)

![](../img/docker-download.png)

```bash
docker -v


# 下载安装脚本
curl -fsSL https://get.docker.com -o get-docker.sh

# 执行安装
sudo sh get-docker.sh


docker images 	#查看是否安装成功(连接到守护进程(开启))

#没有
systemctl status docker
systemctl start docker
systemctl enable docker
systemctl restart docker

```

[详细apt安装](..\note\006docker - 练习.md##docker安装详细)

## 关于systemctl

```bash
#关于systemctl
systemctl list-unit-files | grep [redis/docker...]#查看此别名的服务的真实名称

# 查看 redis 服务的详细信息，找到它链接到哪里
systemctl status redis
# 或者
systemctl cat redis

# 在 systemd 目录中查找 Redis 服务文件
sudo find /etc/systemd/system /usr/lib/systemd/system -name "*redis*" -type f
```



## docker有问题时重新安装

```bash
# 卸载有问题的Docker仓库
sudo rm -f /etc/apt/sources.list.d/docker.list

# 使用官方脚本安装
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```



**权限问题**：安装后记得将用户添加到 docker 组，否则需要一直使用 sudo

安装docker compose

```bash
# 下载最新版本的 Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

# 添加执行权限
sudo chmod +x /usr/local/bin/docker-compose

# 验证安装
docker-compose --version
```



## 镜像源

[阿里云](https://www.aliyun.com/)

详细获取步骤

![](../img/docker-1.png)

![](../img/docker-2.png)

![](../img/docker-3.png)

创建目录 ->创建配置文件并加入镜像源地址 ->加载守护进程 -> 重启docker



配置镜像源

```bash
1. 创建或编辑 Docker 配置文件
sudo mkdir -p /etc/docker
sudo nano /etc/docker/daemon.json


2. 添加国内镜像源
{
  "registry-mirrors": [
    "https://registry.cn-hangzhou.aliyuncs.com",
    "https://docker.mirrors.ustc.edu.cn",
    "https://hub-mirror.c.163.com"
  ]
}

3. 重启 Docker 服务
sudo systemctl daemon-reload
sudo systemctl restart docker

4. 检查配置是否生效
sudo docker info
```

```bash
# 1. 停止 Docker 服务
sudo systemctl stop docker

# 2. 配置镜像加速器
sudo tee /etc/docker/daemon.json <<EOF
{
  "registry-mirrors": [
    "https://registry.cn-hangzhou.aliyuncs.com",
    "https://docker.mirrors.ustc.edu.cn",
    "https://hub-mirror.c.163.com"
  ]
}
EOF

# 3. 重启 Docker 服务
sudo systemctl daemon-reload
sudo systemctl start docker

# 4. 验证配置
sudo docker info | grep -A 10 "Registry Mirrors"

# 5. 测试下载
sudo docker pull nginx
```









##**镜像可以用Windows类比,就是安装包双击安装后下载的一堆直接可运行文件**##

![](../img/docker-5.png)

---

## 部署服务

MySQL为例

> 此为要一行 "**\\**" 是用来换行的

![](../img/docker-4.png)

一次下载多次运行,和软件多开一样

## 命令

![](../img/docker-4.png)

```bash
-d 是后台运行
--name 取名字
-p 端口映射 [真实地址:容器虚拟地址]

##
-e 格式:KEY=VALUE [设置环境变量]
##这个参数有几个要看官方文档

镜像名字(这里是mysql)
格式[镜像名repository:版本tag]
#没写版本默认最新
```

![](../img/docker-6.png)

# docker基础

## 常见命令

**命令过程,要能手绘**

[讲解](https://www.bilibili.com/video/BV1HP4118797?t=32.8&p=5)

![](../img/docker-7.png)

```bash
docker logs
docker exec
```

[练习](C:\Users\1\Desktop\note\002其他\小点\note\006docker - 练习.md)

