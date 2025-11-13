---
layout: program
title: Concert Program
permalink: /program/
---

# Concert Program

**{{ site.data.program.title }}**

{{ site.data.program.date }} at {{ site.data.program.time }}

{{ site.data.program.venue }}
{{ site.data.program.address }}

---

{% for section in site.data.program.sections %}
{% if section.title == "Intermission" %}

## Intermission

{% else %}

## {{ section.title }}

{% if section.items %}
{% for item in section.items %}

### {{ item.title }}

{% if item.performer %}
**{{ item.performer }}**
{% endif %}

{% if item.performers %}
{% for perf in item.performers %}
- {{ perf }}
{% endfor %}
{% endif %}

{% if item.accompaniment %}
*{{ item.accompaniment }}*
{% endif %}

{% if item.notes %}
*{{ item.notes }}*
{% endif %}

{% endfor %}
{% endif %}

{% endif %}
{% endfor %}
