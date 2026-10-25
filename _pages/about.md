---
layout: page
title: The Team
subtitle: We are a diverse team with backgrounds in clinical medicine, medical statistics, nursing, pharmacy and public health. 
---

<p>We use this blog to share new findings, preprints, conference trips and methods notes.</p>
<p>Meet our core team members below, and visit our <a href="https://clinpath.short.gy/about">page</a> at the university website for a full list, including external research fellows.</p>
<div class="team-grid" style="padding:0; margin-top:24px;">

  {% for author in site.data.authors %}
  {% assign a = author[1] %}
  <div class="member">
    {% if a.photo %}
    <a href="{{ '/authors/' | relative_url }}#{{ author[0] | slugify }}" title="Posts by {{ a.name }}">
      <img class="avatar-lg" src="{{ a.photo | relative_url }}" alt="{{ a.name }}">
    </a>
    {% else %}
    <a href="{{ '/authors/' | relative_url }}#{{ author[0] | slugify }}" title="Posts by {{ a.name }}">
      <div class="avatar avatar-initials-lg">{{ a.name | slice: 0 }}{{ a.name | split: ' ' | last | slice: 0 }}</div>
    </a>
    {% endif %}
    <h3><a href="{{ '/authors/' | relative_url }}#{{ author[0] | slugify }}" class="member-name">{{ a.name }}</a></h3>
    {% if a.role %}<p class="role">{{ a.role }}</p>{% endif %}
    {% if a.bio %}<p>{{ a.bio }}</p>{% endif %}
    <div class="links">
      {% for link in a.links %}
      <a href="{{ link[1] }}">{{ link[0] }}</a>
      {% endfor %}
    </div>
  </div>
  {% endfor %}

</div>
