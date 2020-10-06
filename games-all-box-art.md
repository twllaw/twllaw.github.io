---
layout: default
title: All Games
permalink: /gaming-thoughts/all-box-art
---
[Go to list view](/gaming-thoughts/all)
<div>
{% assign filtered_posts = site.posts | where: "category", "gaming-thoughts" %}
{%- if filtered_posts.size > 0 -%}
<div class="content-container">
  {%- for post in filtered_posts -%}
  <div class="box-image-container">
    <a class="post-link" href="{{ post.url | relative_url }}" title="{{ post.title }}">
      <img class="box-image" src="{{ post.box-art}}" alt="{{ post.box-art-desc }}">
    </a>
  </div>
  {%- endfor -%}
</div>

{%- endif -%}
</div>