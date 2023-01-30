---
title: 전체 스크랩 목록
layout: archives-posts-all
---
<div class="archives archive-type-collections">
{% for collection in site.collections %}

<article class="entry entry-format-list-item">
  <h3 class="entry-title">{{ collection.label }}</h3>
  <div class="entry-body">
{% for post in site[collection.label] %}
    <a href="{{ post.url }}">{% if post.title and post.title != "" %}{{post.title}}{% else %}{{post.excerpt |strip_html}}{%endif%}</a>
{% endfor %}
  </div>
</article>

{% endfor %}
</div>
