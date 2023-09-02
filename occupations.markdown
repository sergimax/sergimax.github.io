---
layout: page
title: Занятость
permalink: /occupations/
---

Тут будет история моей занятости и обучения

<!-- https://stackoverflow.com/questions/30933741/jekyll-cant-sort-collection-by-date -->
{% assign sorted = site.occupations | reverse %}
{% for occupation in sorted %}
**{{occupation.position}}** - {{occupation.company}}
<br><sup>{{occupation.from}} - {{occupation.to}}</sup>
<!-- TODO Сделать вывод techStack в цикле -->
<br><sup>{{occupation.techStack}}</sup>
{{occupation.content}}
{% endfor%}