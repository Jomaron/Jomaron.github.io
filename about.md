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




{% include comments.html %}

