---
layout: default
title: All Games
permalink: /gaming-thoughts/all
---
<div>
{% assign filtered_posts = site.posts | where: "category", "gaming-thoughts" %}
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
{%- if filtered_posts.size > 0 -%}
{%- for post in filtered_posts -%}
  <a href="{{ post.url | relative_url }}" title="{{ post.title }}">{{ post.date | date: date_format }} - {{ post.title }}</a>
  <br/>
{%- endfor -%}

{%- endif -%}
</div>