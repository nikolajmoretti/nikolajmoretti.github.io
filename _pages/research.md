---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<style>
.archive__item-title { font-size: 1em; }
.archive__item p { font-size: 0.85em; }
</style>

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<h2>Publications</h2>
{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}


<h2>Working Papers</h2>
{% for post in site.workingpapers reversed %}
  {% include archive-single.html %}
{% endfor %}

<h2>Work in Progress</h2>
{% for post in site.work_in_progress reversed %}
  {% include archive-single-teaching.html %}
{% endfor %}
