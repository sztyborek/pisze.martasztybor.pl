---
layout: blog
title: Blog
permalink: /inne-teksty/
---

<section class="post-list clearfix">
  <h2 class="section-heading">Najnowsze posty</h2>
  {% for post in site.posts %}
    <article class="post-list__item">
      <img src="{{ post.image | prepend: site.baseurl }}" alt="">
      <header class="post-list__header">
        <h3 class="post-list__item-title">
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-list__link">
            {{ post.title }}
          </a>
        </h3>
        <p class="post-list__item-meta">
          {{ post.date | date: site.date_format }} &mdash; {{ post.categories[0] }}
        </p>
        <p class="post-list__summary">
          {{ post.summary }}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-list__read-more">Czytaj dalej &rarr;</a>
        </p>
      </header>
    </article>
  {% endfor %}
  {% include pagination.html %}
</section>