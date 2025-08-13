---
layout: page
title: Hobbies
permalink: /hobbies/
---

A mix of personal interests. Recent entries:

<ul>
  {%- assign entries = site.hobbies | sort: "date" | reverse -%}
  {%- for item in entries -%}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      <small> — {{ item.date | date: "%Y-%m-%d" }}</small>
      {%- if item.category -%}
        <small> · {{ item.category }}</small>
      {%- endif -%}
    </li>
  {%- endfor -%}
</ul>

_Add more files under the **_hobbies/** folder (e.g., travel, books, recipes)._