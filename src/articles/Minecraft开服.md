---
title: Minecraft开服
tag: 游戏
date: 2020-05-16
category: 游戏
excerpt: 服务器要到期了，没钱续费orz
index_img: https://www.minecraft.net/content/dam/games/minecraft/screenshots/rtxlaunch-carousel.jpg
---
# 常考
https://jingyan.baidu.com/article/ed2a5d1f6c76ac09f6be1781.html<br/>
https://minecraft-zh.gamepedia.com/Server.properties


# **Window**

## 服务端
打开官方启动器->配置->新建->选择版本->服务器<br/>
接着会打开浏览器下载
得到一个server.jar文件

### 注:
Mod服以及插件服需要第三方服务端


## 启动
新建.txt文件，输入

```cpp
@echo OFF
java -Xmx2G -Xms256M -jar <文件名>.jar
pause
```


改后缀为.bat
双击启动

### 注:
“-Xmx2G”为分配给服务器的最大内存，可以设置为“-Xmx1G”或“Xmx1024M” <br/>
内存单位一定要大写<br/>
“-Xms256M” 为分配给服务器的最小内存<br/>
.bat文件要和服务端文件放在同一目录下


## 配置
第一次启动会提示你同意eula协议<br/>
打开目录下的eula.txt<br/>
将最后一行“eula=false”改成“eula=true”<br/>
保存，重启服务器

### 注:
可通过修改server.properties文件来配置Minecraft服务器<br/>
[参数的解释](https://minecraft-zh.gamepedia.com/Server.properties)


## 畅玩
将默认25565端口映射外网

# **Linux**

## 服务端
同windows

## 启动
这里用脚本启动<br/>

```cpp
#!/bin/sh

java -Xms256M -Xmx2G -jar <路径>
nogui
```

## 配置
同windows
