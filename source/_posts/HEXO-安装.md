---
title: HEXO 安装
date: 2017-03-29 17:40:58
tags: HEXO
typora-root-url: ..
---


今天看到了一篇大神的博客,界面非常的简洁炫酷,顿时燃起了我的那颗折腾的心.

原来是HEXO,搭配的主题真的十分好看,实战起来.

<!-- more -->

### 1.准备工作

1. 安装`node` ,这个是每个程序员的必备额,配好`cnpm`方便下载模块包

2. 穷屌丝没有主机怎么办,可以用github的page,程序猿不可能没有github账号,注册一个,新建一个库,命名方式`username.github.io`,这样可以不用在后边的配置里重新配置根目录,如果你你是放在其他目录下,则需要改写根目录,不然,就会像我一样傻傻折腾半天.



### 2.初始化HEXO

官网上面的提示一目了然,直接按那个来

```
npm install hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
```

现在应该在本地就可以跑起来了.

### 3.安装主题

前面提到的主题就是[NEXT](http://theme-next.iissnan.com/) 

![NextSchemes3](/images/NextSchemes3.png)

使用方法:

1. 打开你的博客目录,首先克隆这个主题

   `cd your-hexo-site`

   `git clone https://github.com/iissnan/hexo-theme-next themes/next`

2.修改根目录下的配置文件 ![image](/images/image.png)  ![image1](/images/image1.png)
3. 然后你就可以在自己服务器跑一下,看看效果有没有出来(`hexo g` `hexo s`) 

4. 常用命令

   ```
   生成静态文件 hexo g
   ```

   ​

### 4.github page发布

1. 同样是修改上图中的 *_config.yml* 文件

   ```
   deploy:
     type: git
     //下面填上你的库源码地址
     repo: <repository url>
     //可以命名为master,直接在主分支上
     branch: [branch]
   ```
   repository url获取:
   ![image3](/images/image3.png)

2. 生成以及部署 

   首先需要安装一个模块:`npm install hexo-deployer-git --save`

   然后执行`hexo d` 就可以发布了,当中应该会让你输入github账号和密码

3. 如果是使用前面提到过的在其他目录下创建的库,可能发布后,会出不来页面,我之前遇到过无法加载js和css样式,这里应该是要更改如下地方:

   ![image4](/images/image4.png)

4. 发布文章:

   `hexo new test`

### 5.其他配置(~~我也没开始使用,哈哈~~)

1. 贴标签

    确认站点,主题的两个配置文件有`tags:tags`

    新建tags页面`hexo new page tags` 

    修改 *source/tags/index.md* 

     ```
     title: tags
     date: 2015-10-20 06:49:50
     type: "tags"
     comments: false

     ```

     > date 可保持系统生成的时间，

     ```
     type: "tags"
     comments: false	
     ```

2. 在文章中添加tags

    ```
    tags: 
    	- Tag1
    	- Tag2
    	- Tag3
    ```

> 最后,欢迎访问我的网站! [https://nico-m.github.io/](https://nico-m.github.io/) 

