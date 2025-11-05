# WSL

## 迁移存储位置

```bash
wsl -l -v  #查看wsl当前状态(需是Stopped)
wsl --shutdown  #关闭wsl
wsl --export [操作系统] [要放的绝对路径]
#比如 wsl --export Ubuntu E:\WSL\Ubuntu\Ubuntu.tar

#注销原来的WSL对应操作系统
wsl --unregister [系统名]
wsl --unregister Ubuntu

#解压(恢复)备份文件到目标位置
wsl --import [系统名] [目标位置绝对路径] [解压目标文件绝对路径]
wsl --import Ubuntu E:\WSL\Ubuntu E:\WSL\Ubuntu\Ubuntu.ta

#检验
wsl

#恢复默认用户
wsl --manage Ubuntu --set-default-user 用户名
wsl --manage Ubuntu --set-default-user prince
#要是还不行就用 wsl.exe --help 查找设置默认用户名的命令
```

[视频](https://www.bilibili.com/video/BV1VhAAecEYP?t=5.4)



