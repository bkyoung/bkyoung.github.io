---
title: Recipe Blog
layout: default
---
{% assign sorted_pages = (site.posts | sort: 'title') %}
{% for page in sorted_pages %}
<div class="row">
  <div class="col-sm-12">
    <a href="{{ page.url }}"><h3>{{ page.title }}</h3></a>
    <small><em>{{ page.author }} ({{ page.date | date: "%A %B %-d, %Y" }}</em>)</small><br/><br/>
  </div>
</div>
{% endfor %}