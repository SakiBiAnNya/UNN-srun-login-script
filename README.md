fork自：

[中国科学院大学雁栖湖校区深澜校园网登录python脚本](https://github.com/coffeehat/BIT-srun-login-script)

另有支持多平台（包括openwrt）的golang版本，请见：https://github.com/Mmx233/BitSrunLoginGo

目前只修改了登录网址，已经可以实现南宁学院的上网认证（深澜）。  

# 概述

南宁学院深澜校园网登录python脚本，可用于任何支持python的设备的网络命令行登录或命令行登录。

详细文档见原fork和原作者：
https://github.com/henry-tujia/UCAS-srun-login-script
https://github.com/coffeehat/BIT-srun-login-script
[深澜校园网登录的分析与python实现-北京理工大学版](https://zhuanlan.zhihu.com/p/122556315)

# 文件说明

|文件|说明|
|:-:|:-:|
|BitSrunLogin/|深澜登录函数包|
|demo.py|登录示例脚本|
|always_online.py|在线监测脚本，如果监测到掉线则自动重连|

修改脚本文件里的：
lm.logout(
    username = "username",#填入你的账号
    password = "password"#填入你的密码

即可

always_online.py可采用`nohup`命令挂在后台：
``` bash
nohup python always_online.py &
```
Windows可以在计算机管理-创建任务计划，触发器自定，添加操作-启动程序-程序或脚本为你的Python安装目录（Python.exe）,添加参数为脚本文件的绝对路径。
