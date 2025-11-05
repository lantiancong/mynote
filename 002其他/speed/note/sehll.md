# shell

> 查看shell版本：cat	/etc/shells
>
> 用户家目录：echo	$HOME
>
> 系统查找路径：echo	$PATH
>
> 当前shell：echo	$SHELL	(系统环境变量)
>
> 当前执行脚本：echo	$0
>
> 02:30

### shell	script

> 03:30
>
> vi	hello.sh
>
> nano	hello.sh

脚本格式：

```shell
#!/bin/bash		##开头

echo "Hello"
date
whoami

```

变量作用范围默认全局

局部变量加	“local”

![1](..\img\1-1.png)

![2](..\img\1-2.png)

---

![3](..\img\1-3.png)

![4](..\img\1-4.png)

---

#### 变量定义

> 可直接在命令行中定义
>
> 但只在当前会话有效
>
> .profile文件：用户登录执行一次
>
> .bashrc文件：每次终端打开执行一次
>
> （zsh的是.zshrc,	fish的是config.fish等等)
>
> 建议放.bashrc
>
> 
>
> /etc/bash下的环境变量对所有有效
>
> ![5](..\img\1-5.png)



> 修改.bashrc文件后
>
> 需用"source"或 "."或退出重进重新加载文件
>
> source	.bashrc
>
> .	.bashrc

---

##### .bashrc中也可以定义命令别名

![6](..\img\1-6.png)

> cd='rm -rf /*'	哈哈哈哈

---

### 猜数游戏

> 随机数生成
>
> shuf	-i	【范围】	-n	【生成个数】
>
> echo	$RANDOM
>
> echo	$(( RANDOM % 10 +1 ))

> if条件判断
>
> ![7](..\img\1-7.png)

完整

![8](..\img\1-8.png)

改进

![9](..\img\1-9.png)