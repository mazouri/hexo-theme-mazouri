

### Introduction 前言

这个主题是基于Yilia -Yelee的，原作者做个不少功能和特性。今后我也会根据自己的喜好修改下风格，效果可参见：[Mazouri的博客](http://mazouri.me/)


### Installation 安装主题

```
git clone https://github.com/mazouri/hexo-theme-mazouri.git themes/mazouri
```

Change theme field in Hexo root's _config.yml file. 修改 Hexo 根目录对应配置文件。

```
theme: mazouri
```

### Update 更新
注意先备份theme下_config.yml文件

```
cd themes/mazouri
git pull
```


### Configuration 配置

#### 0. Post Excerpt 文章摘要
There are two ways to show excerpt in homepage. 

目前主题可使用两种方式在首页显示文章摘要而不是全文。

- a: <!-- more -->

``` diff
title: Hello World
date: 2015-12-03 00:00:00
---
<Excerpt in index | 首页摘要> 
+ <!-- more -->
<The rest of contents | 余下全文>
```
- b: description in Front-matter

``` diff
title: Hello World
date: 2015-12-03 00:00:00
+ description: "Welcome to Hexo! This is your very first post."
---
<Contents>
```

> Description only support plain text. | 通过 description 添加的摘要只能为纯文本。

> Set the value of description with quotes to avoid unexpected error `:`. | description 的内容加双引号，可以避免一些程序错误，例如内容里包含英文冒号时。



#### 1. About Page 关于我页面: 

使用以下代码添加一个新页面：

```
hexo new page about
```

#### 2. Tags Cloud Page 标签云页面:

```
hexo new page tags
```

> Post with several categories 文章设置多个分类后的问题 [issue#4](https://github.com/MOxFIVE/hexo-theme-yelee/issues/4) 

> - [让 Hexo 自动生成 Tag Cloud 标签云页面](http://moxfive.xyz/2015/10/25/hexo-tag-cloud/)

#### 3. Background image 网页背景:

Find or change background images in folder | 修改背景图地址: 

> `/mazouri/source/background/`

Setting in `themes/mazouri/_config.yml` 背景参数:

`
background_image: 5
`

- Default value is 5, free to modify the number | 默认值为5，可按需修改

- "5": show 5 images form bg-1.jpg to bg-5.jpg in `/mazouri/source/background/`

- "5": 设置`/mazouri/source/background/`文件夹中 bg-1.jpg 到 bg-5.jpg 这5张图片为背景

- "0": remove background image and use white-gray theme | 取消网页背景图，使用淳朴的灰白主题 

#### 4. Style image 自定义图片样式:
In order to style posts/pages' image with HTML/CSS within `.md` files, you should disable fancybox function firstly. 

如果要使用 HTML/CSS 自定义文章图片样式，需要先关闭 fancybox 功能。

Disable fancybox in full site | 在全站关闭 fancybox:

> Set `fancybox: false` in `mazouri/_config.yml`

Disable fancybox in certain post/page | 在某篇文章中关闭 fancybox:

> Add `fancybox: false` in [front-matter](https://hexo.io/docs/front-matter.html)

#### 5. Comment 评论:
Disqus, duoshuo and youyan is supported, enable them in theme's "_config.yml".
主题目测支持 Disqus，多说 和友言评论，自行在主题配置中开启。

多说: http://duoshuo.com/create-site/ 登陆你的多说并创建站点，在 "domain" 中填入你设定的域名。请设置好自己专属的多说，不要再群聊了。

> - [保留使用 Yilia 主题时的多说用户评论](https://github.com/MOxFIVE/hexo-theme-yelee/issues/1)

> - [多说样式折腾记录 — 添加 UA 浏览器标识、旋转头像等](http://moxfive.xyz/2015/09/29/duoshuo-style/)

#### 6. Table of Contents 文章目录:

Remove toc and the button via putting `toc: false` before "---" at [post].md.

文章中默认显示目录和对应切换按钮，在文章 “---” 前输入 `toc: false` 关闭目录。

#### 7. Copyright info. 文章版权信息:

Hide this  via putting `original: false` to post's front-matter.

在文章顶部插入行 `original: false` 关闭文章版权声明框

#### 8. 404 Page:

```
hexo new page 404
```
And then set `permalink: /404` in `/source/404/index.md` front matter.

> - [在 Hexo 中创建匹配主题的404页面](http://moxfive.xyz/2015/10/16/hexo-404-page/)

#### 9. RSS Feed 文章订阅:

Install plugin: [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)

#### 10. Sitemap for SEO 站点地图:

Install plugin: [hexo-generator-seo-friendly-sitemap](https://github.com/ludoviclefevre/hexo-generator-seo-friendly-sitemap)

百度专用: [hexo-generator-baidu-sitemap](https://github.com/coneycode/hexo-generator-baidu-sitemap)

#### 11. Apple Touch icon 苹果图标:

替换路径: `/mazouri/source/apple-touch-icon.png`

[Recommended size: 180*180](https://realfavicongenerator.net/blog/apple-touch-icon-the-good-the-bad-the-ugly/)

更多请转：
1. https://github.com/litten/hexo-theme-yilia
2. http://litten.github.io/ "Litten的博客"
3. https://github.com/MOxFIVE/M-Hexo-Blog/commits/master
4. https://github.com/MOxFIVE/hexo-theme-yelee/commits/master
5. http://moxfive.xyz/2015/08/20/blog-building/ "个人博客站点建设历程"
6. http://moxfive.xyz
