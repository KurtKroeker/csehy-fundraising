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
    <a class="btn secondary" href="{{ '/program/' | relative_url }}">Concert Program</a>
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
  <p>We accept donations via the mobile and written options below. Please choose the method that's most convenient.</p>
  
  <h3>Quick Mobile Payments (QR codes)</h3>
  <div class="payment-grid">
    <div class="payment-card">
      <h4>For Josephine Kroeker</h4>
      <p>Venmo (to Kurt Kroeker on behalf of Josephine): <a href="https://venmo.com/KurtKroeker" target="_blank" rel="noopener">venmo.com/KurtKroeker</a></p>
      <p><a href="https://venmo.com/KurtKroeker" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://venmo.com/KurtKroeker" alt="Venmo QR for KurtKroeker"></a></p>
      <p>PayPal (to Kurt Kroeker on behalf of Josephine): <a href="https://paypal.me/kurtkroeker" target="_blank" rel="noopener">paypal.me/kurtkroeker</a></p>
      <p><a href="https://paypal.me/kurtkroeker" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://paypal.me/kurtkroeker" alt="PayPal QR for kurtkroeker"></a></p>
    </div>

    <div class="payment-card">
      <h4>For Elsa, Charlotte, and Alanna</h4>
      <p>Venmo (to Erin Krol on their behalf): <a href="https://venmo.com/Erin-Krol-1" target="_blank" rel="noopener">venmo.com/Erin-Krol-1</a></p>
      <p><a href="https://venmo.com/Erin-Krol-1" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://venmo.com/Erin-Krol-1" alt="Venmo QR for Erin-Krol-1"></a></p>
      <p>PayPal (to Peter Krol on their behalf): <a href="https://www.paypal.com/paypalme/krolpeter" target="_blank" rel="noopener">paypal.com/paypalme/krolpeter</a></p>
      <p><a href="https://www.paypal.com/paypalme/krolpeter" target="_blank" rel="noopener"><img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://www.paypal.com/paypalme/krolpeter" alt="PayPal QR for krolpeter"></a></p>
    </div>
  </div>

  <h3>Written Checks</h3>
  <p>Make checks payable to <strong>Kurt Kroeker</strong>. In the memo line, please indicate which performer(s) the check is for (for example, "For Josephine Kroeker"). If you prefer, checks for Elsa, Charlotte, or Alanna may also be made payable to <strong>Erin Krol</strong>; either way, please note the performer name(s) in the memo.</p>
  <p>Mailing or drop-off instructions: contact the organizers at <a href="mailto:you@example.org">you@example.org</a> for the preferred mailing address or drop-off details.</p>

  <h3>Cash Policy</h3>
  <p>We gladly accept cash donations at the event. Please bring the exact amount if possible and include the donor name and intended performer(s). Receipts are available upon request. For larger donations, we encourage using an electronic payment method or contacting the organizers so we can provide an official receipt.</p>
</section>

<footer>
  <p>Contact: <a href="mailto:you@example.org">you@example.org</a></p>
</footer>