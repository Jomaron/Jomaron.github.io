---
layout:     post
title:      个人博客搭建，概要总结
subtitle:   一个开始
date:       2021-9-11
author:     Jomaron
tags:
    - Blog
    - jekyll
---


### 博客介绍
[jomaron](https://jomaron.top) 该博客模板的特征如下：

 * 简洁的响应式[主页]，适配电脑、手机屏幕。
 * [博客主页]：以 Abstract 模块化显示文章。
 * [所有文章]：以时间点罗列文章。
 * [标签]：基于文章标签，进行博客分栏。
 * 基于[来必力]的评论功能，支持QQ\微信\微博\百度等接口登录。

点击下面链接看效果：

 * [本文博客链接](https://jomaron.top/) （个人站）         
 * [Github Demo链接](https://jomaron.github.io/) （github）         


### 环境搭建
Jekyll 与 Github Pages到底什么关系？如果一开始没搞清这一点，会踩很多坑！！！

好多fork量过百的博客项目，都会来一句“这是利用 GitHub Pages 与 Jekyll 搭建的个人博客”。然后却没一篇文章说清楚 Jekyll 到底怎么用，纳尼？

可查看Github pages官方文档说明：[Github pages](https://docs.github.com/cn/pages)



##### 是否必要搭建Jekyll环境，有三种情况：

当不想fork别人的项目（fork？不是有手就行，没意思~啥也学不到）

1). If 你想自己手动 Jekyll + Github Pages 搭建个人博客，需搭建Jekyll环境。

步骤：
* 在Github里面new Repositoy创建新的仓库，用于构建自己的博客。
* 下载使用开源主题模板。[JekyllThemes.org](http://jekyllthemes.org/)和[JekyllThemes.io](https://jekyllthemes.io/)
* 搭建Jekyll 环境，并创建自己的博客站点。

具体过程请查看相关博文：[Jekyll + Github Pages搭建个人博客详细教程1](https://zhuanlan.zhihu.com/p/87225594)

当想fork别人的项目（嗯，，fork真香~）

2). If 你想在创作博客的过程中能够实时的在本机预览生成的效果，也需搭建Jekyll环境。

步骤：
* fork别人的博客项目，并修改项目名和相关配置文件。
* 搭建Jekyll 环境。
* 创建博客文章，通过jekyll server获取服务地址：http://localhost:4000/，并在浏览器中访问查看预览。
* 最后commit并push到Github上。

具体过程请查看相关博文：[Jekyll + Github Pages, fork搭建个人博客详细教程2](https://github.com/qiubaiying/qiubaiying.github.io/wiki/%E5%8D%9A%E5%AE%A2%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B)

[基于 GitHub Pages 和 Jekyll 搭建个人博客的简单心得](https://www.bilibili.com/video/BV14x411t7ZU?from=search&seid=15722768050730991661&spm_id_from=333.337.0.0)

3). If 你是计算机小白，只想专注于博客内容的创作，那么你也可无需Jekyll。

步骤：
* fork别人的博客项目，并修改项目名和相关配置文件。
* 创建博客文章。
* commit并push到Github。

具体过程请查看相关博文：[有手就行，搭建个人博客详细教程3](https://github.com/qiubaiying/qiubaiying.github.io)


### Windows系统下 Jekyll 的安装

在此之前，请先安装 git工具包，以及Python。Jekyll 是一个静态网站生成器，其依赖于Ruby。因此安装步骤如下：
1. 安装Ruby
2. 安装DevKit
3. 安装RubyGems
4. 安装Bundler
5. 最后才能安装 Jekyll

##### 具体如下
1. Ruby的安装，进入[Jekyll官网](http://jekyllcn.com/)，打开[Jekyll 运行于Windows上](http://jekyllcn.com/docs/windows/#installation)部分，点击[Get started]按钮，进入新界面点击[Get Ruby for Windows] 按钮，进入下载界面进行Ruby的下载与安装。

踩坑1. Ruby官网提供三种安装包，点击右上角[Archives](https://rubyinstaller.org/downloads/archives/) 可详细查看。根据网上教程如果单独下载安装[RubyInstallers] 与 [DevKits]，Jekyll 安装失败，更换多个版本试了很多次都不成功，很无奈！

解决方案：卸载Ruby ，下载[Ruby+Devkit Installers]安装包并安装，结果Jekyll安装成功。

2. Ruby安装完会有个选项，让你安装MSYS2，默认勾选并选择3，该过程会安装很多包，耐心等待，安装完后会让你继续选择123，直接Enter退出即可。如果开始未勾选，安装之后cmd输入“ridk install”进行MSYS2的安装也可。

    * 测试Ruby是否安装成功，cmd 命令运行“Ruby -v”，及“gem -v”，输出版本号即可。gem 是Ruby的一个工具包，相当于Python里面的pip。

3. 为确保Jekyll安装顺利，继续单独安装DevKit,官网[Jekyll官网](https://rubyinstaller.org/downloads/archives/)下载[DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe]，对应64位系统。

4. RubyGems安装 ,[下载RubyGems](https://rubygems.org/pages/download/),下载安装包，解压到你需要的目录下，cmd运行“ruby setup.rb”执行安装。

5. Bundler安装,cmd运行"gem install bundler" 执行安装。

6. 以上安装缺一不可，然后安装Jekyll ,执行命令“gem install jekyll”,安装成功即可。

jekyll的安装要求比较高，本人也是重复好多遍，装了卸，卸了装，建议有一点遗漏就重新整个过程。

参考博文：[windows系统下安装jekyll](https://segmentfault.com/q/1010000013418668/a-1020000013529937)


### Github Pages

1. 想自己动手搭建的，在Github里面new Repositoy。
注意事项：
 * 需以username.github.com 为仓库名。username必须为你的Github用户名，最好为小写名称。
 * 选择Public。README可有可无，因为后面找的主题模板里面都有。
 * 将项目clone到本地。
2. fork了别人项目的
 * 修改项目名同上，并修改相关_config.yml配置信息，以及相关页面信息。
 * 将项目clone到本地。


### 配置域名

为什么需要自己的域名？据说由于百度爬虫的原因，导致Github Pages无法被百度索引。于是购买一个域名可解决上述问题，你特有的域名也是对自己的一种投资，个人认为还是值得的。
提供两个平台：[阿里云](https://wanwang.aliyun.com/domain/?spm=5176.8006371.1007.dnetcndomain.q1ys4x)和[GoDaddy](https://sg.godaddy.com/zh)

步骤：
1. 购买域名
2. 解析域名
3. 修改CNAME

配置 GitHub Pages 站点的自定义域
[Github 官方文档说明](https://docs.github.com/cn/pages/configuring-a-custom-domain-for-your-github-pages-site)


### 推荐几个优秀博客模板

感谢以下作者的主题模板，以及详细的教程说明，喜欢的朋友可以fork，记得Star一下哦。

1. [优源](https://duter2016.github.io/)，[Github地址](https://github.com/Duter2016)
2. [Hux Blog](https://huangxuan.me/)，[Github地址](https://github.com/huxpro) 
3. [BY Blog](http://qiubaiying.vip/)，[https://github.com/qiubaiying)


### 致谢
1. 本文模板fork自[leopardpan 潘柏信](https://github.com/leopardpan)，郑重感谢作者创作的精美主题。
2. 感谢 [Jekyll](http://jekyllcn.com/)、[Github pages](https://docs.github.com/cn/pages)。

### Licence

遵循 MIT 许可证。有关详细,请参阅[LICENSE](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository#disclaimer)
