---
layout: post
title: People
image: assets/images/people_new.png
permalink: people/index.html
---


## Current Members
{% for person in site.data.current_members %}
<div id="person-im">
<figure>

{% if person.link != none %}
<b> <a href="{{person.link}}">{{ person.name }}</a></b><br/>
{% else %}
<b> {{person.name}} </b>
{% endif %}
<img src="{{ site.baseurl }}/assets/images/people/{{ person.image }}.jpg"><br />
{{ person.title }}<br />
<figcaption>
{% if person.name == 'Juliana Navia Pelaez' %}
<span style="font-size: 10pt;"> {{ person.email }}  </span><br />
{% endif %}
{% if person.name != 'Juliana Navia Pelaez' %}
<span style="font-size: 10pt;">      {{ person.email }} </span><br />
{% endif %}
<span class="stretch"></span>
</figcaption>
</figure>
</div>
{% endfor %}
<br/>
<br/>
