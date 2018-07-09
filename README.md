# www.akikun.com

这是[www.akikun.com](http://www.akikun.com) 这个博客站的所有代码。

欢迎大家star或者fork。

如果遇到什么问题，你可以随时：

- [Issues](https://github.com/vagabondize/vagabondize.github.io/issues)
- [Pull Requests](https://github.com/vagabondize/vagabondize.github.io/pulls)

## 环境搭建

### 安装Ruby

jekyll本身基于Ruby开发，因此，想要在本地构建一个jekyll的环境需要具有Ruby的开发和运行环境。

在windows下，可以使用[Rubyinstaller](http://rubyinstaller.org/downloads/)安装。[ruby安装说明](http://www.ruby-lang.org/zh_cn/downloads/)

### 安装Bundle

直接使用下面命令即可：

`$ gem install bundler`


## 项目展示

clone项目到本地

`$ git clone https://github.com/vagabondize/vagabondize.github.io.git`

vagabondize.github.io这个文件夹

`$ cd vagabondize.github.io`

执行bundle命令下载依赖资源：

`$ bundle install`

资源加载完毕后，使用下面命令，启动本地服务：

`$ bundle exec jekyll serve`

浏览器输入 `localhost:4000` 来访问项目。

## 创建第一篇文章

在根目录新建`_posts`文件夹。
`mkdir _posts`

在`_posts`文件夹内新建一个以`.md`格式结尾的markdown文件。
文件名必须以`{:日期}-{:文件名}.md`的格式。
`touch 2015-09-06-hello-world.md`

该文件需要有`--- ---`的头文件声明，如下：
```
---
layout: post
title: Hello World!
categories: frontend
tags: [html, css3]
---
```

- `layout`: 指定文章模板
- `title` : 声明标题
- `categories`: 指定文章分类
- `tags`  : 标签

浏览器输入 `localhost:4000/{:categories}/` 即可访问文章列表，如：
`localhost:4000/frontend/`

浏览器输入 `localhost:4000/{:categories}/{:文件名(去掉日期)}.html` 即可访问文章，如：
`localhost:4000/frontend/hello-world.html`