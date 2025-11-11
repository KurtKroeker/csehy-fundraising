---
layout: default
title: Performers
---

# Performers

Below are the four musicians performing at the benefit concert. Click a card to view the full bio and any media.

<ul style="padding:0;list-style:none;">
{% for performer in site.performers %}
  <li style="margin:1rem 0;padding:0;border-bottom:1px solid #eee;display:flex;gap:1rem;align-items:center;">
    {% if performer.photo %}
      <a href="{{ performer.url | relative_url }}">
        <img src="{{ '/assets/images/' | append: performer.photo | relative_url }}" alt="Photo of {{ performer.name }}" style="width:96px;height:96px;object-fit:cover;border-radius:8px;">
      </a>
    {% endif %}
    <div>
      <a href="{{ performer.url | relative_url }}" style="text-decoration:none;color:inherit;">
        <h2 style="margin:.1rem 0;">{{ performer.name }}</h2>
      </a>
      <p style="margin:.1rem 0;font-weight:600;">{{ performer.instrument }}</p>
      <p style="margin:.25rem 0;color:#444;">{{ performer.excerpt | default: performer.bio | strip_html | truncate:120 }}</p>
    </div>
  </li>
{% endfor %}
</ul>