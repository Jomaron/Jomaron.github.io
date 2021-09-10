---
layout: page
title: 关于我
description: "Jomaron Blog"
header-img: "images/background-cover.jpg"
multilingual: true
---

{% include multilingual-sel.html %}

<!-- Chinese Version -->
<div class="zh post-container">
    {% capture about_zh %}{% include about/zh.md %}{% endcapture %}
    {{ about_zh | markdownify }}
</div>

<!-- English Version -->
<div class="en post-container">
    {% capture about_en %}{% include about/en.md %}{% endcapture %}
    {{ about_en | markdownify }}
</div>


<div class="zh post-container">
    <p>感谢作者<strong> 潘柏信 </strong>打造的精美主题</p>

    <p>博客源码在 <a target="_blank" href='https://github.com/leopardpan/leopardpan.github.io/'>Github</a> 上，支持作者的, Star 一下~</p>
    <p>相关教程如下：</p>
    <p><a href="/2016/10/jekyll_tutorials1/"> Jekyll 搭建个人博客 </a></p>
    <p>搭建博客遇到了<strong>问题</strong>，请查看相关博文，或在下面 [留言~]</p>  
 
</div>

{% include comments.html %}

