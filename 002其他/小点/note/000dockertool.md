# docker

### 2025可用镜像源

```bash
docker.1ms.run
docker-0.unsee.tech
docker.hlmirror.com
docker.m.daocloud.io
hub.rat.dev
```

如拉取redis镜像并运行

```docker
docker pull docker.1ms.run/redis
```

拉取后用	docker	images	可看到新镜像"docker.1ms.run/redis"

使用此镜像创造container

```bash
docker run -it --name my-redis -p 6379:6379 docker.1ms.run/redis
即可创建容器并打开redis
[还有一个是启动并设置密码docker run -it --name my-redis -p 6379:6379 docker.1ms.run/redis redis-server --requirepass "yourpassword"]

然后redis会在后端运行[ctrl+C停]
需再打开一个终端
输入

docker exec -it <容器名(这里是my-redis)或id> redis-cli
```

