---
title: 一些简单的命令
tag: 
    - Linux
    - 笔记
date: 2020-04-24
excerpt: Ubuntu下
category: Linux
---

# 日期与时间
<pre><code class="language-css">date</code></pre>


# 日历
<pre><code class="language-css">cal</code></pre>

## 格式
<pre><code class="language-css">cal [month] [year]</code></pre>


# 计算器
<pre><code class="language-css">bc</code></pre>


# apt包管理

## 安装
<pre><code class="language-css">apt-get install [包名] (-y)</code></pre>

## 移除
<pre><code class="language-css">apt-get remove [包名] (-y)</code></pre>

## 更新源
<pre><code class="language-css">apt-get update</code></pre>

## 更新包
<pre><code class="language-css">apt-get upgrade</code></pre>


# 定位
<pre><code class="language-css">cd [路径]</code></pre>


# 列出文件
<pre><code class="language-css">ls</code></pre>


# 查看当前路径
<pre><code class="language-css">pwd</code></pre>


# 删除
<pre><code class="language-css">rm</code></pre>

## 参数
- -i > 逐一询问确认
- -rf > 删除目录中所有文件，并且不用确认


# 创建
<pre><code class="language-css">mkdir [创建的文件名]</code></pre>


# 复制
<pre><code class="language-css">cp [复制的文件路径] [粘贴的文件路径]</code></pre>


# 权限
<pre><code class="language-css">chmod 777 [文件名] -c（或：chmod u=rwx,g=rwx,o=rwx t.log -c) # 授予文件777的权限</code></pre>