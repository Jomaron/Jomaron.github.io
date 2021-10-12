---
layout: page
title: "关于我"
multilingual: true
---

<div class="zh post-container">
    <!--copied from markdown -->
    <blockquote><p>年轻人你的职责是平整土地，而非焦虑时光，<br>
    你做三四月的事情，在八九月自有答案。<br>
                                   --Motto</p></blockquote>

</div>

###  Hey~

<!-- Chinese Version -->
<div class="zh post-container">
    {% capture about_zh %}{% include about/zh.md %}{% endcapture %}
    {{ about_zh | markdownify }}
</div>

### English version

<!-- English Version -->
<div class="en post-container">
    {% capture about_en %}{% include about/en.md %}{% endcapture %}
    {{ about_en | markdownify }}
</div>


{% include comments.html %}
