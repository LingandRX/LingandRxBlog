---
title: git的基本操作
date: 2023-07-19 11:56:27
tags: 
    - git
categories:
    - [学习]
---

## 创建仓库

### `git init`

> 初始化仓库

``` shell
# 使当前目录初始化为git仓库，同时会生成一个.git隐藏的文件夹，或者重新初始化现有仓库
git init
# 指定一个目录成为git仓库，同时会生成一个.git隐藏的文件夹
git init newRepo
```

### `git clone`

> 克隆远程仓库

```shell
# 克隆仓库
git clone <repo>
# 将仓库克隆到指定目录
git clone <repo> <directory>
```

### `git push`

> 上传远程代码合并

### `git pull`

> 下载远程代码合并

## 提交和修改

### `git add`

> 将文件添加到暂存区

### `git status`

> 查看仓库的当前状态,显示有变更的文件

### `git diff`

> 比较文件的不同,即暂存区和工作区的差异

### `git commit`

> 将文件添加到暂存区

### `git reset`

> 回退版本

### `git rm`

> 将文件从暂存区和工作区删除

### `git mv`

> 移动或者重命名工作区文件

## 分支管理

### `git checkout`

> 切换git分支

## 提交日志

### `git log`

> 查看历史提交日志

### `git blame <file>`

> 查看指定文件的修改日志
