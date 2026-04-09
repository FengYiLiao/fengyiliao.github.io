---
title: "Notes"
permalink: /notes/
layout: home
author_profile: true
classes: wide
---

<!-- This is a place for short notes, paper summaries, and technical thoughts.

{% assign sorted_notes = site.notes | sort: "date" | reverse %}
{% for note in sorted_notes %}
- {{ note.date | date: "%Y-%m-%d" }} [{{ note.title }}]({{ note.url }})
  {% if note.excerpt %}
  > {{ note.excerpt | strip_html | strip }}
  {% endif %}
  {% if note.tags %}
  {% for tag in note.tags %}
  `{{ tag }}`
  {% endfor %}
  {% endif %}

{% endfor %} -->