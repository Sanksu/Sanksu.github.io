---
title: 安装WSL并安装图形界面
date: 2020-07-28
tag: Linux
category: Linux
index_img: https://docs.microsoft.com/zh-cn/windows/images/windows-linux-dev-env.png
excerpt: 适用于 Linux 的 Windows 子系统可让开发人员直接在 Windows 上按原样运行 GNU/Linux 环境（包括大多数命令行工具、实用工具和应用程序），且不会产生传统虚拟机或双启动设置开销。
---

# 参考 #
https://zhuanlan.zhihu.com/p/146146238

## 开始 ##
打开控制面板——程序——启用或关闭Windows功能——适用于Linux的Windows子系统

## 安装Linux ##
在微软商店中搜索Linux，即可安装
这里选的是Ubuntu

## 更换源 ## 
<pre><code class="language-css">sudo sed -i s@/archive.ubuntu.com/@/mirrors.aliyun.com/@g /etc/apt/sources.listsudo 
apt-get update && sudo apt-get upgrade -y</code></pre>

## 安装xfce4 ##
<pre><code class="language-css">sudo apt-get install xfce4 -y</code></pre>

## 添加环境变量 ##
<pre><code class="language-css">export DISPLAY=localhost:0 
source /etc/profile</code></pre>

## 打开XLaunch ## 
一路Next

## 访问图形界面 ##
<pre><code class="language-css">startxfce4</code></pre>


