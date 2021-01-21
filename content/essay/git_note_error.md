---
title: "Git｜报错信息汇总"
date: 2021-01-21T10:26:10+08:00
draft: false
---



###### Q1

```shell
$ git add readme.md

fatal: not a git repository (or any of the parent directories)
# Git命令必须在Git仓库目录内执行（git init除外），在仓库目录外执行是没有意义的

fatal: pathspec 'readme.md' did not match any files
# 添加某个文件时，该文件必须在当前目录下存在
# 用 ls 或者 dir 命令查看当前目录的文件：1. 文件是否存在；2. 是否写错了文件名
```

