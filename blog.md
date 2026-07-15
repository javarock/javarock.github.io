---
layout: default
title: 博客
permalink: /blog/
---

# 所有文章

{% if site.posts.size == 0 %}
  <p>还没有发布文章。</p>
{% else %}
  <div class="post-list">
    {% for post in site.posts %}
    <article class="post-item">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%Y年%m月%d日" }}
        </time>
        {% if post.author %}
          | 作者：{{ post.author }}
        {% endif %}
      </p>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ post.url }}" class="read-more">继续阅读 →</a>
    </article>
    {% endfor %}
  </div>
{% endif %}

<style>
  .post-list {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  
  .post-item {
    border: 1px solid #eee;
    padding: 1.5rem;
    border-radius: 4px;
    transition: box-shadow 0.3s;
  }
  
  .post-item:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  }
  
  .post-item h3 {
    margin-top: 0;
  }
  
  .post-item h3 a {
    text-decoration: none;
  }
  
  .post-item h3 a:hover {
    text-decoration: underline;
  }
</style>
