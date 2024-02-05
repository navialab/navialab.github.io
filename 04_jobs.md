---
layout: post
title: Jobs
image: assets/images/jobs.png
permalink: jobs/index.html
---
{% assign pub_serv = "http://www.navialab.info/jobs/" %}

# We are recruiting!!!
We are thrilled to build a diverse team of enthusiasts and curious scientists where everyone is welcome.
Your contribution will help strengthen the Navia Lab. Come join the fun!

{% for topic in site.data.jobs %}

<!-- Title is stored as the key, so index at 0 -->
<h2> {{ topic[0] }} </h2>

<!-- Other info is stored as the value, so index at 1 -->
{% assign var = topic[1] %}


{{ var.description }}
<br />

{% endfor %}

