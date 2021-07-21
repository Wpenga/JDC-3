## 当前版本：V 1.0.7


JDC.exe windows平台

JDC linux平台

JDC-ARM arm平台（未测试，请自测）

![](https://raw.githubusercontent.com/dadaxiaoxiaod/JDC/main/pic.png)  
青龙面板2.8安装：

1、首先安装docker

2、拉取青龙 docker pull whyour/qinglong:latest

3、运行：edit模式下复制，才有""

docker run -dit

-v $PWD/ql/config:/ql/config

-v $PWD/ql/log:/ql/log

-v $PWD/ql/db:/ql/db

-p 9191:5700

--name qinglong

--hostname qinglong

--restart always

whyour/qinglong:latest

4、进ql docker exec -it qinglong /bin/bash

如果要在宿主机和docker间传递文件：docker cp 96f7f14e99ab:/ql /root/

青龙面板里变量为JC_COOKIE

JDC扫码的安装：

1、安装在/ql/下面

2、nano config.toml

3、chmod -R 777 ./public

4、nohup ./JDC &
