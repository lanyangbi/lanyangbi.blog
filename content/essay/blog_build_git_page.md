---
title: "Blog_build_git_page"
date: 2021-01-20T21:51:17+08:00
draft: false
---



博客静态页面搭建完成后，接下来就需要发布了。但是还没有自己的服务器和注册域名，如何发布呢？

这里要感谢 github 提供的 `gitHub.io`，可以对外发布并展示自己的项目。

`Websites for you and your projects.`



---



### 1. 创建 github.io

如果没有账号就先 [注册](https://github.com/)

**登录 `github` 个人页面，新建仓库**

- 对外发布仓库

注意格式必须为 `用户名.github.io`，这里的用户名可以通过点击头像 `Signed in as xxx` 查看

- 保留博客文件仓库

如果博客文件保留在本地的话，就不需要创建

创建好仓库后，`clone` 到本地路径，这个路径自定义

```shel
$ git clone https://github.com/lanyangbi/lanyangbi.blog.git
```

将创建的所有日志文件全部复制到 `blog` 目录下

```shell
$ cd blog
$ mv * lanyangbi.blog
$ hugo --theme=sam --buildDrafts --baseUrl="https://lanyangbi.github.io/"
$ cd public
$ git remote add origin https://github.com/lanyangbi/lanyangbi.github.io.git
$ git add -A
$ git commit -m “first commit”
$ git push -u origin master
```



### 2. 将 Hugo 生成为 html 格式

进入博客目录下，执行

```shell
# -D 代表草稿也进行编译
$ hugo -D
```

就会在当前目录生成一个 public 目录，生成网页静态文件

这里遇到一个报错：

```log
ERROR 2021/01/20 22:38:04 error: failed to transform resource: POSTCSS: failed to transform "css/main.css" (text/css): PostCSS not found; install with "npm install postcss-cli". See https://gohugo.io/hugo-pipes/postcss/
```

按照提示 `npm install postcss-cli` 下载即可

 

### 3. 将 public 目录移动到发布路径

到这里，就只需要将 public 目录的文件 cp 到

```shell
$ cp 
```

