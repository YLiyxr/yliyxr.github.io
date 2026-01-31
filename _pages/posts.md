---
layout: archive
title: "Selected Posts"
permalink: /posts/
author_profile: true
---

<div class="archive__item">
  {% for post in site.posts %}
    <article class="archive__item-teaser">
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p class="page__meta"><i class="far fa-clock" aria-hidden="true"></i> {{ post.date | date: "%B %d, %Y" }}</p>
      {% if post.excerpt %}
        <p class="archive__item-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
    </article>
    <hr />
  {% endfor %}
</div>
