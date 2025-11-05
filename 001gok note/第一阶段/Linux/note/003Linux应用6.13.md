Linux系统进阶

# 软件管理

包管理

kali/Ubuntu ==>.deb(apt)

【两类】: [.deb],[.rpm]

怎么安装，安装思路

![1](..\img\3-1 apt命令.png)

![2](..\img\3-2 yum.png)

---

### 编译安装

1. 通常是.tar.gz或.tar.bz2格式

2. **解压**包: tar -xzvf <package>.tar.gz 

3.  **配置**:进入源码目录，运行./configure进行必要的配置

   cd <package>

   ./configure

4. 使用make**编译**源代码:  make

5. 使用sudo make install将软件**安装**到系统中

---

# 进程管理

前台进程,后台进程,(守护进程)

> 守护:日志,网络,任务调度

##### 查看进程:

> ps:
>
> ![3](..\img\3-3 查看进程.png)

(ps输出示例在最底)

> top :
>
> 实时更新 
>
> 按q退出

> pstree:
>
> 树状显示

> lsof:
>
> 用于列出系统中打开的文件及其关联的进程
>
> ![5](..\img\3-5 isof.png)

---



### 进程控制

>kill:
>
>kill  【PID】
>
>kill -9 【PID】

> killall:
>
> 结束指定的**所有**进程
>
> 例如，killall apache2会结束所有名为apache2 的进程

> pkill:
>
> 通过**进程名**终止进程，可以使用**正则表达式**匹配。例如，pkill -f python将结束所有与    Python 脚本相关的进程

---

# 服务管理       

> centOS,Ubuntu: systemd 包
>
> 最小单位是单元
>
> systemctl命令
>
> 旧版：service
>
> 传统初始化系统：sysvinit

---

### systemd:

![6](..\img\3-6 systemd.png)

常用命令:

![7](..\img\3-7 systemd.png)

(最下面补充了SysVinit)

---

# 网络管理

> 网络接口
>
> 有线eth0，eth1
>
> 无线wlan，wlp2s0，
>
> lo(本地环回接口)，ens33
>
> **ip a /ifconfig命令**

##### 网络服务(端口)管理:

> web:	http,DNS,FTP...
>
> Linux查看命令:
>
> **ss**:	查看当前系统的TCP、U DP连接信息
>
> 使用ss -tuln查看所有监听的端口(尾附解释)
>
> **netstat**:	
>
> 这是一个传统的工具，用来显示网络连接、路由表和接口信息等。
>
> 常用的选项组合有netstat -tuln和netstat -an

##### 防火墙:

> 工具
>
> iptables、firewalld

![10](..\img\3-10 防火墙.png)



---

---

# 详解

ps输出详解:

![4](..\img\3-4-1 ps输出.png)

![4](..\img\3-4-2 ps.png)

SysVinit(service)

![8](..\img\3-8 sysvinit.png)

![9](..\img\3-9 ss.png)
