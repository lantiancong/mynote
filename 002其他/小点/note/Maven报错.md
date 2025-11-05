# Maven助力手动管理依赖

使用Maven下载依赖,但是导入到lib包

配置完pom.xml后不要直接更新

进IDEA按Alt + F12 进入终端

输入

```shell
mvn dependency:copy-dependencies -DoutputDirectory=lib
```



### ##可能会遇到的几个问题(我的问题)

1. 最好不要配置多个jdk环境变量
2. maven配置文件中java版本更改为和环境变量一样的般本
3. **重启电脑 ! ! **

