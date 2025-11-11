---
layout: default
title: Csehy Benefit Concert
---

<section class="hero">
  <h1>Csehy Benefit Concert</h1>
  <p>Support four young musicians raising funds to attend summer music camp.</p>
  <p><strong>Date:</strong> <span id="event-date">TBD</span> &nbsp;|&nbsp; <strong>Venue:</strong> <span id="event-venue">TBD</span></p>
  <p>
    <a class="btn primary" href="#donate">Donate</a>
    <a class="btn secondary" href="{{ '/performers/' | relative_url }}">Meet the performers</a>
  </p>
</section>

<section class="about">
  <h2>About the Concert</h2>
  <p>This benefit concert is organized by family and friends to help four talented young musicians attend a summer music camp. Your donation helps cover tuition, travel, and instrument needs.</p>
</section>

<section id="performers-preview">
  <h2>Performers</h2>
  <ul>
    {% for p in site.data.performers %}
    <li class="performer-card">
      <img src="{{ '/assets/images/' | append: p.photo | relative_url }}" alt="Photo of {{ p.name }}" loading="lazy">
      <div>
        <h3>{{ p.name }}</h3>
        <p class="instrument">{{ p.instrument }}</p>
        <p class="bio">{{ p.bio }}</p>
      </div>
    </li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/performers/' | relative_url }}" class="btn tertiary">See all performers</a></p>
</section>

<section id="donate">
  <h2>Donate</h2>
  <p>We accept donations via an external donation page. Please click the Donate button to proceed.</p>
  <p><a class="btn donate" href="https://example.org/donate" id="donate-btn" target="_blank" rel="noopener">Donate securely</a></p>
</section>

<footer>
  <p>Contact: <a href="mailto:you@example.org">you@example.org</a></p>
</footer>