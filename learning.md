---
layout: page
title: Learning
permalink: /learning/
---

<ul>
  {%- assign items = site.learning | sort: "date" | reverse -%}
  {%- for item in items -%}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      <small> — {{ item.date | date: "%Y-%m-%d" }}</small>
      {%- if item.tags -%}<small> · tags: {{ item.tags | join: ", " }}</small>{%- endif -%}
    </li>
  {%- endfor -%}
</ul>
