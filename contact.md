---
layout: default
title: Contact
permalink: /contact/
---

<section class="section">
  <div class="wrap">
    <p class="section__eyebrow">Contact</p>
    <h1 class="page-title">Get in touch</h1>
    <p class="page-lede">
      I'm happy to hear from prospective students, collaborators, and journalists. The fastest way
      to reach me is by email.
    </p>

    <div class="contact-grid">
      <div class="contact-card">
        <h3>Email</h3>
        <p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
      </div>
      <div class="contact-card">
        <h3>Phone</h3>
        <p>{{ site.phone }}</p>
      </div>
      <div class="contact-card">
        <h3>Department</h3>
        <p>{{ site.affiliation }}</p>
      </div>
      <div class="contact-card">
        <h3>Google Scholar</h3>
        <p><a href="{{ site.scholar_url }}" target="_blank" rel="noopener">View publications &amp; citation metrics</a></p>
      </div>
    </div>
  </div>
</section>
