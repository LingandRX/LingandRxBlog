---
layout: post
title: git配置
date: 2023-05-31 07:51:51
tags:
    - git
categories:
    - [学习]
---

进入gitbash，或者powershell

## 设置git的用户信息

```powershell
git config --global user.name '用户名'
git config --global user.email 'xxx@qq.com'
```
<!-- more -->
## 生产rsa信息

```shell
ssh-keygen -t rsa
```

rsa信息会存储在`'C:\\Users\\电脑用户名/.ssh'`目录中

```shell
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         2023/5/31      7:54           2602 id_rsa
-a----         2023/5/31      7:54            565 id_rsa.pub
-a----         2023/5/31      7:57            831 known_hosts
-a----         2023/5/31      7:57             93 known_hosts.old
```

## 配置github

在github设置界面打开SSH and GPG keys页面

点击new SSH keys

Title起一个容易记得的名字

Key type默认即可

将`id_rsa.pub`中的内容至Key内容框中

## 测试机器是否连通github

```shell
ssh -t git@github.com
```
