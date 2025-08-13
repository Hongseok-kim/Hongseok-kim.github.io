---
layout: page
title: Thoughts
permalink: /thoughts/
---

<ul>
  {%- assign items = site.thoughts | sort: "date" | reverse -%}
  {%- for item in items -%}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      <small> — {{ item.date | date: "%Y-%m-%d" }}</small>
      {%- if item.tags -%}<small> · tags: {{ item.tags | join: ", " }}</small>{%- endif -%}
    </li>
  {%- endfor -%}
</ul>
