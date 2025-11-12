---
layout: default
title: Csehy Benefit Concert
---

<section class="hero">
  <h1>Csehy Benefit Concert</h1>
  <p>Support four young musicians raising funds to attend summer music camp.</p>
  <p><strong>Date:</strong> <a href="https://calendar.google.com/calendar/render?action=TEMPLATE&text=Csehy+Benefit+Concert&dates=20260120T190000Z/20260120T210000Z&details=Support+four+young+musicians+raising+funds+to+attend+summer+music+camp.&location=1865+Waddle+Rd,+State+College,+PA+16803&ctz=America/New_York" target="_blank" rel="noopener" id="event-date" style="text-decoration: underline;">Tuesday, January 20, 2026 at 7:00 P.M. (EST)</a> &nbsp;|&nbsp; <strong>Venue:</strong> <a href="https://www.google.com/maps/dir/?api=1&destination=1865+Waddle+Rd,+State+College,+PA+16803" target="_blank" rel="noopener" id="event-venue" style="text-decoration: underline;">Oakwood Presbyterian Church</a></p>
  <p style="font-size: 0.95em; margin-top: 0.5rem;"><strong>Address:</strong> <a href="https://www.google.com/maps/search/1865+Waddle+Rd,+State+College,+PA+16803" target="_blank" rel="noopener" style="text-decoration: underline;">1865 Waddle Rd, State College, PA 16803</a></p>
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