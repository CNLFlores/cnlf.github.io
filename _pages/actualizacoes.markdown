---
layout: single
title: Publicações
permalink: /publicacoes/
header:
  image: /assets/images/ambos.jpeg
  og_image: /assets/images/ambos.jpeg
---


<h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}