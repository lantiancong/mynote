# Ubuntu

## 安装redis

```bash
# 安装编译所需的依赖
sudo apt update
sudo apt install build-essential tcl

# 下载最新稳定版Redis（请替换版本号为最新）
wget http://download.redis.io/releases/redis-7.2.4.tar.gz

# 解压文件
tar xzf redis-7.2.4.tar.gz

# 进入解压后的目录
cd redis-7.2.4

# 编译
make

# 安装
sudo make install

# 启动Redis服务器
redis-server
```

## 配置java环境变量

### **步骤 1：确定 WSL 中对应的 Windows 目录路径**

WSL 会将 Windows 的磁盘挂载到 `/mnt/` 目录下，因此：

- 你 Windows 中的 `D:\002\soft\java\JDK\jdk1.8.0_65` 目录，在 WSL Ubuntu 中对应的路径为：
  `/mnt/d/002/soft/java/JDK/jdk1.8.0_65`

```bash
#编辑环境变量配置文件
nano ~/.bashrc

# 配置 JDK 路径
export JAVA_HOME=/mnt/d/002/soft/java/JDK/jdk1.8.0_65
# 将 JDK 的 bin 目录添加到系统 PATH
export PATH=$JAVA_HOME/bin:$PATH

source ~/.bashrc

java -version
javac -version
```

输出类似以下内容即表示成功：

```bash
java version "1.8.0_65"
Java(TM) SE Runtime Environment (build 1.8.0_65-b17)
Java HotSpot(TM) 64-Bit Server VM (build 25.65-b01, mixed mode)
```

## 远程连接

```bash
systemctl status ssh
systemctl status sshd #CentOS里的
systemctl start ssh
systemctl enable ssh
systemctl restart ssh

#有没下载的可能
sudo apt install openssh-server
```

## 配置gcc环境

## 下载docker

