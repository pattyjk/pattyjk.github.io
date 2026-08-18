---
layout: default
title: Publications
permalink: /publications/
---

<section class="section">
  <div class="wrap">
    <p class="section__eyebrow">Publications</p>
    <h1 class="page-title">Selected &amp; complete publication record</h1>
    <p class="page-lede">
      {{ site.data.publications.size }} peer-reviewed papers spanning microbial ecology, host-microbe
      interactions, and biogeochemistry. Full record and citation metrics on
      <a href="{{ site.scholar_url }}" target="_blank" rel="noopener">Google Scholar</a>.
      My name is bolded within each author list.
    </p>

    {% assign pubs_by_year = site.data.publications | group_by: "year" %}
    {% for group in pubs_by_year %}
      <div class="pub-year-group">
        <h2 class="pub-year">{{ group.name }}</h2>
        <ul class="pub-list">
          {% for pub in group.items %}
          <li class="pub-item">
            <p class="pub-authors">{{ pub.authors | markdownify | remove: "<p>" | remove: "</p>" }}</p>
            <p class="pub-title">{{ pub.title }}</p>
            <p class="pub-venue">
              {{ pub.journal }}{% if pub.volume and pub.volume != "" %}, {{ pub.volume }}{% endif %}{% if pub.number and pub.number != "" %}({{ pub.number }}){% endif %}{% if pub.pages and pub.pages != "" %}: {{ pub.pages }}{% endif %}
            </p>
          </li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>
</section>
