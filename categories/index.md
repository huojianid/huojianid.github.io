---
layout: default
title: 分类
permalink: /categories/
seo_title: 小火箭文章分类｜教程、账号、下载与问答导航
description: 按主题浏览 i小火箭的全部内容：使用教程、账号选购、下载安装与常见问题四大分类，快速找到需要的 Shadowrocket 配置步骤与账号说明。
keywords: 小火箭文章,Shadowrocket教程分类,小火箭教程导航,i小火箭
---

<section class="page-hero">
  <h1>🗂️ 文章分类</h1>
  <p>按主题浏览 Shadowrocket 相关的全部文章。</p>
</section>

<div class="cat-grid cat-grid-large">
  {% for cat in site.categories %}
  {% assign cat_name = cat[0] %}
  {% if cat_name != "categories" %}
  <a class="cat-card" href="{% include cat_url.html cat=cat_name %}">
    <span class="cat-name">{{ cat_name }}</span>
    <span class="cat-count">{{ cat[1] | size }} 篇</span>
  </a>
  {% endif %}
  {% endfor %}
</div>
