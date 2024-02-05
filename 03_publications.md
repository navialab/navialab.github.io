---
layout: post
title: Publications
image: assets/images/publications.png
permalink: publications/index.html
---


<!-- Section for publications. Don't add them here directly. Add new publications to /data/pubs.yaml. The following code reads directly from that file. -->
## Publications

{% assign pub_serv = "http://www.navialab.info/publications/" %}
{% for year in site.data.pubs %}
<span style="display: block; width: 100%; text-align: center; font-size: 18pt; font-weight: 600;">{{ year[0] }}</span>
{% for paper in year %}
{% for p in paper %}
{% assign links = p.links %}

**{{ p.title }}** by {{ p.author }} <i>{{ p.journal }}</i>
  {{ p.volume  }} {{ p.number }} {{ year[0] }}. {% for val in links %} \|{% if val[0] == 'DOI' %}<a href="{{val[1]}}" target="_blank">DOI</a> {% elsif val[1] contains 'http' %} <a href="{{val[1]}}" target="_blank"> {{val[0]}}</a>{% else %} <a href="{{pub_serv}}{{val[1]}}" target="_blank"> {{val[0]}}</a>{% endif %} {% endfor %}{% endfor %}
{% endfor %}
{% endfor %}



