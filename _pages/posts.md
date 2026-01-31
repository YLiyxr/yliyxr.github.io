---
layout: default
title: "Selected Posts"
permalink: /posts/
author_profile: true
---

# Selected Posts

---

<div class="posts-container">
  {% for post in site.posts %}
    <div style="margin-bottom: 2rem; border-bottom: 1px solid #eee; padding-bottom: 1rem;">
      <h2 style="margin-bottom: 0.5rem;">
        <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: #0366d6;">{{ post.title }}</a>
      </h2>
      <div style="color: #666; font-size: 0.9rem; margin-bottom: 1rem;">
        <span>📅 {{ post.date | date: "%B %d, %Y" }}</span>
        {% if post.categories %}
          <span style="margin-left: 15px;">🏷️ {{ post.categories | join: ", " }}</span>
        {% endif %}
      </div>
      <div style="line-height: 1.6;">
        {{ post.excerpt | strip_html | truncate: 200 }}
      </div>
      <a href="{{ post.url | relative_url }}" style="display: inline-block; margin-top: 10px; font-weight: bold; font-size: 0.9rem;">Read More →</a>
    </div>
  {% endfor %}
</div>
