---
layout: archive
title: "Open Source"
permalink: /software/
author_profile: true
---

{% include base_path %}

Check out my <a href="https://gchochla.github.io/publications">Publication</a> for paper-specific code.
{% if author.github %}
  You can also find my open-source repositories on <u><a href="https://github.com/{{author.github}}">GitHub</a>.</u>
{% endif %}

{% for post in site.software reversed %}
  {% include archive-single.html %}
{% endfor %}
