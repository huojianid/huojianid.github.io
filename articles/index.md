---
layout: default
title: 全部文章
permalink: /articles/
seo_title: 小火箭文章列表｜Shadowrocket 教程与账号攻略全收录
description: i小火箭全部文章按时间倒序排列：Shadowrocket 下载安装、订阅配置、共享与独享账号选购、常见报错排查，持续更新。
keywords: 小火箭文章,Shadowrocket教程,小火箭攻略,Shadowrocket账号,i小火箭
---

<section class="page-hero">
  <h1>📚 全部文章</h1>
  <p>Shadowrocket 下载、账号选购、配置使用的全部原创教程，按时间倒序排列。</p>
</section>

<div class="post-list">
  {% assign latest = site.posts %}
  {% for post in latest %}
  <article class="post-row">
    {% if post.image %}
    {% assign img_src = post.image | replace: '.webp', '-thumb.webp' %}
    <a href="{{ post.url }}" class="row-img"><img src="{{ site.url }}{{ img_src }}" alt="{{ post.title }}" loading="lazy" width="1200" height="674"></a>
    {% endif %}
    <div class="row-body">
      <div class="row-meta">
        <time>{{ post.date | date: '%Y-%m-%d' }}</time>
        {% if post.category %}<a class="card-cat" href="{% include cat_url.html cat=post.category %}">{{ post.category }}</a>{% endif %}
      </div>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.description }}</p>
    </div>
  </article>
  {% endfor %}
</div>
