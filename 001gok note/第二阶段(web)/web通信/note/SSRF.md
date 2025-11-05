# SSRF

web服务器对后端服务器的访问限制没做好,使得web服务器可以读取敏感数据

![](../img/SSRF-1.png)



后端尝试的php代码

前端搜索栏中,可对file_get_contents();传递URL参数,比如 **https://www.baidu.com**

![](../img/SSRF-2.png)





![](../img/SSRF-3.png)

```php
curl
file_get_content
    
#这两个函数常可触发这个漏洞
```



直接扫端口号之类的,因为有一些会回显版本信息



gopher协议

类似www



![](../img/SSRF-4.png)


![](../img/SSRF-5.png)


![](../img/SSRF-6.png)


![](../img/SSRF-7.png)


![](../img/SSRF-8.png)


![](../img/SSRF-9.png)


![](../img/SSRF-10.png)


![](../img/SSRF-11.png)


![](../img/SSRF-12.png)


![](../img/SSRF-13.png)


![](../img/SSRF-14.png)


![](../img/SSRF-15.png)


![](../img/SSRF-16.png)


![](../img/SSRF-17.png)


![](../img/SSRF-18.png)


![](../img/SSRF-19.png)


![](../img/SSRF-20.png)


![](../img/SSRF-21.png)


![](../img/SSRF-22.png)


![](../img/SSRF-23.png)


![](../img/SSRF-24.png)


![](../img/SSRF-25.png)


![](../img/SSRF-26.png)


![](../img/SSRF-27.png)


![](../img/SSRF-28.png)


![](../img/SSRF-29.png)


![](../img/SSRF-30.png)



























