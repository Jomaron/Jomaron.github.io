---
layout: page
title: 关于我
description: "Jomaron Blog"
header-img: "images/background-cover.jpg"
---

<div class="zh post-container">

    <!--copied from markdown -->
    <blockquote><p>任何的限制<br>
    都是从自己的内心开始的</p></blockquote>

    <p>Hey，我是<strong>邱万勇(Jomaron)</strong>，一枚脑科学研究生，北京理工大学博士在读。</p>
    <p>这是利用 <a href="https://pages.github.com/">GitHub Pages</a> 与 <a href="http://jekyll.com.cn/">Jekyll</a> 搭建的个人博客，在此记录自己的科研学习</p>
    
    <p>GitHub主页<a href="https://github.com/jomaron">👉GitHub·Jomaron</a> 与 CSDN主页<a href="https://blog.csdn.net/qiu1440528444">👉万勇Blog</a>，欢迎留言~提出探讨~</p>
    

    <h5>Link</h5>

    <ul>
        <li><a href="https://github.com">GitHub</a></li>
        <li><a href="http://jekyll.com.cn/">jekyll</a></li>
    </ul>
</div>

<!-- English Version -->
<!-- <div class="en post-container">
    <blockquote><p>Yet another iOS Developer. <br>
    Yet another Life-long Student.</p></blockquote>

    <p>Hi, I am <strong>Wanyong Qiu</strong>，you can call me <strong>Jomaron</strong>. I am a postgraduate in brain science and a PhD candidate in Beijing Institute of Technology.</p>

    <p>This is my personal blog, through making Github Pages and Jekyll.My GitHub  👉 <a href="http://github.com/Jomaron">Github·Jomaron</a>.</p>

    <h5>Talks</h5>

    <ul>
    <li><a href="https://github.com">GitHub</a></li>
    <li><a href="http://jekyll.com.cn/">jekyll</a></li>
    </ul>
</div> -->

<!-- Handle Language Change -->
<script type="text/javascript">
    // get nodes
    var $zh = document.querySelector(".zh");
    var $en = document.querySelector(".en");
    var $select = document.querySelector("select");

    // bind hashchange event
    window.addEventListener('hashchange', _render);

    // handle render
    function _render(){
        var _hash = window.location.hash;
        // en
        if(_hash == "#en"){
            $select.selectedIndex = 1;
            $en.style.display = "block";
            $zh.style.display = "none";
        // zh by default
        }else{
            // not trigger onChange, otherwise cause a loop call.
            $select.selectedIndex = 0;
            $zh.style.display = "block";
            $en.style.display = "none";
        }
    }

    // handle select change
    function onLanChange(index){
        if(index == 0){
            window.location.hash = "#zh"
        }else{
            window.location.hash = "#en"
        }
    }

    // init
    _render();
</script>


<div class="zh post-container">
    <p>感谢作者<strong> 潘柏信 </strong>打造的精美主题</p>

    <p>博客源码在 <a target="_blank" href='https://github.com/leopardpan/leopardpan.github.io/'>Github</a> 上，支持作者的, Star 一下~</p>
    <p>相关教程如下：</p>
    <p><a href="/2016/10/jekyll_tutorials1/"> Jekyll 搭建个人博客 </a></p>
    <p>搭建博客遇到了<strong>问题</strong>，请查看相关博文，或在下面 [留言~]</p>  
 
</div>

{% include comments.html %}

