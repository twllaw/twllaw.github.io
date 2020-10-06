---
layout: default
title: All Games
permalink: /gaming-thoughts/all
---
<div>
{%- if site.posts.size > 0 -%}
<div class="content-container">
  {%- for post in site.posts -%}
  <div class="box-image-container">
    <a class="post-link" href="{{ post.url | relative_url }}" title="{{ post.title }}">
      <img class="box-image" src="{{ post.box-art}}" alt="{{ post.box-art-desc }}">
    </a>
  </div>
  {%- endfor -%}
</div>

{%- endif -%}
</div>