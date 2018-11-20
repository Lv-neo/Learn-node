---
title: 安装Hexo
tag: hexo
---

<!-- toc -->

## install

```
npm install -g hexo-cli
npm install hexo-deployer-git --save
hexo -v        
```

## create blog

创建一个你的博客文件夹(必须是空文件夹)，如放在桌面~/Desktop/hexo-blog，并进入这个文件夹,示例如下

```
cd ~/Desktop/hexo-blog
hexo init
npm install
hexo generate          // hexo g 也可以
hexo server
```

打开http://localhost:4000/，会看效果

在博客根目录下的 _config.yml 中如下配置:
```
server:
  port: 8080
```
修改服务端口

## 部署Github仓库

```
deploy:
  type: git
  repo: git@github.com:Lv-neo/Learn-node.git
  branch: master
  name: 
  email: 
```

## 生成和部署
```
hexo clean   //清除缓存文件 (db.json) 和已生成的静态文件 (public)
hexo g       //生成缓存和静态文件
hexo d       //重新部署到服务器
```

## toc

```
npm install hexo-toc --save
```

在博客根目录下的 _config.yml 中如下配置：
```
toc:
  maxDepth: 3
```

文章中请添加
```
<!-- toc -->
```

