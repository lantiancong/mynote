# w13rs

> 3306端口不一定能sql注入
>
> sql注入需要有数据库交互

> Apache
>
> sql

> echo	"base64"	|	base64	-d

> whatweb	(扫框架)

> 文件包含

> curl构造post请求
>
> 用burp或postman

w1r3s
1.信息收集
PORT      STATE  SERVICE
21/tcp    open   ftp
	21/tcp   open  ftp     vsftpd 2.0.8 or later
	ftp-anon: Anonymous FTP login allowed (FTP code 230)
22/tcp    open   ssh
	OpenSSH 7.2p2 Ubuntu 4ubuntu2.4 (Ubuntu Linux; protocol 2.0)
80/tcp    open   http
	Apache httpd 2.4.18 ((Ubuntu))
	/wordpress/wp-login.php
	
3306/tcp  open   mysql    *** 
	MySQL (unauthorized)   mysql -uroot -proot =》后台密码

站点：3306端口（mysql数据库）= sql注入（需要数据库交互）

2.漏洞验证
	ftp 匿名登录：
		常用名： W1R3S.inc
		
		hash：01ec2d8fc11c493b25029fb1f47f39ce
			This[空格]is[空格]not[空格]a[空格]password
		base64：SXQgaXMgZWFzeSwgYnV0IG5vdCB0aGF0IGVhc3kuLg==
			It is easy, but not that easy..
	
		The W1R3S.inc employee list
		Naomi.W - Manager
		Hector.A - IT Dept
		Joseph.G - Web Design
		Albert.O - Web Design
		Gina.L - Inventory
		Rico.D - Human Resources
		
	HTTP &ver=4.9.26"
		Administrator/admin/admin
		目录遍历漏洞： =》 知道某个文件名（不解析） =》 自动下载
		http://192.168.200.153/administrator/  cumappcms  =》 文件包含读取文件
			=》/etc/passwd   /etc/shadow  =》 john