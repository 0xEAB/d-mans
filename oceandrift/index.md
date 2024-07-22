---
layout: default
title: Oceandrift
---

# Oceandrift D-Man collection

by Elias A. Batek ([@0xEAB](https://github.com/0xEAB)).  
License: [CC-BY-4.0](./COPYING.txt).

<div>
{% assign sorted_files = site.static_files | sort: 'path' -%}
{% for file in sorted_files -%}
  {%- assign pageurl = page.url | replace: 'index.html', '' -%}
  {%- if file.path contains pageurl -%}
    {%- if file.extname == '.svg' or file.extname == '.png' %}
<img src="{{ site.baseurl }}{{ file.path }}" alt="{{ file.basename }}" style="max-width:30%">
    {%- endif -%}
  {%- endif -%}
{% endfor -%}
</div>
