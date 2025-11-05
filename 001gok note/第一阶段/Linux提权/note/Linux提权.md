### Linux提权

#### 信息收集

### **操作系统	=>  版本漏洞**

> 内核：uname	-a
>
> 发行版：ls	/etc/*-release
>
> 主机名：hostname

### **安装的软件包	=》版本漏洞**

> Debian	=》**APT**	=》**dpkg	--list**
>
> Red Hat	=》**YUM**	=》**yum	list	installed**
>
> **RPM**	=》**rpm	-qa**

### **敏感凭据信息	=》**

> find /var/www -type f -regex '.*.jsp|.*php' | xargs egrep -i "user|pass"
>
> history（历史命令）

### **用户和组**	=》

> /etc/passwd文件	=》grep 'bash' /etc/passwd
>
> /etc/group文件
>
> /etc/shadow文件
>
> ![1](..\img\1-1.png)

> who
>
> whoami
>
> w
>
> id
>
> last	和	sudo lastlog
>
> sudo	-l	=>>	是否有sudo权限

### **进程和服务	=》**  杀软

> **ps	aux**
>
> > ps axjf以进程树的的格式打印。ps -ef也值得尝试，也可以配合grep过滤

### **网络连接**	=>网段，服务器多张网卡

> cat /etc/resolv.conf	=》配置DNS解析
>
> ip	a
>
> netstat	-unapt
>
> ss	-untpl
>
> (见document)
>
> 可以使用	lsof -i :22	进行端口过滤

### **linux提权**

> 没有一劳永逸的方法
>
> ![2](..\img\1-2.png)
>
> sudo	-l

> #### **SUID提权**
>
> ([GTFOBins](https://gtfobins.github.io/))
>
> ![3](..\img\1-3.png)

> #### **定时任务提权**
>
> [🔰雨苁ℒ🔰 - 暗网|黑客|极客|渗透测试|专注信息安全|数据泄露|隐私保护](https://www.ddosi.org/)
>
> ([反弹shell命令在线生成器|🔰雨苁🔰](https://www.ddosi.org/shell/))
>
> ![4](..\img\1-4.png)
>
> #### **系统级的cron任务**
>
> > 系统级别的cron任务位于/etc/crontab文件和/etc/cron.d/目录下

> #### **Linux内核提权**
>
> 见document
>
> **脏牛**
>
> 出现写数据到进程地址空间内只读内存区域的机会
>
> **DirtyPipe（CVE-2022-0847）**
>
> 可覆盖重写任意可读文件（甚至是只读文件）中的数据