---
title: "Git｜速查表"
date: 2021-01-21T10:03:29+08:00
draft: false
---



[廖雪峰 Git 教程](https://www.liaoxuefeng.com/wiki/896043488029600)

---

##### 设置全局用户名和邮箱

因为 git 是分布式版本控制系统，机器需要自报家门

```shell
# --global 参数：表示机器上所有的仓库都会使用这个配置
$ git config --global user.name "Your Name"
$ git config --global user.email "emai@example.com"
```

##### 创建版本库

```shell
# 创建本地目录
$ mkdir git_notes
$ cd git_notes

# 将这个目录变为 git 仓库
$ git init

# 该目录下会自动创建 .git 隐藏目录，通过 -al 参数查看
$ ls -al 
```

##### 提交文件到本地仓库

```shell
# 随便新建个文件
$ cd git_notes
$ echo "git notes" > readme.md

# - 添加单个文件到本地仓库
$ git add readme.md
# - 添加目录下所有文件到本地仓库
$ git add . 

# 提交文件到本地仓库
$ git commit -m "first commit readme.md"
```

##### 查看状态

```shell
$ git status
```

##### 查看改动内容

```shell
$ git diff readme.md
```

