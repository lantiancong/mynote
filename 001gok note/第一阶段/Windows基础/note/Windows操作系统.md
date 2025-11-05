# Windows操作系统

#### 版本

> 1985年诞生
>
> 09Windows7
>
> 15Windows10
>
> 21Windows11

#### 特点

> 图形化
>
> 兼容性强
>
> 多任务处理

#### 安全性

> 过于安全
>
> systeminfo可看补丁信息

#### Windows应用

> **sever**
>
> 针对服务器
>
> 服务器管理器
>
> **嵌入式**
>
> ATM，等等

#### 版本

> 家庭版，专业版，企业版，服务器版  
>
> 查看版本
>
> Get-WmiObject -Class win32_OperatingSystem | select Version,BuildNumber

> 版本号
>
> 如10.0.10240.16384
>
> 主版本号，次版本号，内部版本号，修订号

---

### 文件系统

> **NTFS**
>
> windows默认文件系统
>
> 权限参数：
>
> **权限层级：显式，继承权限。拒绝>允许**

> **FAT32**
>
> 管理简单



**NTF权限:**

读,写,执行,删除,修改,完全控制

**权限层级**

显式权限	继承权限

拒绝权限 > 允许权限

---

**ICACLS**(访问控制列表)

> **常用权限**
>
> 完全控制	修改
>
> 读取和执行	写入	特殊权限

> **常用继承类型**
>
> 容器继承
>
> 对象继承
>
> 不继承
>
> 继承权限

*常用icacls命令见document文件夹*

---

### 服务和进程

> 服务
>
> 由SCM（服务控制管理器）管理

> 进程
>
> 进程的⽣命周期包括创建、运⾏、等待和终⽌等状态
>
> 任务管理器、资源监视器和命令⾏⼯具（如 tasklist 和 taskkill ）

服务与进程关系(见document)

**LSASS**(价值高)

**SAM(在注册表中)**

01:50:00



LSASS

---

#### 管理服务

> 可以使⽤sc.exe和PowerShell的Get-Service查询和管理服务
>
> powershell命令
>
> Get-Service | ? {$_.Status -eq "Running"} 

> sc命令
>
> (见document)

#### 管理进程

任务管理器





