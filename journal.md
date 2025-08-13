---
layout: page
title: Learning Journal
permalink: /journal/
---

Here are my learning journal entries (newest first):

<ul>
  {%- assign entries = site.journal | sort: "date" | reverse -%}
  {%- for item in entries -%}
    <li>
      <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
      <small> — {{ item.date | date: "%Y-%m-%d" }}</small>
      {%- if item.tags and item.tags.size > 0 -%}
        <small> · tags: {{ item.tags | join: ", " }}</small>
      {%- endif -%}
    </li>
  {%- endfor -%}
</ul>

_Add more files under the **_journal/** folder to grow this section._