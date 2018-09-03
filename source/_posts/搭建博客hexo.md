---
layout: 工具
title: 搭建博客 hexo & github & theme
date: 2018-05-23 16:46:47
tags: 工具使用
---
 hexo 搭建博客
 github 将博客与 github 关联, 同时实现 一边写 md 文件, 一边本地预览
 theme  本博客，用的主题 yilia 设置博客主题

 <font colo="red">this is a test, upload git book, online added</font> 

-----------------------------------------------------------------------------------------------

### 一、github 博客托管，可直接实现外网访问  https://lefthandcat.github.io

  ![github.io](/blogImg/hexo/blog.png)

### 二、 hexo 安装及配置
1.全局安装 hexo
```
npm install -g hexo
```
  
2.随便哪个盘，创建一个新的文件夹 Hexo, 在这个文件夹下 打开 git bash 依次操作下面的命令：
```
hexo init
```

```
npm install
```

```
hexo clean
```

```
hexo generate
```

```
hexo deploy
```

```
hexo server
```

 <font color=#e4393c size=5>
注： hexo deploy 报错的话（在与 github 关联时会增加配置，会报错 git undefined  
     解决办法: 在当前目录下安装
</font>

```
npm install hexo-deployer-git --save
```


* 本地访问：http://localhost:4000/
* 线上访问：https://lefthandcat.github.io/ 

<font color=#e4393c size=5>
 注： 
        hexo clean  
        hexo generate  
        hexo deploy  
        hexo server 
        在 本地 与 线上 (github.io) 同步时都要进行这几个步骤
</font>

如图：
![github.io](/blogImg/hexo/deploy.png)


3._config.yml 增加配置，关联 github

```
deploy:
  type: git
  repository: https://github.com/leftHandCat/leftHandCat.github.io
  branch: master
```

如图：
![github.io](/blogImg/hexo/config.png)

![github.io](/blogImg/hexo/github.png)


 ### 三、设置主题 yilia 
1.github 去搜索 yilia, 克隆 到 Hexo/themes 文件夹中
2.修改 _config.yml
3.修改头像地址，根目录是 Hexo/source

```
avatar: /headImg/timg.jpg
```

 ### 四、添加 md 文件

目录： Hexo/source/_posts

 ![github.io](/blogImg/hexo/img.png)

再执行：
        hexo clean  
        hexo generate  
        hexo deploy  
        hexo server 












