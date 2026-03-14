---
layout: page
title: Our Team
permalink: /our-team/
---

# Our Team

<div class="team-grid">
{% assign leaders = site.data.team | where: "group", "leadership" %}
{% for member in leaders %}
  <div class="team-card">
    <img src="{{ '/assets/images/team/' | append: member.photo | relative_url }}" alt="{{ member.name }}" class="team-photo">
    <h3 class="team-name">{{ member.name }}</h3>
    <p class="team-title">{{ member.title }}</p>
    <p class="team-bio">{{ member.bio }}</p>
  </div>
{% endfor %}
</div>

## Research Assistants

<div class="team-grid">
{% assign ras = site.data.team | where: "group", "research_assistants" %}
{% for member in ras %}
  <div class="team-card">
    <img src="{{ '/assets/images/team/' | append: member.photo | relative_url }}" alt="{{ member.name }}" class="team-photo">
    <h3 class="team-name">{{ member.name }}</h3>
    <p class="team-title">{{ member.title }}</p>
    <p class="team-bio">{{ member.bio }}</p>
  </div>
{% endfor %}
</div>
