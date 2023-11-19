---
layout: post
title: Git配置 
date: 2023-05-31 07:51:51
tags:
    - git
categories:
    - [学习]
---

## 设置机器的git的用户信息

```shell
git config --global user.name 'testname'
git config --global user.email 'test@test.com'
```
<!-- more -->
## 生成id_rsa密钥和id_rsa.pub公开密钥

```shell
ssh-keygen -t rsa
```

密钥和公开密钥信息存储在`'~/.ssh'`目录中

```shell
.ssh/
├── authorized_keys
├── id_rsa
├── id_rsa.pub
└── known_hosts
```

authorized_keys: 免密登录/密钥登录
id_rsa: 密钥
id_rsa.pub: 公开密钥
known_hosts: 记录登录机器信息

## 配置github

1. 在github设置界面打开SSH and GPG keys页面
2. 点击new SSH keys
3. 填写Title,任意名称
4. Key type默认即可
5. 将`id_rsa.pub`中的内容至Key内容框中

## 测试机器是否连通github

```shell
ssh -t git@github.com
```

## 配置免密登录

1. 将pub文件传给要登录的机器`scp -P 22 ~/.ssh/id_rsa.pub root@ip地址:~/地址`
2. 将公开密钥写入`authorized_keys`,`cat ~/地址/id_rsa.pub > ~/ssh/authorized_keys`
3. 测试免密登录`ssh root@ip地址`
