---
layout: page
# FIXME Возможно, стоит разделить на отдельные страницы
title: Учеба и работа
permalink: /occupations/
---

Тут будет история моей занятости в обучении, а также профильной и непрофильной работе

<!-- TODO Разбивка на профильный и непрофильный опыт -->

<!-- https://stackoverflow.com/questions/30933741/jekyll-cant-sort-collection-by-date -->
<!-- {% assign sorted = site.occupations | reverse %} -->
{% for occupation in sorted %}
**{{occupation.position}}** - {{occupation.company}}
<!-- TODO Сделать расчет времени по занятости https://stackoverflow.com/questions/31340018/get-the-difference-in-days-between-two-dates-in-jekyll -->
<br><sup>{{occupation.from}} - {{occupation.to}}</sup>
<!-- TODO Сделать вывод techStack в цикле -->
<br><sup>{{occupation.techStack}}</sup>
{{occupation.content}}
{% endfor%}