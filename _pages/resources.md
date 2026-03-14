---
layout: page
title: Resources
permalink: /resources/
---

# Caregiver Resources

<div class="resources-list">
{% for resource in site.data.resources %}
<div class="resource-item">
{% if resource.url != "" and resource.url %}
<h3><a href="{{ resource.url }}" target="_blank">{{ resource.name }}</a></h3>
{% else %}
<h3>{{ resource.name }}</h3>
{% endif %}
<p>{{ resource.description }}</p>
{% if resource.phone %}
<p><strong>{{ resource.phone }}</strong></p>
{% endif %}
</div>
{% endfor %}
</div>
