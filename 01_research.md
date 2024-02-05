---
layout: post
title: Research
image: assets/images/panel2.png
permalink: research/index.html
---
{% for topic in site.data.research_members %}

<!-- Title is stored as the key, so index at 0 -->
<h2> {{ topic[0] }} </h2>

<!-- Other info is stored as the value, so index at 1 -->
{% assign var = topic[1] %}

<img style="display: block; margin: auto; max-width: 100%;" src="{{ site.baseurl }}/assets/images/{{ var.image }}">

{{ var.description }}
<br />

{% endfor %}
