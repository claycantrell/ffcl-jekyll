---
layout: page
title: Publications
permalink: /publications/
---

# Publications

Interested in obtaining a copy of an article listed below? Email [ffcl@usc.edu](mailto:ffcl@usc.edu) to request access.

<div class="publications-list">
<ul>
{% for pub in site.data.publications %}
<li>{{ pub.citation }} <a href="{{ pub.doi }}" target="_blank">DOI</a></li>
{% endfor %}
</ul>
</div>
