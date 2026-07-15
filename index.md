---
layout: default
title: 首页
---

<section class="hero">
  <h1>欢迎来到我的博客</h1>
  <p>这里记录我关于生存和生活的思考。</p>
</section>

<section class="latest-posts">
  <h2>最新文章</h2>
  
  {% for post in site.posts limit:5 %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%Y年%m月%d日" }}</p>
    <p class="post-excerpt">{{ post.excerpt }}</p>
    <a href="{{ post.url }}" class="read-more">继续阅读 →</a>
  </article>
  {% endfor %}
  
  {% if site.posts.size == 0 %}
  <p>还没有发布文章，敬请期待！</p>
  {% endif %}
</section>

<style>
  .hero {
    text-align: center;
    padding: 2rem;
    background: linear-gradient(135deg, rgba(102,126,234,0.1), rgba(118,75,162,0.1));
    border-radius: 8px;
    margin-bottom: 2rem;
  }
  
  .hero h1 {
    color: #667eea;
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }
  
  .hero p {
    font-size: 1.2rem;
    color: #666;
  }
  
  .post-preview {
    border-bottom: 1px solid #eee;
    padding: 1.5rem 0;
  }
  
  .post-preview:last-child {
    border-bottom: none;
  }
  
  .post-preview h3 {
    margin-top: 0;
  }
  
  .post-preview h3 a {
    color: #667eea;
    text-decoration: none;
  }
  
  .post-preview h3 a:hover {
    text-decoration: underline;
  }
</style>
