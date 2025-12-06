---
layout: default
title: Csehy Benefit Concert
---

<section class="hero">
  <img class="banner-img" src="/assets/images/Krol Benefit Recital_Web Banner.jpg" alt="Csehy Benefit Concert - Support four young musicians raising funds to attend summer music camp." />
  <!-- <h1>Csehy Benefit Concert</h1>
  <p>Support four young musicians raising funds to attend summer music camp.</p> -->
  <p><strong>Date:</strong> <a href="https://calendar.google.com/calendar/render?action=TEMPLATE&text=Csehy+Benefit+Concert&dates=20260120T190000Z/20260120T210000Z&details=Support+four+young+musicians+raising+funds+to+attend+summer+music+camp.&location=1865+Waddle+Rd,+State+College,+PA+16803&ctz=America/New_York" target="_blank" rel="noopener" id="event-date" style="text-decoration: underline;">Tuesday, January 20, 2026 at 7:00 P.M. (EST)</a> &nbsp;|&nbsp; <strong>Venue:</strong> <a href="https://www.google.com/maps/dir/?api=1&destination=1865+Waddle+Rd,+State+College,+PA+16803" target="_blank" rel="noopener" id="event-venue" style="text-decoration: underline;">Oakwood Presbyterian Church</a></p>
  <p style="font-size: 0.95em; margin-top: 0.5rem;"><strong>Address:</strong> <a href="https://www.google.com/maps/search/1865+Waddle+Rd,+State+College,+PA+16803" target="_blank" rel="noopener" style="text-decoration: underline;">1865 Waddle Rd, State College, PA 16803</a></p>
  <p>
    <a class="btn primary" href="#donate">Donate</a>
    <a class="btn secondary" href="{{ '/program/' | relative_url }}">Concert Program</a>
    <a class="btn secondary" href="{{ '/performers/' | relative_url }}">Meet the performers</a>
    <a class="btn secondary" href="{{ '/csehy/' | relative_url }}">About Csehy</a>
  </p>
</section>

<section class="about">
  <h2>About the Concert</h2>
  <p>This benefit concert is organized by family and friends to help four talented young musicians attend a summer music camp. Your donation helps cover tuition, travel, and instrument needs.</p>
</section>

<section id="performers-preview">
  <h2>Student Performers</h2>
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
  <p>We accept donations via the mobile and written options below. Please choose the method that's most convenient.</p>
  
  <h3>Quick Mobile Payments (QR codes)</h3>
  <div class="payment-grid">
    <h4>For Josephine Kroeker</h4>
    <div class="payment-card">
      <div class="qr-container">
        <p><a href="https://venmo.com/KurtKroeker" target="_blank" rel="noopener">Venmo</a></p>
        <p><a href="https://venmo.com/KurtKroeker" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=https://venmo.com/KurtKroeker" alt="Venmo QR for KurtKroeker"></a></p>
      </div>
      <div class="qr-container">
        <p><a href="https://paypal.me/kurtkroeker" target="_blank" rel="noopener">PayPal</a></p>
        <p><a href="https://paypal.me/kurtkroeker" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=https://paypal.me/kurtkroeker" alt="PayPal QR for kurtkroeker"></a></p>
      </div>
    </div>
    <h4>For Elsa, Charlotte, and Alanna</h4>
    <div class="payment-card">
      <div class="qr-container">
        <p><a href="https://venmo.com/Erin-Krol-1" target="_blank" rel="noopener">Venmo</a></p>
        <p><a href="https://venmo.com/Erin-Krol-1" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=https://venmo.com/Erin-Krol-1" alt="Venmo QR for Erin-Krol-1"></a></p>
      </div>
      <div class="qr-container">
        <p><a href="https://www.paypal.com/paypalme/krolpeter" target="_blank" rel="noopener">PayPal</a></p>
        <p><a href="https://www.paypal.com/paypalme/krolpeter" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=100x100&data=https://www.paypal.com/paypalme/krolpeter" alt="PayPal QR for krolpeter"></a></p>
      </div>
    </div>
  </div>

  <h3>Written Checks</h3>
  <p>If you prefer to mail a check to the family you wish to support, please make the check payable to <strong>Csehy Summer School of Music</strong> and write <strong>"Kroeker camper fees"</strong> or <strong>"Krol camper fees"</strong> in the memo.</p>

  <h3>At the Recital</h3>
  <p>Two boxes (one for each family) are available in the back of the performance hall for cash or check donations. Please make checks payable to <strong>Csehy Summer School of Music</strong> and write <strong>"Krol camper fees</strong> or <strong>"Kroeker camper fees"</strong> in the memo.</p>
</section>

<footer>
  <!-- nothing to see here -->
</footer>
