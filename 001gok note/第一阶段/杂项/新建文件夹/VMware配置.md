# kali配置

1. 下载
2. 官网 文件目录  -->> 通用设置  -->>  更新安装包

---

## 改中文

sudo dpkg-reconfigure locales

(上下看语言, 空格选中, 回车确定)

重启

---

---

# VMware相关

### 网络

- **Host-Only**(仅主机)
  - 不能访问外网, 仅主机可访问
  - 使用VMnet1网卡
- **NAT**(网络地址转换模式)
  - 常用
  - 宿主机充当网关, 外界不可见
  - 可访问外网, 外不可访问虚拟机
  - 使用VMnet8网卡
- **Bridged**(桥接模式)
  - 想真机(物理机)一样(复制) 
  - 可被访问 , 和访问外网
  - 网络支配器(网卡)是VMnet0

---

---

**主机有多张网卡, 所以有多个IP**

**NAT:**

​		xxx.xxx.xx.1  真机IP

​		xxx.xxx.xx.2  负责NAT的设备 

​		xxx.xxx.xx.3  到  xxx.xxx.xx.127 静态地址

​		xxx.xxx.xx.254  DHCP服务器

​		xxx.xxx.xx.255 广播 